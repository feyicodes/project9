## TOOLING WEBSITE DEPLOYMENT AUTOMATION WITH CONTINUOUS INTEGRATION. INTRODUCTION TO JENKINS

This project aims to enhance the architecture prepared in Project 8 by adding a Jenkins server, configure a job to automatically deploy source codes changes from Git to NFS server. 

![image 1](images/img0.png)


I created an AWS EC2 instance based on Ubuntu Server 20.04 and named it **Jenkins** and I opened up the TCP port 8080 by creating a new inbound rule in the EC2 security group on the server.

![image 2](images/img2.png)

I installed JDK and Jenkins and confirmed Jenkins is up and running.

![image 3](images/img3.png)

![image 4](images/img4.png)

I configured jenkins via the web browser.

![image 5](images/img5.png)

![image 6](images/img6.png)

![image 7](images/img7.jpeg)

I enabled webhook in my Github repository settings.

![image 8](images/img8.jpeg)

I clicked on new item and created a freestlye project on jenkins. Afterwards I connected my github repository and inputted the url. 

![image](images/img10.png)

I tested it and it reflected.

![image](images/img11.jpeg)


I  configured the process of triggering the job from github webhook.

![image](images/img12.png)

![image](images/img13.png)

I saw that the new build has been launched automatically by webhook and the results- artefact has been saved on jenkins server.

![image](images/imgv.jpeg)

After configuring the build, I clicked build now

I made changes in the readme.md file in the Github repository and pushed the changes into the master branch and the build was automatically launched and the result artifacts saved on jenkins server.

![image](images/imgv.jpeg)

I connected to my NFS server and and checked readme.md file to check if the /mnt/apps has been updated.

![image](images/imgw.jpeg)

While this is the equivalent output of the readme.md on github. 

![image](images/imgz.jpeg)

The new information I added to the read,e file is "Should be there on /mnt/apps".




















