<div align="center">
<img src=https://static.wixstatic.com/media/1c706c_a5df0ad56f894928bf858a74ba744b32~mv2.png/v1/fit/w_2500,h_1330,al_c/1c706c_a5df0ad56f894928bf858a74ba744b32~mv2.png width="400" height="200">
 </div>

# <div align="center"> JENKINS HANDS-ON </p>

# <div align="center"> DevOps Instructor-led Training </div>

# <div align="right"> $`\textcolor{brown}{\text{Contact us: }}`$  &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; </div>

<div align="right"> T O A C C E L E R A T E Y O U R C A R E E R G R O W T H </div>

### <div align="right"> For questions and more details: </div>

<div align="right"> <img src=https://w7.pngwing.com/pngs/759/922/png-transparent-telephone-logo-iphone-telephone-call-smartphone-phone-electronics-text-trademark-thumbnail.png width="20" height="20"> +91 98712 72900 </div>

<div align="right"> <img src=https://pbs.twimg.com/profile_images/1450734615946219520/jmBHQRRa_400x400.jpg width="20" height="20"> https://www.thecloudtrain.com </div>

<div align="right"> <img src=https://icons.iconarchive.com/icons/martz90/circle/512/email-icon.png width="20" height="20"> support@thecloudtrain.com </div>

<div align="right"> <img src=https://png.pngtree.com/png-vector/20221018/ourmid/pngtree-whatsapp-icon-png-image_6315990.png width="20" height="20"> +91 98712 72900 </div>

## JENKINS HANDS-ON

1. **Create 3 instances (Master, Slave1, Slave2) on Linux server.**
2. **Install Jenkins on Master. (Refer the above steps or the Jenkins installation documentation)**
3. **Set up a Jenkins Master-Slave Cluster**
4. **Create a CI CD pipeline triggered by Git Webhook.**

## Install Jenkins

