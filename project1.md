# WEB STACK IMPLEMENTATION (LAMP STACK) IN AWS
This is my implementation process on i created a technology stack called LAMP((Linux, Apache, MySQL,PHP)

Requirements:

. A free tier version of AWS account
. A LINUX Terminal
. A basic knowledge of Linux, AWS, EC2, Web Technology stack and VIM editor.

The first task to perform before the core Steps include:

  .Launching an EC2 instance in the AWS account 
  
  <img width="1784" alt="EC2 instance Running (P1)" src="https://user-images.githubusercontent.com/105996656/169698192-0ac209a5-a05d-473f-85e2-b4aff56b0678.png">
  
  .SSH into your instance via your linux Terminal - you first have to change permissions for the private key using the command: sudo chmod 0400 <private-key-name>.pem, then you connect to the instance by running: ssh -i <private-key-name>.pem ubuntu@<Public-IP-address>
  
  STEP 1-INSTALLING APACHE AND UPDATING THE FIREWALL: 
  update a list of packages in package manager using: sudo apt update
  
  run apache2 package installation using: sudo apt install apache2
  
  To verify that apache2 is running as a Service in our OS, use following command: sudo systemctl status apache2
  
  <img width="1312" alt="Apache server installed (P1)" src="https://user-images.githubusercontent.com/105996656/169699505-65a00bd2-184d-425e-a950-66130168960b.png">

  Next, you need to add a new rule to EC2 configuration to open the inbound connection through port 80.
  
  <img width="1703" alt="Editing the inbound rules for port 80" src="https://user-images.githubusercontent.com/105996656/169700135-bd619e58-e718-47c4-a65a-ffbfc4b265b7.png">

  Our server is up and running and we can access it locally in our ubuntu shell by running :  curl http://localhost:80
or
 curl http://127.0.0.1:80
  
  Another way to test is running : http://<Public-IP-Address>:80 or http://<Public-IP-Address> on the browser and you will see this:
 
  <img width="1792" alt="webserver correctly installed (P1)" src="https://user-images.githubusercontent.com/105996656/169700814-7f2be4cc-feb2-4f57-ae57-a27bbffe2b29.png">
  
STEP 2:- INSTALLING MYSQL
  Use this command to run MYSQL INSTALLATION: sudo apt install mysql-server
  
  Upon running the command, you'd get a couple of prompts, patiently follow through.
  When the installation is finished, log in to the MySQL conole and test if everything is working ok by using this command: sudo msql
  
  This will connect to the MySQL server as the administrative database user root, which is inferred by the use of sudo when running this command. 
  
  STEP 3 - INSTALLING PHP
  Run this command to install the 3 Required Packages at one go: sudo apt install php libapache2-mod-php php-mysql
  
  To test what you have installed, Run: php -v
  
  <img width="937" alt="Step 3 installing PHP (P1)" src="https://user-images.githubusercontent.com/105996656/169702332-781dd5a8-89d2-449b-aeb2-9905b66d0346.png">

  STEP 4: CREATING A VIRTUAL HOST FOR YOUR WEBSITE USING APACHE
  Here, my intention was to establish a domain projectlamp. I made a directory for projectlamp using: sudo mkdir /var/www/projectlamp. Next, i changed ownership of the directory to my current user using :  sudo chown -R $USER:$USER /var/www/projectlamp.
  After that, i used the Vim editor to creae and open a new configuration file in Apache's sites-available directory, where i put this code in:
  
  <VirtualHost *:80>
    ServerName projectlamp
    ServerAlias www.projectlamp 
    ServerAdmin webmaster@localhost
    DocumentRoot /var/www/projectlamp
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
  
  Enable the new virtual host using the a2ensite command: sudo a2ensite projectlamp
  
  Disable Apache's default Website: sudo a2dissite 000-default
  
  Check for syntax Error and run :sudo apache2ctl configtest
  
  Finally, reload Apache so these changes take effect and run: sudo systemctl reload apache2
  
  Access the website by it's public DNS name or IP
  
  
<img width="754" alt="website on web browser (P2)" src="https://user-images.githubusercontent.com/105996656/169703743-d7834bf9-eb4b-4c44-ac10-3e17655daa6c.png">
  
  STEP 5- ENABLE PHP ON THE WBSITE
  
  Run: sudo vim /etc/apache2/mods-enabled/dir.conf
  and paste :
  <IfModule mod_dir.c>
        #Change this:
        #DirectoryIndex index.html index.cgi index.pl index.php index.xhtml index.htm
        #To this:
        DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm
</IfModule>
  
  To save this file we use :wqa
  After which we run: sudo systemctl reload apache2, this will reload Apache so its take effect
  
  Now, create a new file named index.php inside your custom web root folder: vim /var/www/projectlamp/index.php
  
  and paste this in : 
  <?php
phpinfo();

Save this file and reload the webpage, you will see:


<img width="1792" alt="PHP installation working as expected  (P1)" src="https://user-images.githubusercontent.com/105996656/169704669-0a4613f2-949b-4c7b-b91b-1721289ccf66.png">

Remove the file you created as it contains sensitive information about your PHP enviroment, use 

: sudo rm /var/www/projectlamp/index.php
  
  
  



