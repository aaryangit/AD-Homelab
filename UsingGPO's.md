## **Using Group Policy Object**

To enforce any policy like having certain Desktop background for certain departments or restricting users from accessing certain files or softwares on the Workstations we can use GPO's to enforce this.  
In this example we will implement having a certian background for a dept and they cant change it.

Go to the top right corner and select "Group Policy management".  

<img width="1256" height="699" alt="image" src="https://github.com/user-attachments/assets/31838f85-85c2-431f-b734-6ec9f167babb" />  

Right click on the OU or the group to enforce the policy. I have selected the Engineering OU here.  

<img width="468" height="389" alt="image" src="https://github.com/user-attachments/assets/01594caa-aaa1-41f7-b945-d779147e00b9" />  

Set the Name of the GPO you want to set.  

<img width="407" height="203" alt="image" src="https://github.com/user-attachments/assets/ee79444c-8f39-44eb-bc14-49b44afe8065" />  

Right click on it to Edit and set the actual policies.  

<img width="599" height="109" alt="image" src="https://github.com/user-attachments/assets/35876a79-f5ee-485f-83ed-dd4e6f5978f4" />  

Now on the right hand side you can find various folders and preset conditions to enforce. Now since this concerns a user's Desktop background navigate to the Users Config ---> Administrative template ---> Desktop.  
Right click on Desktop wallpaper to edit the properties.  

<img width="473" height="356" alt="image" src="https://github.com/user-attachments/assets/3ded9e01-9a6d-4a6b-a136-97ec603902eb" />  

Click on Enable and copy the image as its path which you can paste in the input box and click "Apply".  

<img width="676" height="648" alt="image" src="https://github.com/user-attachments/assets/966c62f6-61ea-41df-83b3-55d4f1852f8d" />  

Now for users to prevent changing it we can create another GPO. So follow the same steps shown above create a Lockscreenbg GPO for the same group.  
Navigate to the Users policy ---> administrative templates ---> control panel ----> personalization. ( Have to explore a bit to understand the templates)).  

<img width="784" height="539" alt="image" src="https://github.com/user-attachments/assets/5e215365-792c-4bf1-8a85-50d09800fb73" />  

Right click on prohibit changing Desktop background and select Enable.   

<img width="683" height="597" alt="image" src="https://github.com/user-attachments/assets/230616e4-f2e4-41b3-99fd-211f4a5197c8" />


Now to verify login as a member from the group on the windows endpoint.   

<img width="1283" height="812" alt="image" src="https://github.com/user-attachments/assets/af79fc75-d2e0-447d-8d92-05a774032095" />





