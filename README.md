**Active Directory Homelab — Windows Server & Domain Environment**

This project documents my hands-on Active Directory (AD) homelab setup, built to simulate an enterprise-grade identity and access management environment.  
It demonstrates how core IT infrastructure concepts — such as user authentication, DNS, Group Policy, and Certificate Services — work together in a secure, isolated environment.  

---------------------------------------------------------------------------------------------------------------------------------------------------------------


🧰 **Tech Stack**  
Component	Description  
Windows Server 2025	- Domain Controller, DNS, and CA.  
Windows 10          - Client Domain-joined workstation.  
Virtualization      -	Oracle VirtualBox.  
Networking          -	Internal NAT network with static IPs.  

---------------------------------------------------------------------------------------------------------------------------------------------------------------

⚙️ **Key Configurations**

Set static IPs for DC and client machines.  
Configured DNS resolution for domain communication.  
Created organizational units, users, and groups.  
Deployed a root Certificate Authority (CA) with private key for internal use.  
Implemented basic GPOs for demonstration of locking desktop background.  
Tested domain logon and remote access scenarios.  

---------------------------------------------------------------------------------------------------------------------------------------------------------------

🔐 **Learning Outcomes**  

Deepened understanding of identity management and authentication flows.  
Gained practical experience with Microsoft enterprise services.  
Built a foundation for Azure AD hybrid integration and certificate-based login.  
Enhanced troubleshooting, documentation, and IT administration skills.  

---------------------------------------------------------------------------------------------------------------------------------------------------------------

📘 **Future Enhancements**  

Add RADIUS / NPS server integration.  
Implement hybrid Azure AD join and Intune management.  
Configure certificate-based (passwordless) authentication.  
Integrate SIEM logging (Splunk / Wazuh) for security monitoring.  

---------------------------------------------------------------------------------------------------------------------------------------------------------------

## **Inspired by the Course materials taught in TCM-SEC academy**
