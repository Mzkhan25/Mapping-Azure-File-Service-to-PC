In this tutorial, we’ll be seeing on how we can map azure file storage drives to our windows machine.

Starting our tutorial, once we have logged in our Azure portal, we need to click on “New”.

   ![1](https://user-images.githubusercontent.com/14289218/30209909-addeaae2-94b3-11e7-967b-a1c29b355e9f.png)

Now we’ll click on “Storage” and choose “Storage account”. 

![2](https://user-images.githubusercontent.com/14289218/30209907-add99bf6-94b3-11e7-9254-cc1d6c62377f.png)

Let’s choose the name of our storage account, along with resource group.

![3](https://user-images.githubusercontent.com/14289218/30209912-ade49ede-94b3-11e7-8489-21abdaf1325e.png)

Once it’s created, we’ll choose our created File Storage from our resources. 

![4](https://user-images.githubusercontent.com/14289218/30209908-addb5612-94b3-11e7-9f9c-09a214dc4607.png)

Now let’s click on “Files” 

![5](https://user-images.githubusercontent.com/14289218/30209910-addfbdce-94b3-11e7-816f-3dd542a8ee2e.png)

![6](https://user-images.githubusercontent.com/14289218/30209911-ade074e4-94b3-11e7-9315-37e803dc39ee.png)

Let’s click on “+ File Share” and enter the name for our file service. We can also mention the size of our disk by writing it in “Quota”. 

In-case we leave it blank, maximum size (5 TiB ) will be allocated for the drive. 

![7](https://user-images.githubusercontent.com/14289218/30209914-ae06ea7a-94b3-11e7-9845-3ba0e7bda2f8.png)

Once our file service is clicked, we’ll click on it 
 
![8](https://user-images.githubusercontent.com/14289218/30209913-ae0675cc-94b3-11e7-9c0e-874b8751d983.png)

![9](https://user-images.githubusercontent.com/14289218/30209915-ae0facbe-94b3-11e7-8559-898b522c09b2.png)

Now, we’ll click on “Connect”

![10](https://user-images.githubusercontent.com/14289218/30209916-ae10191a-94b3-11e7-8ed9-fa34dafcb96c.png)

Now, we’ll copy the path of our drive. It’s the highlighted text from above picture. Important thing is that we need a specific part from it. 

The path which we need starts from “\\\” and goes uptil our service’s name. So, in or context, our path becomes
“\\\mappingtutorial.file.core.windows.net\testmapping “.

Now, let’s open our file explorer and click on “Map Network Drive”
 
![11](https://user-images.githubusercontent.com/14289218/30209918-ae1a200e-94b3-11e7-8c1e-8dda5ad2993e.png)
 
![12](https://user-images.githubusercontent.com/14289218/30209917-ae10d382-94b3-11e7-8606-0fd9042a619e.png)
 
Let’s paste the above copied path in folder and check “Connect using different credentials”. 

![13](https://user-images.githubusercontent.com/14289218/30209919-ae34c846-94b3-11e7-9305-d8012174492b.png)

A pop up asking for credentials would appear. These credentials are found under “Access keys” of our Storage Account
 
![14](https://user-images.githubusercontent.com/14289218/30209920-ae35e514-94b3-11e7-8adc-06ef6405b956.png)

![15](https://user-images.githubusercontent.com/14289218/30209921-ae54c650-94b3-11e7-89a3-bea6d5b10334.png) 

The text in “Storage account name” is our username and “Key” value in “Key1” and “Key2” is our password. So let’s copy paste them in our Credentials Prompt
 
![16](https://user-images.githubusercontent.com/14289218/30209922-ae548f50-94b3-11e7-8864-8da0984ac7a2.png)

![17](https://user-images.githubusercontent.com/14289218/30209923-ae560b96-94b3-11e7-9866-7909e247faa7.png)

Check “Remember my credentials” and click “Ok”

If entered Username and Password is correct, it will automatically create a new networked drive on our Pc. 
 
![18](https://user-images.githubusercontent.com/14289218/30209924-ae67987a-94b3-11e7-82eb-8fd4ccebf174.png)

Now let’s just place any file in this drive and see how it’s mapped to our Azure File Service

![19](https://user-images.githubusercontent.com/14289218/30209925-ae70ebc8-94b3-11e7-8fbf-f8dd7f3f25ab.png)

I’ve added this file manually from my PC and it should be uploaded to Azure automatically. 

![20](https://user-images.githubusercontent.com/14289218/30209926-ae757f44-94b3-11e7-9664-36e9d34cd88e.png)

We can view and share the URL of this file by clicking it. 

![21](https://user-images.githubusercontent.com/14289218/30209927-ae8c6a1a-94b3-11e7-94c6-bc59b301032e.png)


This is one of the few methods of mapping our Azure File Service to PC, consecutively this is also achievable by Powershell and Command Prompt Command (CMD). 

Official documentation of File Storage:
https://azure.microsoft.com/en-us/services/storage/files/
