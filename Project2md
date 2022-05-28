LEMP STACK IMPLEMENTATION

This is a set of frameworks and tools are very specifically chosen to work together in creating a well-functioning software. 
The individual technologies involved in the web stack implementation called LEMP are (Linux, Nginx, MySQL, PHP or Python, or Perl)
The process in similar to that of project 1, we get the web server NGINX also running on AWS. The requirements are a free tier version of AWS account . A LINUX Terminal . A basic knowledge of Linux, AWS, EC2, Web Technology stack and VIM editor.

STEP 1 – INSTALLING THE NGINX WEB SERVER
The first step is to update the server's package index with the "apt" package manager using sudo to give us administrative access into the server, after this the server is installed using the same package manager and sudo for unrestricted access.

c<img width="1026" alt="Installed Nginix p2" src="https://user-images.githubusercontent.com/105996656/170803062-ad8a3dc7-c23c-4201-b5b9-d96c72ce11bb.png">

To verify that nginx was successfully installed and is running as a service in ubuntu, run : sudo systemctl status nginx 

<img width="1504" alt="Nginx Active   running" src="https://user-images.githubusercontent.com/105996656/170803174-c04d4bb0-5097-49ad-a7d9-bccbba910a2c.png">

Before we can receive any traffic by our Web Server, we need to edit the inbound rules in the Aws console and open the inbound connection through TCP port 80 which is default port that web brousers use to access web pages in the Internet.

<img width="1792" alt="Port 80 added p2" src="https://user-images.githubusercontent.com/105996656/170803352-1a0e746e-46f7-47f0-b955-75f1cd20c723.png">

using the Ip address we can check the webpage on a browser.

<img width="663" alt="Welcome to NGINX (P2)" src="https://user-images.githubusercontent.com/105996656/170803462-f188dbaf-efc9-46ab-a002-d82d3c6f9938.png">

STEP 2 — INSTALLING MYSQL
Again, use ‘apt’ to acquire and install this software:  sudo apt install mysql-server
Now that the server is active, we need to install a DBMS, to enable us store and data on the site in a relational database, MYSQL is works well with php
enviroments, so it is the suitable choice.

STEP 3 – INSTALLING PHP

Now PHP needs to be installed to process code and generate dynamic content for the web server by running this : sudo apt install php-fpm php-mysql
This command contains a PHP module that allows PHP to communicate with MySQL-based databases. Core PHP packages will automatically be installed as dependencies.

<img width="1672" alt="installing php   mysql p2" src="https://user-images.githubusercontent.com/105996656/170804058-bad6db80-6830-4df2-a069-2ae52c17c090.png">

STEP 4 — CONFIGURING NGINX TO USE PHP PROCESSOR

Create the root web directory for your_domain using this command: sudo mkdir /var/www/projectLEMP
After that the ownership of the directory will be changed using this command : sudo chown -R $USER:$USER /var/www/projectLEMP

A nano configuration file will be opened and edited using the command: sudo nano /etc/nginx/sites-available/projectLEMP
After the configuration, a simple test is performed to check for syntax errors.

<img width="919" alt="Syntax is Ok p2" src="https://user-images.githubusercontent.com/105996656/170805042-3c3d1f2f-88be-4f35-b29f-8cddacf65333.png">

Nginx host is then disabled
To test that the configuration is complete open the IP address with port 80: to see the host name: 

<img width="754" alt="website on web browser (P2)" src="https://user-images.githubusercontent.com/105996656/170805295-5fe23227-10a4-4e4b-99c7-aff5bdc2747e.png">

STEP 5 – TESTING PHP WITH NGINX

The command : sudo nano /var/www/projectLEMP/info.php is used to edit the file 

You will see a web page containing detailed information about your server:

<img width="1792" alt="php working correctly  p2" src="https://user-images.githubusercontent.com/105996656/170805426-1670927d-d35f-4dd8-9227-48e170f2dd20.png">

STEP 6 – RETRIEVING DATA FROM MYSQL DATABASE WITH PHP (CONTINUED)

Here commands are used to create and edit mysql database to suit the purpose, and when  http://<Public_domain_or_IP>/todo_list.php is pasted on the 
web browser we get this: 

<img width="274" alt="accessing page on web browser (P2)" src="https://user-images.githubusercontent.com/105996656/170805576-fbaaeb30-5ba9-4d5a-adf6-a09b419f5daa.png">


   BLOCKERS AND HOW THEY WERE RESOLVED:

<img width="1792" alt="Error php not logging  p2" src="https://user-images.githubusercontent.com/105996656/170805693-b26a9134-7c42-4870-bb24-8d4962c1f60d.png">

This errors came up in step 5 because the version of the php files needed to be modified, and i figured it out and did it below.


<img width="863" alt="Php software version modified" src="https://user-images.githubusercontent.com/105996656/170805736-c98911e6-2af7-49e3-9ac4-227dc0f6ca05.png">



