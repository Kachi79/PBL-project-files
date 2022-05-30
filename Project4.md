Project 4 MEAN STACK DEPLOYMENT TO UBUNTU IN AWS.
This Project requires the implementation of a simple Book Register web form using MEAN stack.
The components of the MEAN stack are:

MongoDB (Document database) – Stores and allows to retrieve data.
Express (Back-end application framework) – Makes requests to Database for Reads and Writes.
Angular (Front-end application framework) – Handles Client and Server Requests
Node.js (JavaScript runtime environment) – Accepts requests and displays results to end user

Step 1: Install NodeJs:
sudo apt update was introduced:  <img width="1792" alt="sudo apt update  p4" src="https://user-images.githubusercontent.com/105996656/170894624-c55808cb-ee5e-498f-a388-240a43b1b394.png">
After which the NodeJs was upgraded with the command: sudo apt upgrade.

I added certificates with the command: sudo apt -y install curl dirmngr apt-transport-https lsb-release ca-certificates and 
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash - :
<img width="1626" alt="certificates p4" src="https://user-images.githubusercontent.com/105996656/170895150-89e5d561-e5e9-425a-a8a4-458729c028d7.png">

I Installed NodeJS: <img width="1534" alt="install node js  p4" src="https://user-images.githubusercontent.com/105996656/170895209-861651a5-cb31-47cc-9d87-2b5ded461508.png">

Step 2: Install MongoDB: <img width="1789" alt="install mondodb p4" src="https://user-images.githubusercontent.com/105996656/170895298-9d00e8ae-ce6a-4981-a0af-7ea8e4a9fbb8.png">
i installed mongodb with command: sudo apt install -y mongodb : <img width="1792" alt="install second mongodb  p4" src="https://user-images.githubusercontent.com/105996656/170895375-07d70a63-0eb9-42b4-b77d-5dd351bd1ce6.png">

Start The server: I started the server with the command: 
<img width="899" alt="start mongodb p4" src="https://user-images.githubusercontent.com/105996656/170895428-732643ab-f7e7-494e-adae-57ba043f7af5.png">
After which i verified the server with the command: sudo systemctl status mongodb 
<img width="1316" alt="verify mongodb server  p4" src="https://user-images.githubusercontent.com/105996656/170895521-d409bab1-f3da-4310-b118-f7470f1d9101.png">

I installed the Node package manager with the command : sudo apt install -y npm : 

<img width="753" alt="sudo apt install -y npm p4" src="https://user-images.githubusercontent.com/105996656/170895652-c87aac77-7b0a-4691-9204-a7a2d8f1a278.png">

I created a folder named ‘Books’ and entered it with the command : mkdir Books && cd Books
While in the books directory, Initialized npm project with command: npm init
 
 I added a file named server.js and pasted the code into it : <img width="1792" alt="server js p4" src="https://user-images.githubusercontent.com/105996656/170895897-37831808-07b7-4984-8e96-546e6bd5638a.png">

INSTALL EXPRESS AND SET UP ROUTES TO THE SERVER

 I installed express alongside mongoose package manager using :sudo npm install express mongoose.
 <img width="1192" alt="install express mongoose p4" src="https://user-images.githubusercontent.com/105996656/170896184-d8e66e18-42b6-4f44-84d2-ecdfdf8f31b9.png">

  I moved to the Books folder and created a folder called apps using : mkdir apps && cd apps
  
  I created a file named routes.js and modified it with this command : 
  <img width="1792" alt="vi routes js p4" src="https://user-images.githubusercontent.com/105996656/170896252-9c9da096-0cfd-4a6b-b345-592298f88629.png">
  
  In the ‘apps’ folder, i created another folder named models, in this folder i created a file named book.js and modified the file with vi book.js
  <img width="1792" alt="vi book js p4" src="https://user-images.githubusercontent.com/105996656/170896446-b109bcd9-9a6c-4035-b83f-5e09c0932a97.png">

Step 4 – Access the routes with AngularJS

Here i created and moved into a folder named public with the command : mkdir public && cd public
i created an empty file named script.js and i pasted the given code into it: 

<img width="1792" alt="vi script js p4" src="https://user-images.githubusercontent.com/105996656/170896627-e432041b-d92f-4d62-b2b5-aded49e221dd.png">

In the public folder i created an empty file named index.html which i opened and pasted the given code into it :

<img width="1792" alt="vi index html p4" src="https://user-images.githubusercontent.com/105996656/170896753-56b17155-82d6-4cc6-92b0-929315d5b3bb.png">
I changed to the Books directory and i started the server by running the command : node server.js
<img width="839" alt="node js p4" src="https://user-images.githubusercontent.com/105996656/170896950-379c49f5-c8a9-474b-8817-03ae6b73c913.png">

At this point the server was up and running at port 3300, 

I went into my AWS web console to open TCP port 3300 for my EC2 Instance.

I extracted my ip address and added :3000 to it and pasted it in a web browser :

<img width="1792" alt="web boog reg  in browser p4" src="https://user-images.githubusercontent.com/105996656/170897035-56cf2591-4e6d-4d3a-af45-47426b3695f9.png">




