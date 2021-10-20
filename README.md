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
