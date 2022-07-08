PROJECT 9 :TOOLING WEBSITE DEPLOYMENT AUTOMATION WITH CONTINUOUS INTEGRATION AND INTRODUCTION TO JENKINS.

The task is to enhance the architecture prepared in Project 8 by adding a Jenkins server, configure a job to automatically deploy source codes 
changes from Git to NFS server.

The first thing i did was to update and install jenkins package managers after which i installed jenkins.
<img width="1207" alt="jenkins update" src="https://user-images.githubusercontent.com/105996656/178069815-a3363d44-9661-4120-b179-de26a9c2ef33.png">
<img width="1772" alt="jenkins update 2" src="https://user-images.githubusercontent.com/105996656/178069820-bf99b52d-0571-43ea-9dbb-3e96474b5f05.png">
I restarted the jenkins server to ensure that it is running:
<img width="1789" alt="Screenshot 2022-07-08 at 22 08 24" src="https://user-images.githubusercontent.com/105996656/178070649-9a61fed5-aa23-4269-973f-9bc6c1923c8f.png">

 I opened port 8080 to ensure that connections routed through this port gained access. I securely set up jenkins and customised it.
 I went on to configure jenkins to retrieve source codes from GitHub using Webhooks.
 
I made some changes in the READ.me file in my github repository and configured my Jenkins freestyle project choosing, providing the link
to my Tooling GitHub repository and credentials (user/password) so Jenkins could access files in the repository.
<img width="1792" alt="first build" src="https://user-images.githubusercontent.com/105996656/178074326-d5cc6f45-0310-456d-903d-f67db98f01ee.png">

After that i configured my Post-build Actions to archive all the files, files resulted from a build are usualy called artifacts.
<img width="1792" alt="post build actions" src="https://user-images.githubusercontent.com/105996656/178074802-5fc85bb8-be7c-478f-ac1f-ebee26f30301.png">

I made some changes in my GitHub repository file (e.g. README.MD file) and pushed the changes to the master branch.
<img width="1792" alt="new build" src="https://user-images.githubusercontent.com/105996656/178075204-4348bd51-d5f0-4784-b65f-7f8732e26c73.png">

I went on to configure Jenkins to copy files to NFS server via SSH:
<img width="1792" alt="ssh key config" src="https://user-images.githubusercontent.com/105996656/178075440-7247db59-ac06-4722-8dbe-2d52e3b8d245.png">

Finally i used the command "cat /mnt/apps/README.md" to ensure that the files in /mnt/apps have been udated and can connect via 
SSH/Putty to your my server and check README.MD file :

<img width="1792" alt="final" src="https://user-images.githubusercontent.com/105996656/178075960-461194be-fc93-4b9d-85e1-79f3e5da26a7.png">

From my terminal i could see the changes i had previously made on gihub.                        






