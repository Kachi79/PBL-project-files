DEVOPS TOOLING WEBSITE SOLUTION

In the previous project i implemented a wordpress based solution, Project 7 was a continuation of that.
Moving further i added some more value to our solutions that a DevOps team could utilize. I was introduced to a set of DevOps tools that will help 
the team in the  day to day activities in managing, developing, testing, deploying and monitoring different projects. The Tooling solution consist of Jenkins,
kubernetes, Rancher, Grafana just mention a few. I was required to spin 3 webservers and 1 nfs server in redhat and 1 database server in ubuntu.

The task was to implement a tooling website solution which makes access to DevOps tools within the corporate infrastructure easily accessible.

I repeated the basic early steps for project 6 which was centered on disk partitioning and creating mount points for the logical volumes.
<img width="980" alt="configuring the partitions  p7" src="https://user-images.githubusercontent.com/105996656/177424369-61ce239f-f0be-46ef-963e-da7f37bc2258.png">
<img width="1792" alt="configuring the partitions 2  p7" src="https://user-images.githubusercontent.com/105996656/177424371-3b8f8eb5-9e69-4802-a8bf-28b8c3a1b372.png">

I installed and configured the NFS server to start running.
<img width="1174" alt="install p7" src="https://user-images.githubusercontent.com/105996656/177425012-372bb8df-50b5-465f-8a28-571e94c8cdd9.png">

I Configured access to NFS for clients within the same subnet using the command: sudo vi /etc/exports, after that i exported apps, logs & mount.
<img width="629" alt="exporting apps, logs and opt  p7" src="https://user-images.githubusercontent.com/105996656/177425811-a0fa70ec-2288-4167-9878-81d4cf005d7d.png">
In order for NFS server to be accessible from your client, you must also open following ports: TCP 111, UDP 111, UDP 2049

In order for NFS server to be accessible from the client, i was tasked to open the following ports: TCP 111, UDP 111, UDP 2049
<img width="1792" alt="Screenshot 2022-07-05 at 02 43 00" src="https://user-images.githubusercontent.com/105996656/177426037-f41d8779-0aea-440d-8175-fcaa07fb0e6f.png">

The next thing i did was to install and configure mysql on the database server.
<img width="1792" alt="mysql installation on db server  p7" src="https://user-images.githubusercontent.com/105996656/177426436-fb4041a8-21c7-48f3-b68e-a326afa225b0.png">
<img width="1214" alt="mysql config 2   p7" src="https://user-images.githubusercontent.com/105996656/177426613-e9c5b34d-b4b4-435d-aebe-5f425968692e.png">

I went on to configure the webservers
<img width="1792" alt="mysql configuration on db server p7" src="https://user-images.githubusercontent.com/105996656/177427601-4f62d2f0-0f25-4658-bea3-023d501b5557.png">
<img width="1214" alt="mysql config 2   p7" src="https://user-images.githubusercontent.com/105996656/177427607-3a48c67f-2900-4faf-af1a-706a2e7fb1a1.png">
I configured nfs client on all 3 webservers using the command: "sudo yum install nfs-utils nfs4-acl-tools -y".

I mounted /mnt/apps directory in the nfs server in the /var/www in the webserver, to enable the webserver have access to the nfs server and vice versa.
<img width="685" alt=":var:www file in webserevr p7" src="https://user-images.githubusercontent.com/105996656/177428695-20ffc80f-897d-44b3-b32b-8e9c52ed606a.png">

I installed Apache on the webserver.
<img width="1789" alt="Installing apache on webserver p7" src="https://user-images.githubusercontent.com/105996656/177428791-86dd463e-3f7a-47fc-aefc-5ddf307b36f7.png">

I cloned git initialised it.
<img width="976" alt="git cloning p7" src="https://user-images.githubusercontent.com/105996656/177428981-e9b3e622-858e-46b5-83ff-41e12b3207fa.png">
<img width="1111" alt="initialising git p7" src="https://user-images.githubusercontent.com/105996656/177428986-b7a4dffc-b658-4cff-b7e6-2734a6b100ec.png">

I update the website’s configuration file to connect to the database: var/www/html/functions.php

i substituted the correct credentials and opened the website in my browser. http://<Web-Server-Public-IP-Address-or-Public-DNS-Name>/index.php
  <img width="1792" alt="webpage successfully loaded p7" src="https://user-images.githubusercontent.com/105996656/177429497-20caa700-b65e-4fc0-ad1c-4db0c9a9fb45.png">


 

