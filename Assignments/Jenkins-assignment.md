<div align="center">
<img src=https://static.wixstatic.com/media/1c706c_a5df0ad56f894928bf858a74ba744b32~mv2.png/v1/fit/w_2500,h_1330,al_c/1c706c_a5df0ad56f894928bf858a74ba744b32~mv2.png width="400" height="200">
 </div>

# <div align="center"> JENKINS ASSIGNMENT </p>

# <div align="center"> DevOps Instructor-led Training </div>

<br />

<br />

<br />

<br />

# $${\color{brown} &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; Contact&emsp;us: &emsp;&emsp;&emsp; }$$

<div align="right"> T O A C C E L E R A T E Y O U R C A R E E R G R O W T H </div>

### <div align="right"> For questions and more details: </div>

<div align="right"> <img src=https://w7.pngwing.com/pngs/759/922/png-transparent-telephone-logo-iphone-telephone-call-smartphone-phone-electronics-text-trademark-thumbnail.png width="20" height="20"> +91 98712 72900 </div>

<div align="right"> <img src=https://pbs.twimg.com/profile_images/1450734615946219520/jmBHQRRa_400x400.jpg width="20" height="20"> https://www.thecloudtrain.com </div>

<div align="right"> <img src=https://icons.iconarchive.com/icons/martz90/circle/512/email-icon.png width="20" height="20"> support@thecloudtrain.com </div>

<div align="right"> <img src=https://png.pngtree.com/png-vector/20221018/ourmid/pngtree-whatsapp-icon-png-image_6315990.png width="20" height="20"> +91 98712 72900 </div>

## Exercise 1: Jenkins Freestyle Job

### Complete below tasks as part of this exercise:

1. Create a Jenkins job **Demo** to clone repo https://github.com/vistasunil/devopsIQ.git and deploy the website inside it the slave1 instance in container.
2. Observe the console output of this job to understand the stages output during execution.
3. Create another job **Demoprod" to clone repo https://github.com/vistasunil/devopsIQ.git and deploy the website inside it the slave2 instance in container.
4. Configure and update the Demo job to trigger Demoprod internally, only if the Demo build is stable
5. Create a Jenkins pipeline view using **Build Pipeline** plugin and to trigger and view Demo and Demoprod job
6. Create another job **Cleanup** to delete workspace of Demo job and trigger internally, only if Demo job fails.

## Exercise 2: Jenkins Pipeline for CI/CD

### Complete below tasks as part of this exercise:

1. Install Ansible on one of the Slave node (Ansible Master) of Jenkins and connect your deployment machine as slave to this Ansible master
2. Create a Jenkins pipeline that should execute below tasks in stages (Refer Jenkinsfile in devopsIQ repo):
  1. Check git repo https://github.com/vistasunil/devopsIQ.git
  2. Build the docker image with tag \<dockerhub\_account\>/devopsdemo using Dockerfile inside the repo synced
  3. Push this docker file to your dockerhub account. Make sure you have logged in to the dockerhub account before pushing the image
  4. Configure the target machines(Ansible Slaves) for Docker using Ansible and run 3 containers of devopsIQ website. (Refer docker.yaml in above git repo for the playbook.
3. Make sure this pipeline runs on Ansible installed Slave only.
4. Run the pipeline to Build and deploy the website code present in devopsIQ repo
5. Test the website deployed correctly

## Exercise 3: Jenkins Pipeline for Continuous Testing and Deployment

### Complete below tasks as part of this exercise:

1. Install a local Jenkins on Windows server or laptop
2. Create a Jenkins pipeline that should execute below tasks in stages (Refer Jenkinsfile_sel in devopsIQ repo)::
  1. Checkout git repo https://github.com/vistasunil/devopsIQ.git
  2. Build the docker image using Dockerfile inside the repo synced
  3. Remove existing containers for devopsiq website
  4. Deploy the website using one container with name devopsiq website.
  5. Checkout Selenium code repo https://github.com/vistasunil/selenium.git
  6. Test the website is running and title is **Jenkins Webhook Website**

_**Note: Refer code testing.java to test the webpage title.**_
