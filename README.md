### wordpress
# sudo apt update
update the list of available packages
# sudo apt upgrade
upgrade all installed packages to the latest versions
# sudo apt install apache2
install the apache webserver to serve wordpress
# sudo apt install mysql-server
install my-sql database server to store data
# sudo mysql_secure_installation
Run a security script to configure MYSQL setting root passwards removing test databases removing anonymous users
# sudo apt install php libapache2 -mod-php php-mysql php-curl php-xml php-mbstring php-zip
install php and require php modules
# cd /tmp
switches to the temporary directory
# wget https://wordpress.org/latest.tar.gz
download the latest version of wordpress
# tar xzvf latest.tar.gz 
extract the downloaded worpress archive
# sudo mv wordpress/* /var/www/html/
move all wordpress files to apache root directory because it will accessible through web
# sudo chown -R www-data:www-data /var/www/html/
change ownership of wordpress files to the apache user(www-data) permission to manage files
# sudo chmod -R 755 /var/www/html/
set the permission for files and directories
# sudo mysql -u root
login to mysql as root user
# CREATE DATABASE wordpress;
create a database name wordpress
# CREATE USER 'wpuser'@'localhost' IDENTIFIED BY 'password';
create a new MYSQL user wpuser with password 'password'
# GRANT ALL PRIVILEGES ON wordpress.* TO 'wpuser'@'localhost';
give a user complete access to do all operations in a database
# FLUSH PRIVILEGES;
which ensures that changes to user permissions are applied imediately
# EXIT;
mean exit the MYSQL database
# cd /var/www/html
change the current directory into the /var/www/html
# sudo cp wp-config-sample.php wp-config.php
# sudo nano wp-config.php
copies the sample configuration file (wp-config-sample.php)to wp-config.php used by wordpress
open the wp-config.php file and update the data base with these credentials 
# define('DB_NAME', 'wordpress');
# define('DB_USER', 'wpuser');
# define('DB_PASSWORD', 'password');
and then go to browser and put vm ip it will open wp installation page.
