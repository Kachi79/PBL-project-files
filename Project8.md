LOAD BALANCER SOLUTION WITH APACHE

In this project we will enhance our Tooling Website solution by adding a Load Balancer to disctribute traffic between Web Servers and allow users to 
access our website using a single URL.

The task would be to deploy and configure an Apache Load Balancer for Tooling Website solution on a separate Ubuntu EC2 intance and ensure that the users 
can be served by Web servers through the Load Balancer.

The first thing i did was to edit my inbound rules as directed by the documentation and open port 80 and make it accessible from anywhere.
<img width="1792" alt="Screenshot 2022-07-07 at 23 44 20" src="https://user-images.githubusercontent.com/105996656/177883846-10a5a0cb-3904-4200-bd6d-0e748bf274a9.png">

After i installed Apache Load Balancer on my load balancer (LB) server and configured it to point traffic coming to LB to both Web Servers: 1 & 2.
<img width="1519" alt="Screenshot 2022-07-07 at 23 49 29" src="https://user-images.githubusercontent.com/105996656/177884296-fe18bef8-6501-4898-9594-90bddf252c2c.png">
<img width="1792" alt="Screenshot 2022-07-07 at 23 50 20" src="https://user-images.githubusercontent.com/105996656/177884325-13c6919d-d0f9-42b3-bd47-d93a1011c544.png">

After that i restarted apache and ensured that it was running.
<img width="1150" alt="Screenshot 2022-07-07 at 23 53 26" src="https://user-images.githubusercontent.com/105996656/177884625-691c3e5f-1f6b-46a2-b031-333edb1bf168.png">
I unmounted both webservers and ensured that they both had their invidual log directories after which i ran the command:
sudo tail -f /var/log/httpd/access_log

After that i configured the local DNS NAMES RESOLUTION.
<img width="1792" alt="Screenshot 2022-07-07 at 23 55 56" src="https://user-images.githubusercontent.com/105996656/177885252-71fbc01b-886a-4c28-98a5-b0633ef9b7cf.png">

Finally i curled both webservers locally using the command : curl http://Web1 
<img width="1792" alt="Screenshot 2022-07-08 at 00 02 13" src="https://user-images.githubusercontent.com/105996656/177885527-206c2fdc-ed44-4062-a7ca-cf785c41e289.png">
<img width="1792" alt="Screenshot 2022-07-08 at 00 02 04" src="https://user-images.githubusercontent.com/105996656/177885529-92dc473d-ccf8-4656-aa37-9f0dececbf68.png">

