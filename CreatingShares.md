## **Creating Shares**  

Here we will look at creating Shares to manage Effective sharing of documents with the users of a particular Group while others are not able to access those folders and files.  

Open the Server Dashboard and on the left panel click on Files and storage services.  

<img width="224" height="354" alt="image" src="https://github.com/user-attachments/assets/a768d21c-c858-448c-ad3a-8a88f9d1672e" />  

Then go to shares and click on "Tasks" and select on "New Share".  

<img width="826" height="388" alt="image" src="https://github.com/user-attachments/assets/8a369158-92c2-4247-9647-60e65beee15d" />  

<img width="762" height="552" alt="image" src="https://github.com/user-attachments/assets/0ab5383d-f2a0-4827-9480-ef939f68b6a0" />  

Keep hitting next until you land on this page. Here you can input the name of the new share that you want to create, I will be using the one i previously created which is showed in the File linked below.  

<img width="806" height="587" alt="image" src="https://github.com/user-attachments/assets/da43c028-b728-4bfe-ac6b-41d8cca28e2b" />  

<img width="723" height="368" alt="image" src="https://github.com/user-attachments/assets/5edc8f01-6521-4adc-bb4a-94bcf4db23f6" />  

Click on "Customize Permissions".  

<img width="986" height="583" alt="image" src="https://github.com/user-attachments/assets/2fdb90ac-979b-435d-ad5f-fdd7a97b003e" />  

In the image above you can see all the permission entries. But we cant allow everyone to access it hence we have to make some permission changes. To start with click on Disable Inheritance and click on first option.  

<img width="548" height="305" alt="image" src="https://github.com/user-attachments/assets/9fd4e865-762f-403c-a94c-86ce9afe5af2" />  

Following this remove everything apart from the one listed below.  

<img width="769" height="514" alt="image" src="https://github.com/user-attachments/assets/ba7f805d-f58a-440b-93aa-3c504709cb91" />  

Then click on "ADD" and then "select Principal" as seen below.  

<img width="946" height="514" alt="image" src="https://github.com/user-attachments/assets/85c25560-be7d-4dcd-b732-bda64a6c3f6f" />  

Enter the name of the group that you want to create the share for. I entered "EngineeringShare" that i created before.  

<img width="486" height="307" alt="image" src="https://github.com/user-attachments/assets/a01ef6e2-3c3a-424b-94fb-b5fc6c481b21" />  

Give the following permissions to it.  

<img width="935" height="503" alt="image" src="https://github.com/user-attachments/assets/eb3ef565-c2c9-44d8-9dab-cafcc83068be" />  

Go on hitting next and then create. Once its created you can see it like this.  

<img width="772" height="575" alt="image" src="https://github.com/user-attachments/assets/c06325fc-8622-461c-9b3e-afc66c8503de" />  

## **Checking the implementation**  

Go to the Windows Endpoint and sign in as a user who is in the group "EnginneeringShare".  

<img width="1059" height="822" alt="image" src="https://github.com/user-attachments/assets/8bbde456-ed49-43d3-a1fc-9116a55967a5" />  

In the file explorer you can search for the following share and then Map it to the empty drive to access easily next time.  

<img width="1004" height="737" alt="image" src="https://github.com/user-attachments/assets/c5f71666-0102-4eb0-8e96-fd2c80e424cc" />  

<img width="770" height="535" alt="image" src="https://github.com/user-attachments/assets/9e981b1f-7cda-4f3a-a07a-a77344672709" />


## **Additional documenetation can be found here**

**Lab setup:- https://github.com/aaryangit/AD-Homelab/blob/main/LAB%20setup.md**

**Creating Users:- https://github.com/aaryangit/AD-Homelab/blob/main/CreatingUsers.md**
















