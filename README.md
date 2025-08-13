# Azure Secure Infrastructure for a Web Application
  ### Created by Drayton Rolle

  ---

## 📝 Project Summary
 This project demonstrates the foundational steps for building a secure and scalable infrastructure for a modern web application using Microsoft Azure. The primary goal was to establish a secure network, implement proper identity and access controls following the Principle of Least Privilege, and enable continuous security monitoring. This project reflects a security-first mindset for cloud deployments.

 This project was built to showcase core competencies in cloud security, networking, and identity management, which are critical skills for Cloud Engineering and Cybersecurity roles.

 ---

 ## 🚀 Key Features & Concepts Demonstrated

 * **Secure Network Architecture:** Deployed a Virtual Network (VNet) with three distinct subnets (Web, App, DB) to properly segment resources and control traffic flow.

 * **Network Security Groups (NSGs):** Implemented NSG rules to act as a stateful firewall, allowing only necessary web traffic to the web server.

 * **Role-Based Access Control (RBAC):** Created a custom `Virtual Machine Operator` role with the minimum required permissions to manage a VM, demonstrating the Principle of Least Privilege.

 * **Identity and Access Management (IAM):** Assigned the custom role to a user at a specific resource group scope, ensuring granular control over permissions.

 * **Cloud Security Posture Management (CSPM):** Enabled Microsoft Defender for Cloud to continuously assess the security posture of the deployed resources, identify vulnerabilities, and provide security recommendations.

 * **Resource Management:** Organized all project components within a single Resource Group for effective management and cleanup.

 ---

 ## 🏛️ Architecture Overview

 The infrastructure consists of the following components:

 1.  **Resource Group (`SecuredAppRG`):** A logical container for all project resources.

 2.  **Virtual Network (`AppVNet`):** A private network in Azure with three subnets:

     * `WebSubnet`: Contains the web server VM.
     * `AppSubnet`: Reserved for future application servers.
     * `DbSubnet`: Reserved for a future database.

 3.  **Network Security Group (`WebSubnet-nsg`):** Associated with the `WebSubnet` and configured with inbound rules to allow HTTP/HTTPS traffic.

 4.  **Virtual Machine (`WebServer01`):** An Ubuntu Server VM deployed into the `WebSubnet` to act as the front-end web server.

 5.  **Microsoft Defender for Cloud:** Enabled at the subscription level to monitor the security of all deployed resources.

 ---

 ## 📸 Portfolio Screenshots

 *(To complete this section, take screenshots of your Azure portal and upload them to a folder named `images` in this GitHub repository. Then, replace the descriptions below with the actual images using the format `![Description](images/your-screenshot-name.png)`)*

 **1. Network Topology**
 *A screenshot of your VNet diagram showing the three subnets.*
 `![Network Diagram](images/network-diagram.png)`

 **2. Custom Role Permissions**
 *A screenshot of the "Permissions" tab for your `Virtual Machine Operator` custom role.*
 `![Custom Role Permissions](images/custom-role.png)`

 **3. Role Assignment**
 *A screenshot of the "Role assignments" screen showing your user assigned the custom role.*
 `![Role Assignment](images/role-assignment.png)`

 **4. Microsoft Defender for Cloud - Secure Score**
 *A screenshot of the Defender for Cloud dashboard showing the Secure Score for your resources.*
 `![Defender for Cloud Score](images/defender-score.png)`
