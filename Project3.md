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

The index.js file was created using : touch index.js  

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

 STEP 2 – FRONTEND CREATION
 Firstly, in the todo directory, the same directory where i ran the backend code i ran : npx create-react-app client, after which i ran concurrently with
 this command: pm install concurrently --save-dev.  nodemon was installed to monitor the server with this command :  npm install nodemon --save-dev.
 
 In the Todo folder, i opened and modified the package.json file, also in the client folder, i added the proxy configuration : "proxy": "http://localhost:5000". 
 
 <img width="1792" alt="frnt end creatn, key value pair  p3" src="https://user-images.githubusercontent.com/105996656/170870712-8d38236f-166a-4d07-98de-2488e24d001a.png">

 The the reactjs App started running at  localhost:3000 after i added port 3000 to my AWS console: 
 <img width="1792" alt="react js app running at port 300" src="https://user-images.githubusercontent.com/105996656/170870944-a9e98b90-ad00-488d-8299-81f98c307148.png">

 Inside ‘components’ directory i created three files Input.js, ListTodo.js and Todo.js. using this command : touch Input.js ListTodo.js Todo.js,
 after that i opened the input.js file to edit it using : vi Input.js.
 
 After editing i moved to the client folder to install axios using : npm install axios
 
 FRONTEND CREATION (CONTINUED)
 Here i moved to the components directory to open the  ListTodo.js file using : vim  ListTodo.js., upon opening the file i pasted the given code; 

 <img width="1348" alt="list Todo js file p3" src="https://user-images.githubusercontent.com/105996656/170871727-81c6772d-5633-4bcb-94f0-5960e9ab074d.png">.
 
 Next i moved the src folder where i opened the App.js file and pasted the given code in it: 
 <img width="1174" alt="api  js file edited p3" src="https://user-images.githubusercontent.com/105996656/170871997-af58081d-3261-422e-80b6-f98f18770cb3.png">

After pasting, i exited the editor in the src directory and opened the App.css file with : vi App.css and pasted the code:

 <img width="1792" alt="Edited App css file  p3" src="https://user-images.githubusercontent.com/105996656/170872167-9a15eb63-7075-4a19-ba01-4d1973cdf33a.png">

 I open the index.css file in the src directory and pasted the given code using  vim index.css.
 
 I changed to the Todo directory to run the command : npm run dev, that showed the Todo app.


 
 

  
 
  
  
  

