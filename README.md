# NGINX-New-Site-with-Certbox
Simple script to setup a new site with a Lets Encrypt SSL Certificate


Learn more about Lets Encrypt for NGINX
https://letsecure.me/secure-web-deployment-with-lets-encrypt-and-nginx/

## How to use:
As root (sudo user)
sudo ./new_site.sh

You will be promted to enter the root domain, eg: example.com (NOT www.example.com)

As basic config file will be created, NGINX will be reloaded, and then the Certbot Let Encrypt call will be made. 
Once that has created the certificates, a full secure hardened conf file will be installed and NGINX will be reloaded again. 

Then you're ready to go!
