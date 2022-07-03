
## Project 2 ##

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


