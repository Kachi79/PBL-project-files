PROJECT 3: MERN STACK IMPLEMENTATION:
This project requires that i implement a web solution, MERN STACK on the AWS cloud. The components for the implementation of this project are:
MongoDB: A document-based, No-SQL database used to store application data in a form of documents.
ExpressJS: A server side Web Application framework for Node.js.
ReactJS: A frontend framework developed by Facebook. It is based on JavaScript, used to build User Interface (UI) components.
Node.js: A JavaScript runtime environment. It is used to run JavaScript on a machine rather than in a browser.

STEP 1 – BACKEND CONFIGURATION
The first task is to update the ubuntu OS as an administrator using the "apt" package manager with this command: sudo apt update, next is to upgrade it
with is command: sudo apt upgrade.

<img width="962" alt="sudo apt update p3" src="https://user-images.githubusercontent.com/105996656/170847886-a446a823-72d7-46ad-afcb-aa98868bbe9b.png">

nodejs was also install with its corresponding package manger with the command: sudo apt-get install -y nodejs 

<img width="793" alt="install node js on server  p3" src="https://user-images.githubusercontent.com/105996656/170847954-74ad5746-0384-4077-8186-e4e794b8417f.png">

A new Todo directory was created with the command : mkdir Todo.

A new file was created for dependencies, application information with the command: npm init

<img width="1089" alt="creating  json file" src="https://user-images.githubusercontent.com/105996656/170848032-a33e5740-dfc5-4a6d-97ad-a396f5f2b4e7.png">

INSTALL EXPRESSJS
 Express is a framework for Node.js, therefore a lot of things developers would have programmed is already taken care of out of the box, 
 express was installed using the npm package manager with the command : npm install express.
 
<img width="845" alt="installing express js p3" src="https://user-images.githubusercontent.com/105996656/170848136-da1d716d-19d0-411c-8eae-9d309e0e703b.png">

The index.js file was created using : touch index.js:  

dotenv module was created using the command: npm install dotenv.

index.js file edited and saved using vim index.js. 

<img width="1354" alt="index js file edited   saved" src="https://user-images.githubusercontent.com/105996656/170848444-4805cc86-1bd7-46d9-821f-098a5c36bd2c.png">

server was fully operational on port 5000

<img width="648" alt="port 5000 up   running p3" src="https://user-images.githubusercontent.com/105996656/170848518-3839786f-0a3b-4d8f-9aa2-62573bf2ce2f.png">

My browser was opened to access the server’s Public IP or Public DNS name followed by port 5000:

http://<PublicIP-or-PublicDNS>:5000: <img width="1792" alt="port 5000 opened in web browser p3" src="https://user-images.githubusercontent.com/105996656/170848619-c7e759e8-d1d6-4094-8fbe-f7e3ba7c0597.png">

To achieve the end goal, a new directory was created with the command :mkdir routes
  api file was created with the command: touch api.js and edited with : vim api.js
  
  MODELS
  Since the app is going to make use of Mongodb which is a NoSQL database, we need to create a model.
  
  I installed mongoose with the command : npm install mongoose. I changed directory into the models directory to create a file using the command: touch todo.js
  
  todo.js was edited with the command : vim todo.js
  
  MONGODB DATABASE
  
  I created a MongoDb account and configured it to suit the aim of the project: <img width="1792" alt="mongodb data creation  p3" src="https://user-images.githubusercontent.com/105996656/170849000-2fc822c8-3ee5-4d67-a4a9-3fb967891612.png">

  MongoDb was configured to allow access from anywhere.
  
  I created and edited a new file in the Todo directory using the command :touch .env
  vi .env. 
  
  I used the connection string of the MongoDb to access it's database:DB = 'mongodb+srv://<username>:<password>@<network-address>/<dbname>?retryWrites=true&w=majority'
  
  I also tested the backend connection using postman: 
  
  <img width="1792" alt="postman configuration  p3" src="https://user-images.githubusercontent.com/105996656/170849279-37f8392f-07bb-49c0-a050-68c05249186f.png">

<img width="1792" alt="postman:GET creation 3" src="https://user-images.githubusercontent.com/105996656/170849296-a16b67bd-83ce-449b-a27f-f7563f6ba942.png">

  
 
  
  
  

