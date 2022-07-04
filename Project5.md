  The task in this project is to Implement a Client-Server Architecture using MySQL Database Management System (DBMS).
In this project i created a client (webserver) and dababase server.
MYSQL SERVER INSTALLATION ON CLIENT:
<img width="790" alt="mysql-client server installatn" src="https://user-images.githubusercontent.com/105996656/177167391-de724c6a-e7aa-42a0-b7c3-7bcfaa1f60ca.png">
After installing the server the next thing i did was to configure the server with the right credentials
I also installed, updated and and configured mysql on the database server.

<img width="883" alt="db server config file" src="https://user-images.githubusercontent.com/105996656/177176221-b06d83ea-a81c-4a0c-996d-814861ad9f81.png">
To ensure connectivity i retrieved the the database server ip address from the client server:

<img width="1066" alt="db ip addr retrieval frm clnt server" src="https://user-images.githubusercontent.com/105996656/177176791-0f16eab4-71bc-41a1-9728-e0b86d3b8f3e.png">

After my configuration, i accessed and was able to show my database from client server.

Finally, i was able to connect to my database server from client server (webserver)

<img width="1000" alt="connectn 2 db server from client" src="https://user-images.githubusercontent.com/105996656/177177566-cc585e28-e579-4496-9684-e1a03539666b.png">




GLITCHES: In the implementation, i encountered a recurring blocker, when i was trying to gain access into mysql database, i could not gain access using the: "sudo mysql" command. i had to first register a root user user the command: ALTER USER 'root'@'localhost' IDENTIFIED BY 'password'; afterwhich i gained entry with the passowrd i created.
