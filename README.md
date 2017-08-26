# NGINX: Create a New Site/virtual Host and secure it with Lets Encrypt SSL Certificate
Simple script to setup a new site with a Lets Encrypt SSL Certificate


Learn more about Lets Encrypt for NGINX
https://letsecure.me/secure-web-deployment-with-lets-encrypt-and-nginx/

## First Steps: 
Install certbot
``` bash
sudo add-apt-repository ppa:certbot/certbot
sudo apt-get update
sudo apt-get install certbot
```

## Check out this script then make it excuitable 
``` bash 
chmod .+ new_site.sh
```

## Edit any variables
You will need to check the script as I have set the paths to the default NGINX install on Ubuntu 16.04 which assumes the gninx sites config are in /etc/nginx/sites-enabled and that your web root is /var/www/. 

## How to use:
As root (sudo user)
``` bash
sudo ./new_site.sh
```

You will be promted to enter the root domain, eg: example.com (NOT www.example.com)

As basic config file will be created, NGINX will be reloaded, and then the Certbot Let Encrypt call will be made. 
Once that has created the certificates, a full secure hardened conf file will be installed and NGINX will be reloaded again. 

A site folder will be created on the server in 
``` bash 
/var/www/{domain}/www
```

NGINX will be configured to point to here also.


You're ready to go!

## Do what you want
Do what you want with this, use it, alter it, give feedback. 
If you have suggestions to make it better, please let me know. 
