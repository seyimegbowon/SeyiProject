
## Project 2 ##

# LEMP STACK IMPLEMENTATION #

sudo apt update

sudo apt install nginx

sudo systemctl status nginx

curl http://localhost:80

![image](https://user-images.githubusercontent.com/106885875/177059656-5c37c998-9723-43c4-baa4-2b262caf29a8.png)

sudo apt install mysql-server

sudo mysql

sudo mysql_secure_installation

Failed! Error: SET PASSWORD has no significance for user ‘root’@’localhost’ as the authentication method used doesn’t store authentication data in the MySQL server. Please consider using ALTER USER instead if you want to change authentication parameters.

solved: sudo mysql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password by 'mynewpassword';

sudo mysql_secure_installation

sudo mysql -p

sudo apt install php-fpm php-mysql

sudo mkdir /var/www/myprojectLEMP

sudo chown -R $USER:$USER /var/www/myprojectLEMP

sudo nano /etc/nginx/sites-available/myprojectLEMP

sudo ln -s /etc/nginx/sites-available/myprojectLEMP /etc/nginx/sites-enabled/

sudo nginx -t

sudo unlink /etc/nginx/sites-enabled/default

sudo systemctl reload nginx

sudo echo 'Hello LEMP from hostname' $(curl -s http://169.254.169.254/latest/meta-data/public-hostname) 'with public IP' $(curl -s http://169.254.169.254/latest/meta-data/public-ipv4) > /var/www/myprojectLEMP/index.html


http://44.201.205.94:80
![image](https://user-images.githubusercontent.com/106885875/177115655-934c1c34-7e82-45d6-80cd-6eca9b279b39.png)
![image](https://user-images.githubusercontent.com/106885875/177115793-0220694f-0c25-4c49-8438-6a8a21786760.png)


  
  
sudo nano /var/www/myprojectLEMP/info.php
  
![image](https://user-images.githubusercontent.com/106885875/177114983-b841d00f-bf78-4800-9854-1033ebfb7973.png)


 sudo rm var/www/myprojectLEMP/info.php
 sudo mysql
 sudo mysql -p
 
 mysql> CREATE USER 'example_user'@'%' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';
 
 GRANT ALL ON example_database.* TO 'example_user'@'%';
 
 exit
 
 mysql -u example_user -p
mysql> SHOW DATABASES;

CREATE TABLE example_database.todo_list (
mysql>     item_id INT AUTO_INCREMENT,
mysql>     content VARCHAR(255),
mysql>     PRIMARY KEY(item_id)
mysql> );

INSERT INTO example_database.todo_list (content) VALUES ("My first important item");
SELECT * FROM example_database.todo_list;

nano /var/www/myprojectLEMP/todo_list.php


https://44.201.205.94/todo_list.php
![image](https://user-images.githubusercontent.com/106885875/177124189-36b2ee6e-3c45-423c-8691-70daf2dde6e3.png)




 
  
