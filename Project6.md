In this project i was be tasked to prepare a storage infrastructure on two Linux servers and implement a basic web solution using WordPress. WordPress is a free and open-source content management system written in PHP and paired with MySQL most times, it is a backend Relational Database Management System (RDBMS).
I configured storage subsystem for Web and Database servers based on Linux OS and the focus of this exercise was to give me a practical experience of working with disks, partitions and volumes in Linux. I was also installed WordPress and connected it to a remote MySQL database server. This was intented to solidify my skills of deploying Web and DB tiers of Web solution.

The first thing i did was to spin my instances and created volumes with i attached to "webserver".
<img width="1471" alt="Screenshot 2022-07-05 at 01 40 30" src="https://user-images.githubusercontent.com/105996656/177229579-86caeeb8-58dd-46dc-95a6-92bce43881f9.png">

Using the lsblk command i inspected the block devices attached to the webserver.
<img width="440" alt="lsblk" src="https://user-images.githubusercontent.com/105996656/177229769-26d86be5-68ac-4529-b6fa-cb271f259d7c.png">

Furthermore, i used the gdisk utility command to create a single partition on each of the 3 disks.
<img width="795" alt="gdisk :dev:xvdf" src="https://user-images.githubusercontent.com/105996656/177229984-1e12ae6c-a450-43e1-a602-653372544be1.png">

I sued the sudo pvs command to verify that the physical volumes were successfully created.
<img width="484" alt="sudo pvs" src="https://user-images.githubusercontent.com/105996656/177230248-18550686-1521-4eaa-ac9f-d23ba51711dd.png">

I also verified that the volume groups were created successfully using the sudo vgs command.
<img width="511" alt="volume groups" src="https://user-images.githubusercontent.com/105996656/177230456-c43bed77-82ab-4638-a6c7-9ae8319a7e1d.png">
 
 I updated the /etc/fstab file with my own UUID.
 <img width="741" alt="UUID updated" src="https://user-images.githubusercontent.com/105996656/177230965-3a2512da-9050-4ef6-b19a-2ec7e6089d22.png">
 
 After that i tested the configuration with the command "sudo mount -a" and reloaded daemon with the command "sudo systemctl daemon-reload".
 
 I updated and installed wordpress on my webserver, i restarted apache and configured selinux policies by changing the ownership of the file using this 
 command:   "sudo chown -R apache:apache /var/www/html/wordpress"
 
 I installed and configured mysql on my database sever, i further configured the database server to work with wordpress.
 
I opened MySQL port 3306 on my dbserver and allowed access to the dbserver only from my WebServer’s IP address, so in the Inbound Rule configuration i specified source as /32 and i enabled tcp port 80.

I then tested my configurations on the webpage using the public ip address: 

<img width="1792" alt="wordpress" src="https://user-images.githubusercontent.com/105996656/177232755-d44af428-e1ea-4603-bc98-552bcfdc7af4.png">


 


