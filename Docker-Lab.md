I set the IP address for docker01-riley as 10.0.5.12, hostname as docker01-riley.

Adding myself as a user was different, because I had to use "usermod -aG sudo riley", since I am using Ubuntu 22.04 rather than CentOS 7.

I added my docker01-riley system to my mgmt01-riley server's DNS Manager, and used the following source for disabling remote root for SSH.
Source: https://www.ionos.com/help/server-cloud-infrastructure/getting-started/important-security-information-for-your-server/deactivating-the-ssh-root-login/ 

I had various issues with connectivity and my Firewall going out, which I fixed each time by restarting my PFSense Firewall, which only took about 45 seconds.

I followed the instructions on the following link in order to install Docker on Ubuntu.

Source: https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04

In order to install docker-compose, I followed the instructions on the link provided.
Source: https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-compose-on-ubuntu-20-04

![image](https://github.com/RileyBashaw/SYS265/assets/112733012/8b5af60f-32bc-45d4-919b-ac04c3604e4d)
Installed Google via powershell since my mgmt01-riley system didn't come with any browser pre-installed. 
Watched this video https://www.youtube.com/watch?v=9d3tdTDxqRs&ab_channel=EasyTechStudios to download, as other resources failed to work.

I also used PFSense rather than centOS and Firewalld like the lab suggested, and added 32768/tcp to my firewall by adding it under NAT alongside the ports that were forwarded.


Used the following source to dockerize Wordpress within my docker01-riley server, utilizing some of the code and instructions.
Source: https://www.digitalocean.com/community/tutorials/how-to-install-wordpress-with-docker-compose

One of the frequent Docker commands I used were "docker-compose su", which shows the current containerized operations. Another one was "docker run" which was used to create a container based on a given template.

