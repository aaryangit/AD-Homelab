## **Creating an Active Directory HomeLab**

This is a documentation of the Active Directory HomeLab hosted on Virtual Machines. The documentation covers the deployement of the AD and the connected Windows Endpoint and creation of shares and usage of Group policy (GPO) to implement policies.

## **Technical requierments**
System-  Storage ~ 40-50 GB | 16GB /32GB RAM (preferred) Host System  
ISO files- Windows Server 22/2025 .iso | Windows 10/11 .iso  
HyperVisor- VirtualBox / VMWare.  

## **Implementation**
Download the ISO files which are mentioned above from the official Microsoft WebPage. 
On the HyperVisor (I have used VirtualBox) first create a NAT Network from tools section as shown in the picture below

![Screenshot 2025-10-06 211437](https://github.com/user-attachments/assets/a1662eae-430f-49d7-847d-1a3564be6fd2)

Now Add both the .iso files to the VirtualBox   
Specs- Windows Server 2025:- RAM = 8 gigs | 4 processors  
       Windows 10 Endpoint:- RAM = 6 gigs | 3 processors  
       Network :- The "NAT Network" that we created and make sure to check the Cable Forwarding and keeping the same adapter. If the adapter or network is different the VMs can't locate each other.

<img width="681" height="372" alt="image" src="https://github.com/user-attachments/assets/c998d3ae-c0f7-4e67-b56c-ef87eb17544d" />

## **Windows Server**
After installing the ISO you'll get a homepage like this  
<img width="1347" height="552" alt="image" src="https://github.com/user-attachments/assets/f195aa40-46c7-45fc-bd65-b0df2e75bb73" />  

On the top right corner you can "Add roles or Features" where we can install AD DS (Active Directory Domain Services) and AD CS (Active Directory Certificate Services) where it acts as Certificate Authority and install DNS services.  
<img width="798" height="559" alt="image" src="https://github.com/user-attachments/assets/173329cd-9401-4787-a7a7-dd75ad450553" />  

<img width="789" height="577" alt="image" src="https://github.com/user-attachments/assets/70764f82-4786-4add-baa1-8a1cfda68904" />    

Here you can see the name of the server and IP address  

<img width="793" height="573" alt="image" src="https://github.com/user-attachments/assets/c1c837ff-fdcd-4d75-8083-459f36d8ca85" />  

Here we select the Active Directory Domain Services   

<img width="775" height="556" alt="image" src="https://github.com/user-attachments/assets/d048eec4-ef13-4329-be53-a926b28ee265" />    
  
<img width="974" height="554" alt="image" src="https://github.com/user-attachments/assets/ca807c05-5f26-417b-9e6a-c6cfcc6ac095" />  

<img width="773" height="541" alt="image" src="https://github.com/user-attachments/assets/d148f8bc-83e7-49d1-acf8-ab1e205cb108" />  

**Click on Promote to Domain Controller**  
<img width="756" height="562" alt="image" src="https://github.com/user-attachments/assets/a16e2dcf-7152-4890-b9c7-ccad7a4eca26" />  
  
<img width="766" height="565" alt="image" src="https://github.com/user-attachments/assets/85a274a9-8948-429d-94f7-fcaa99bc1b1b" />  

**Don't forget to Click on DNS for DC capabilities** and set a secure password as its a AD admin password  

<img width="755" height="562" alt="image" src="https://github.com/user-attachments/assets/9f65bc4c-01d0-48b4-a258-8af51220788a" />   

<img width="775" height="562" alt="image" src="https://github.com/user-attachments/assets/3d65be4d-5ad7-4f7a-a7b9-b4582551bbbb" />   

<img width="856" height="584" alt="image" src="https://github.com/user-attachments/assets/ee5fdeae-b0cc-48cf-9dbf-94fb68260f58" />  

These alerts are okay and you can ignore them and click install  

**After this installation the system reboots and now you can login as an Admin with the password you just set**  
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Just as a Good installation practice and for the connected devices to securely communicate with the DC and to authenticate the certificates issued by we are configuring it to be a root CA.  
For that again to top right corner and select "Add users and roles" and select Azure Directory Certificate Services (AD CS) and keep all the deafault settings for now.  

<img width="820" height="573" alt="image" src="https://github.com/user-attachments/assets/7bcee8a9-6166-4dce-b675-c2f6fbb1f5f5" />    

                                          
<img width="768" height="540" alt="image" src="https://github.com/user-attachments/assets/7cfdc923-9316-4f17-9120-0488e301079c" />  

<img width="754" height="552" alt="image" src="https://github.com/user-attachments/assets/69b0a728-fdee-40f3-a312-4f7dc35ae3cf" />  

<img width="767" height="553" alt="image" src="https://github.com/user-attachments/assets/aa2331b8-973c-449e-a974-e07bfc3b2d28" />  

<img width="772" height="565" alt="image" src="https://github.com/user-attachments/assets/18fe7907-66d5-47e8-ba6f-de4827ffaa31" />  

<img width="754" height="559" alt="image" src="https://github.com/user-attachments/assets/a12abd0b-43fb-42b9-a0d5-4fd938a79c83" />  

Now the Key for Self signed Root CA is stored on the server and since its a private key make sure no unauthorized entity is able to access it or the whole integrity of the AD is compromised.  

## **IP Configuration and DNS provisioning**
So for the lab we are using the Domain Controller as the DNS server, as if we use the defualt google or Microsoft DNS server, they cant resolve the DNS queries for our Domain and the AD setup will render useless.  
Hence due to lack of a dedicated DNS server, we will use DC as a DNS server and will configure static IPs for both the DC and Windows Endpoint to avoid connectivity issues after reboot due to DHCP.   

<img width="1083" height="577" alt="image" src="https://github.com/user-attachments/assets/d4bd99e8-69a6-4f54-985a-bd6a050adcfa" />  

Here we can see the configuration of DC with its DNS configured to itself.  

<img width="820" height="669" alt="image" src="https://github.com/user-attachments/assets/d3f7ff3b-10c9-4e11-a0a8-6cbd34b3f354" />  

The IP configuration of the Workstation.  

On the Workstation you can connect to the domain with entering the user or admin credentials. 


## **To divide the lab in different sections, the creation of users and groups is documented on a different page linked below**

**Creating Users and OU's in AD - https://github.com/aaryangit/AD-Homelab/blob/main/CreatingUsers.md**




## **Key learnings**
1. Configuration of Active Directory on a Windows Server using it as a Domain Controller, DNS server and CA and configuring its Endpoints.  
2. Creation of Users and Shared folders in AD.  
3. Using GPO's to enforce policies.   


## **This lab is for educational purpose only and insprired by the Content generated by TCM-SEC academy.**






















