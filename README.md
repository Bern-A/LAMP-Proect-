# LAMP-Proect-
Created my AWS account and did the following;

1. Signed into my AWS and created a new EC2 instance with Ubuntu Server. Saved the private key. Connected to my instance using CMD.
2. Install package update by running sudo apt update. Install apache by running sudo apt install apache2. Verified that apache2 is running by entering command sudo systemctl status apache2. see screen shot 

![Capture1](https://user-images.githubusercontent.com/92868845/138126652-684416ee-495b-46da-9f02-8e365319a3f0.PNG)

Opened TCP port 80 which is the default port that web browsers use to access web pages see screen shot

![Capture2](https://user-images.githubusercontent.com/92868845/138127938-29d5cc13-ff5f-4519-9eca-7c8c9b4a07ab.PNG)

Verified my web server is now correctly installed and accessible through my firewall. Open my EC2 public IP Address on my browser. See Screen Shot 

![Capture3](https://user-images.githubusercontent.com/92868845/138140963-dcc2ce58-40fa-45ec-8605-a5cc54c76cf1.PNG)

# Installed MySql
Install a DBMS to be able to store and manage data for my site in a relational database MySQL is a popular relational databse management syste, used within PHP environment. Ran sudo apt install mysql-server. 
Ran a security script that comes pre-installed with MYSQL sudo mysql_secure_installation
Validated my password. Tested my if i was able to log into  mysql console by typing sudo mysql. SEE SCREEN SHT

![Capture4](https://user-images.githubusercontent.com/92868845/138145829-a7559737-68d4-4e47-a976-5976149898e3.PNG)

Exit MYSQL console by typing mysql> exit

# Installing PHP
PHP is the component of our set up that will process code to disp;ay dynamic contect to end user. In addition to php package, php-mysql, php module that allos php to communicate with MYSQL-based databses is needed. libapache2-mod-php is needed to enable apache to handle php files. Core packages will automatically be installed as dependecies.
I installed  pakages at onces by running; sudo apt install php libapache2-mod-php php-mysql and ran php -v to confirm version. SEE SS

![Capture5](https://user-images.githubusercontent.com/92868845/138149696-7bc51501-f45c-4a0b-bdbd-37762e1ffa4b.PNG)

# Creating A Virtual Host For My Website Using Apache
I set up a domain called projectlamp using apache on Ubuntu 20.04 that has one server block enabled by default that is configured to serve document from the /var/www/html directory. i rand the command sudo mkdir /var/www/projectlamp
Assigned pwnership of the directory with current system user sudo chown -R $USER:$USER /var/www/projectlamp
Created and open a new configuration file in Apache's sites-available directory using sudo vi /etc/apache2/sites-available/projectlamp.conf
This created a new file. Pasted in the following bare-bones configuration by hitting i key to enter insert mode and pasted the text:
<VirtualHost *:80>
    ServerName projectlamp
    ServerAlias www.projectlamp 
    ServerAdmin webmaster@localhost
    DocumentRoot /var/www/projectlamp
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>

The saved and closed the file, using the steps below;
1. Hit esc on the keyboard
2. Type  :
3. Type wq
4. Hit Enter

I used the ls to show the file in the sites-available directroy by using sudo ls /etc/apache2/sites-available. SEE SS

![Capture6](https://user-images.githubusercontent.com/92868845/138155367-9875f9fe-be93-47f0-a90b-e0a0a0aa2a5d.PNG)