[Refer official documentation](https://www.jenkins.io/doc/book/installing/linux/) for installation steps. 

[Refer offline plugin download page](https://updates.jenkins.io/download/plugins/).

[Refer this repo for homework](https://github.com/vistasunil/jenkins-terraform-docker-webinar.git).

[Refer this repo to install Jenkins on Kubernetes Cluster](https://github.com/vistasunil/Jenkins-on-Kubernetes.git)

First, we have created 3 instances Master Slave1and Slave2. And then we have installed the Jenkins on Master Machine. Now Let us set up the Jenkins Master-Slave Cluster.

### Step 1: Check the status of the Jenkins first.

`service jenkins status`

![image](https://user-images.githubusercontent.com/37858762/236325469-8b58cf0a-500c-4b8a-928a-f523da2b3242.png)

### Step 2: Now open browser and enter _**http://`<master-public-IP`>:8080**_

You should land on a page like this:

![image](https://user-images.githubusercontent.com/37858762/236325442-30eec6b4-e8a9-4695-84d4-e2d7b46aae8c.png)

### Step 3:Copy the path mentioned in the page and perform cat operation in master terminal.

`sudo cat <path>`

![image](https://user-images.githubusercontent.com/37858762/236325431-bfb42a82-0253-453b-8904-384f9f08942a.png)

This will give us the password which we will use to unlock our Jenkins.

Copy the password from there and paste it on the Jenkins Server page.

![image](https://user-images.githubusercontent.com/37858762/236325404-4fdb3136-78f3-4ac9-9a10-b6104384534a.png)

Now click on continue. Then click on Install Suggested Plugins.

![image](https://user-images.githubusercontent.com/37858762/236325389-2fdfb048-d934-402f-82ba-d6840bb8a05c.png)

### Step 4: Once done, enter the Admin User details.

![image](https://user-images.githubusercontent.com/37858762/236325369-48e9dc24-c1f1-4c23-ad16-450d16185c44.png)

Then click on **Save and Continue**.

![image](https://user-images.githubusercontent.com/37858762/236325341-1a609634-429a-4de5-b88a-3ea76724086f.png)

Again, click **Save and Finish**. Click on **Install Suggested Plugins.** Once it's done we will land on a page as shown below.

![image](https://user-images.githubusercontent.com/37858762/236325322-a59ee2bd-202c-491e-8fe1-f777e69ac103.png)

This is our **Jenkins Dashboard**.

## Hands-On: Configure Slave nodes

### Step 5: Go to **Manage Jenkins**. Click on **Configure Global Security.**

![image](https://user-images.githubusercontent.com/37858762/236325282-f127604e-e77e-44dc-b834-92a54dcb5a66.png)

### Step 6: Change the **Agents** to **Random**. Then click on **Save**.

![image](https://user-images.githubusercontent.com/37858762/236325265-63196af3-1bfc-4603-975d-7ab5ca6b87cd.png)

### Step 7: Now go to **Manage Nodes**. 

![image](https://user-images.githubusercontent.com/37858762/236325188-533022f8-c886-4b4f-8e8e-5fa2718e94fb.png)

### Step 8: Click on **New Node.** Add **Slave1** as new node and make **Permanent Agent**. Click on **ok**.

![image](https://user-images.githubusercontent.com/37858762/236325169-cbad64f6-f6c3-4033-b26b-4041700a0b4e.png)

![image](https://user-images.githubusercontent.com/37858762/236325152-118320ba-29eb-456e-a1ad-c1a6300752b1.png)

### Step 9: Go to **Launch method** change it to **Launch agent by connecting it to the controller.**

![image](https://user-images.githubusercontent.com/37858762/236325136-3c09a6c4-6ec9-4a2f-9a4f-83b5c9332bde.png)

### Step 10: Then add the current working directory path to **/home/ubuntu/jenkins.** Then click on **Save.**

![image](https://user-images.githubusercontent.com/37858762/236325125-2f888c5b-bb2f-43f9-98d6-e8fee6d46dde.png)

### Step 11: Make another node **Slave2** and copy from **Slave1 as** shown below: 

![image](https://user-images.githubusercontent.com/37858762/236325104-3f1e9a34-a001-4f50-9b80-a976a1ca5c4a.png)

### Step 12: Then click ok. You can see the list of nodes that we have on the Jenkins Dashboard.

![image](https://user-images.githubusercontent.com/37858762/236325085-d38e8064-0a5e-457b-a479-6635bbe8e5c6.png)

### Step 13: Go to the Jenkins Dashboard, Click on **Slave1**. Download the **Agent.jar** file by clicking on it.

![image](https://user-images.githubusercontent.com/37858762/236325062-bc798d38-34b0-4784-9fdc-c28c489b2020.png)

### Step 14: Now download **agent.jar** file and upload on the ubuntu server using scp, winscp or filezilla.

### Step 15: Let us verify if the file has been transferred to **Slave1** or not. Open a new session on putty. Connect to slave1. Run **ls command.**

![image](https://user-images.githubusercontent.com/37858762/236325041-411f2795-df6a-49be-9629-0c903d3a5a60.png)

As you can see the agent.jar file appears there, which means our file has been successfully transferred to **Slave1.**

### Step 16: Perform the steps for Slave2 as well. (Tip: Rename the agent.jar file of **Slave2.**

![image](https://user-images.githubusercontent.com/37858762/236325026-fa2b26a6-cacf-44fe-8019-6ab170ba387b.png)

### Step 17: Again, verify by opening a new putty session for Slave2.

![image](https://user-images.githubusercontent.com/37858762/236325006-5cb7ed57-16ca-4328-bd19-ef1745ac4cd3.png)

### Step 18: Now before moving ahead **install open jdk on both Slave1 and Slave2**.

`sudo apt-get update`

![image](https://user-images.githubusercontent.com/37858762/236324968-316f2fdd-0eeb-4fb4-ab3b-ca2dbd895805.png)

![image](https://user-images.githubusercontent.com/37858762/236324957-a1812bdb-e4f5-4690-99b5-2bd80e43392f.png)

### Step 19: Now install run the following installation command on both terminal.

`sudo apt install openjdk-11-jdk`

![image](https://user-images.githubusercontent.com/37858762/236324904-e16233e9-4141-479b-a50f-f5a73f9b6212.png)

### Step 20: Now we will connect Slave1 and Slave2 to the Jenkins Server. Go to the Jenkins Dashboard, Click on Slave1, **Copy the command line** as shown.

Run the command line from Slave1 as shown below.

![image](https://user-images.githubusercontent.com/37858762/236324887-5baa000b-a6fe-45a6-abc8-02e834ea05de.png)

![image](https://user-images.githubusercontent.com/37858762/236324873-50e47c38-8ec4-440a-935b-b50aa2fabf35.png)

It shows **Connected**.

### Step 21: Perform the **Step-20** for **Slave2** as well.

![image](https://user-images.githubusercontent.com/37858762/236324846-17dc2863-3449-46f5-8526-2b9a25bd810e.png)

Paste the command line in the Slave2 Terminal.

![image](https://user-images.githubusercontent.com/37858762/236324833-932f3697-8855-4add-a173-de9e06bbd08a.png)

_**Important Note: Don't end the Sessions that we just Connected. To perform further operations on Slave1 and Slave2 duplicate the sessions.**_

So now that our Slave1 and Slave2 has been connected to Jenkins Server, it looks like this.

![image](https://user-images.githubusercontent.com/37858762/236324814-3477cb58-01e3-46fc-a39f-728793f1635c.png)

After we have successfully created the Master Slave Cluster on AWS Jenkins. We will now create a CI CD pipeline triggered by Git Webhook.

## Hands-on: Create and Run Jenkins Jobs.

### Step 1: Before that open your GitHub account and import the below given repository.

https://github.com/vistasunil/devopsIQ.git

### Step 2: Install docker on both **Slave1** and **Slave2**.

`sudo apt install docker.io`

![image](https://user-images.githubusercontent.com/37858762/236324780-c8d8bb4b-b1e5-47a3-af22-9cdf33eabaab.png)

![image](https://user-images.githubusercontent.com/37858762/236324765-26156971-40c4-4f99-959d-5a68ac3a3461.png)

### Step 3: Open **Jenkins Dashboard**. **Create a new job** (Freestyle Project) for Slave1.

![image](https://user-images.githubusercontent.com/37858762/236324740-a9ee01ed-6dda-44d0-a776-ae0360e1e5d8.png)

Name the Project as **Demo** , Select **Freestyle Project** option.

![image](https://user-images.githubusercontent.com/37858762/236324717-e562f715-231b-4831-ab82-c58714e25bcd.png)

Then click on **Ok**.

You should land on a page like this.

![image](https://user-images.githubusercontent.com/37858762/236324696-684d928b-6d90-48f1-a724-4ec6a06411dd.png)

### Step 4: Place your git repository link https://github.com/vistasunil/devopsIQ.git as shown below.

![image](https://user-images.githubusercontent.com/37858762/236324671-b155e93c-b41a-4213-9ac6-b11503c7dae5.png)

Click on **Restrict where this project can be run**. Add **Slave1** there.

![image](https://user-images.githubusercontent.com/37858762/236324640-f81a8ba5-40e1-4fa6-9940-cb5316607e27.png)

Go to **Source Code Management** , click on **git** , add the **git repository link** there as well.

![image](https://user-images.githubusercontent.com/37858762/236324620-a6ef9601-cdd3-47b8-aef2-2f9b97e834a1.png)

Click on **Save.**

### Step 5: Click on **Build Now,** if the building is done without any error there will be **blue circle** in the building history.

![image](https://user-images.githubusercontent.com/37858762/236324583-cb3e8174-5376-4bd2-a298-444ef108caf2.png)

Click on the blue circle of build #1.

![image](https://user-images.githubusercontent.com/37858762/236324568-5224fb5b-5768-4ba3-a0dc-a76bdde1918a.png)

You can see it has been built successfully. Let us verify that.

### Step 6: Go to slave1.

```
ls
cd workspace
ls
cd Demo
ls
```

![image](https://user-images.githubusercontent.com/37858762/236324534-ac6fa6a7-e8d1-4b99-a108-4b9405770914.png)

You can see the repository files there. This means the git repository has been successfully cloned into the Demo job.

Now we will deploy the website that we have stored in our repository.

### Step 7: To run the **Dockerfile** we have to check the copy the present working directory.

![image](https://user-images.githubusercontent.com/37858762/236324509-ccaa9a1b-e2f5-4213-892d-acdb1d2b9798.png)

Now go back to configuring the job.

### Step 8: Click on **Build** , then go to **Execute shell**

```
sudo docker rm -f $(sudo docker ps -a -q)
sudo docker build /home/ubuntu/jenkins/workspace/Demo -t devopsdemo
sudo docker run -it -p 82:80 -d devopsdemo
```

![image](https://user-images.githubusercontent.com/37858762/236324483-4963bcdf-4d68-4f10-bf4b-80df710e8811.png)

Click on save.

Before building our job again we must add one arbitrary container in slave1.

### Step 9: Add container by performing the following command.

`sudo docker run -it -d ubuntu`

![image](https://user-images.githubusercontent.com/37858762/236324422-6c2c0cd2-5f67-411e-9748-fb89b175da11.png)

Now we have added in a container.

![image](https://user-images.githubusercontent.com/37858762/236324407-d18628b0-f362-4c31-ae6a-ae3c432123b1.png)

### Step 10: Now open Jenkins Dashboard and **build the project**.

![image](https://user-images.githubusercontent.com/37858762/236324364-b3cd6316-5e5d-4216-9b4e-20841b3cc70c.png)

Build was successful.

### Step 11: Now open browser and enter **Slave1 IP:82**

![image](https://user-images.githubusercontent.com/37858762/236324343-8bc34b8d-66f9-4a2f-8af7-5f6fb252106f.png)

This is the apache page that means our container is working perfectly.

### Step 12: Now enter **slave1 IP:82/devopsIQ/** in the browser.

![image](https://user-images.githubusercontent.com/37858762/236324319-38fca951-dae6-43fb-b501-addc2bac7524.png)

Now, we will create a new project.

### Step 13: Create a new project.

![image](https://user-images.githubusercontent.com/37858762/236324297-f677d186-fc91-4cee-9b1f-4d9d98978b39.png)

### Step 14: Click on git project.Enter the git hub repository URL.

![image](https://user-images.githubusercontent.com/37858762/236324273-9b160723-724e-4630-af20-fcdea082fd96.png)

### Step 15: Click on **Restrict where this project can be run** enter **Slave2.**

![image](https://user-images.githubusercontent.com/37858762/236324250-06049133-1493-4cd9-9bec-9c172dbe3131.png)

### Step 16: Go to Source code management enter the git repository URL there as well.

![image](https://user-images.githubusercontent.com/37858762/236324226-26797bd5-afbd-4263-bdaa-7eec2e21eb8a.png)

### Step 17: Now enter the following command in the **Execution shell**

```
sudo docker rm -f $(sudo docker ps -a -q)
sudo docker build /home/ubuntu/jenkins/workspace/Demoprod -t devopsprod
sudo docker run -it -p 82:80 -d devopsprod
```

![image](https://user-images.githubusercontent.com/37858762/236324187-928d8dd1-9ec5-4201-ab64-6b25bca85065.png)

### Step 18: Again, add one container to the Slave2 as shown below.

`sudo docker run -it -d ubuntu`

![image](https://user-images.githubusercontent.com/37858762/236324162-5e5a9eb1-8e96-40bb-bafd-66e58faa3c83.png)

Now that we have added an arbitrary container, go to Jenkins Dashboard and build the project.

### Step 19: Build the project **Demoprod**.

![image](https://user-images.githubusercontent.com/37858762/236324135-a23c2d78-3f12-4748-8d9b-3095afe8a787.png)

Our Project building was successful.

### Step 20: Now go to the browser and enter **Slave2 IP:82/devopsIQ/**

![image](https://user-images.githubusercontent.com/37858762/236324109-63879c7c-d80d-41d6-bd69-21765619845e.png)

Now trigger **Demoprod** job only when **Demo** job will be completed.

### Step 21: Go to the **Demo** job, click on **Configure**. Add **Post-Build Actions**. Then go to **Build Other Projects.**

![image](https://user-images.githubusercontent.com/37858762/236324080-b14f45b2-fb60-4c2d-ac94-be3f87923bca.png)

Click on Save.

## Hands-on: Create a CI CD pipeline triggered by Git Webhook.

### Step 22: Go to the manage Jenkins and then Manage Plugins, click on available, search for Build Pipeline. Click on install without restart.

![image](https://user-images.githubusercontent.com/37858762/236324035-8584954b-1790-45d9-928c-efba8d9f1905.png)

### Step 23: Go to the jenkins dashboard. Click on the +.

![image](https://user-images.githubusercontent.com/37858762/236324010-b1d496fe-cade-4aa4-b93c-4bf9b8ad7751.png)

### Step 24: Enter view name and click ok. ![]

![image](https://user-images.githubusercontent.com/37858762/236323991-e41635ab-fbec-433a-a8be-76cb04e2ab01.png)

### Step 25: There add the Build Pipeline View Title, then Select initial job as Demo.

![image](https://user-images.githubusercontent.com/37858762/236323962-3f98eb33-91b8-4870-a049-05bea46a5d8f.png)

Click on ok. You should see the Pipeline Page like this.

![image](https://user-images.githubusercontent.com/37858762/236323916-65c7a118-cb5b-45c4-ac06-f377e4c761ce.png)

### Step 26: Click on Run. Then Refresh the Page once.

![image](https://user-images.githubusercontent.com/37858762/236323910-521b20f2-afc6-4477-919f-145be2d1e7bf.png)

![image](https://user-images.githubusercontent.com/37858762/236323894-3a029c8b-709f-4912-bffa-46c16774f605.png)

![image](https://user-images.githubusercontent.com/37858762/236323882-7c31a0d4-77e6-461c-ba49-56f5f19557b1.png)

**Now we will commit on GitHub, which should trigger our Jenkins Job.**

### Step 27: Go to the Jenkins Dashboard. Click on Demo and then Configure. Check the _**GitHub hook trigger for GITScm polling**_ option.

![image](https://user-images.githubusercontent.com/37858762/236323727-c19a0ba9-dfee-4d5f-9a61-63190a0c93a9.png)

### Step 28: Now configure GitHub Webhook. Go to settings, then click on Webhooks, then add webhooks. There insert the Jenkins Server Address as shown.

***http://Jenkins-Server-Address/github-webhook/***

![image](https://user-images.githubusercontent.com/37858762/236323688-ecc093c3-98b7-4705-a6f6-294e4ae871a4.png)

![image](https://user-images.githubusercontent.com/37858762/236323674-f34bc70a-a9fe-4694-ae32-96438bba68f7.png)

Click on Add webhook. You should see this. 

![image](https://user-images.githubusercontent.com/37858762/236323651-c17a63bb-975e-437a-b53c-3453c43a4b68.png)

### Step 29: Go to the mater terminal to trigger a built.

`git clone <git repository URL>`

![image](https://user-images.githubusercontent.com/37858762/236323618-541adb6a-c729-40b8-a344-8369a10863e2.png)

### Step 30: Now we will try to modify the website from the master terminal. Go to the master terminal and then go to the devopsIQ directory where you can find index.html file. Open it for modification

`vim index.html`

![image](https://user-images.githubusercontent.com/37858762/236323590-26e53022-c543-4e91-b2e7-f5e09716e935.png)

### Step 31: Make the modification in the **title** and **body** of that html file as shown below.

![image](https://user-images.githubusercontent.com/37858762/236323564-57f30283-76d6-40ae-9f5c-a858e1294c26.png)

```
git add
git commit -m "new commit"
```

![image](https://user-images.githubusercontent.com/37858762/236323489-92251181-d531-42bc-9aea-7a92936308e1.png)

### Step 33: Perform git push.

`git push origin master`

![image](https://user-images.githubusercontent.com/37858762/236323442-910cf213-e6d3-4622-98f9-6ef6c35e9484.png)

### Step 34: Go to the browser. Refresh it. And you can see the background image got changed.

![image](https://user-images.githubusercontent.com/37858762/236323418-92b9fff3-e3d7-4930-931f-9acef95053f5.png)

**Congratulations!** You have successfully completed the hands on.
