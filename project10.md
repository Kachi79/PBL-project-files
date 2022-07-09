LOAD BALANCER SOLUTION WITH NGINX AND SSL/TLS

This project is made up of 2 components, the firs part was to configure Nginx as a load balancer and the second was to register a new domain name and
configure a secured connection using SSL/TLS certificates.

The first thing i did was to update my server using the "sudo apt update" command.
After that i installed and configured nginx as a load balancer on the ubuntu instance i just created.
<img width="1334" alt="Screenshot 2022-07-09 at 12 10 48" src="https://user-images.githubusercontent.com/105996656/178103160-a47f1b58-ae8e-431e-9c9e-64a2be57b387.png">
<img width="1792" alt="Screenshot 2022-07-09 at 12 11 22" src="https://user-images.githubusercontent.com/105996656/178103198-3b416c21-9754-41cd-bd77-0ef4266fde7f.png">

The next thing i did was to update the nginx default configuration file using the command: sudo vi /etc/nginx/nginx.conf
<img width="1264" alt="nginx config  file" src="https://user-images.githubusercontent.com/105996656/178103311-0e43494c-6f6f-4da3-b6ae-62bd1d443d65.png">

I restarted the server and checked the status using: sudo systemctl restart nginx and sudo systemctl status nginx.
<img width="1376" alt="Screenshot 2022-07-09 at 12 20 51" src="https://user-images.githubusercontent.com/105996656/178103461-c136a9f4-7204-4e39-88eb-87aabf50d425.png">

After that i checked that i could reach my webservers from my browser using new domain name which uses HTTP protocol – and it could.

I installed certbot and requested for an SSL/TLS certificate using this command: "sudo ln -s /snap/bin/certbot /usr/bin/certbot"
<img width="950" alt="Screenshot 2022-07-09 at 12 52 48" src="https://user-images.githubusercontent.com/105996656/178104488-38840ae4-621b-4298-9801-a9cdc53f778e.png">

i tested a secured access to my Web Solution by trying to reach https://harrisdev.link (my domain name)

I was able to access my website by using HTTPS protocol (that uses TCP port 443) and see a padlock pictogram in your browser’s search string.
<img width="1792" alt="Screenshot 2022-07-09 at 11 51 11" src="https://user-images.githubusercontent.com/105996656/178104566-c025eba4-b0c2-444f-99a3-3db465a971a1.png">

<img width="1792" alt="Screenshot 2022-07-09 at 13 00 06" src="https://user-images.githubusercontent.com/105996656/178104726-e0c68887-4052-4b11-b1be-b9c579ea77bb.png">
