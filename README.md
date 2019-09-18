# Magento 2.1.7
## Requires  
Apache 2.2 or 2.4+  
MySQL 5.6  
PHP ~5.6.5|7.0.2|7.0.4|~7.0.6  
composer  
Some PHP extensions (mentioned below)  

# Linux installation
```
sudo apt-get update
```
```
sudo apt-get remove apache2* mysql* php* composer
```
```
sudo apt-get purge apache2* mysql* php* composer
```
```
sudo apt-get autoremove
```
```
sudo apt-get autoclean
```
```
sudo apt-get install apache2
```
```
sudo apt-get install mysql
```
Enter the root password and note it as well  
```
mysql_secure_installation
```
```
sudo nano /etc/apache2/apache2.conf
```
Change AllowOveride attribute of Directory /var/www to 'All'  
```
<Directory /var/www>
  AllowOveride All
  ...
</Directory>
```
```
sudo a2enmod rewrite
```
```
sudo service apache2 restart
```
```
sudo mkdir /var/www/html/magento2
```
```
sudo chown -R $USER:root /var/www/html
```
```
mysql -u root -p
```
Enter the root password you entered while installing MySQL  
```
mysql> CREATE DATABASE magento2;
```
```
mysql> quit
```
Go to https://github.com/magento/magento2/releases/tag/2.1.7 and download Source code (tar.gz)  

```
sudo tar ~/Downloads/ <name of tar file> -C /var/www/html/magento2
```
```
cd /var/www/html/magento2
```

```
sudo apt-get install php7.0*
```

```
sudo apt-get install composer
```

```
sudo composer install
```

```
sudo chmod -R 777 var/ pub/ app/etc
```

```
sudo service apache2 restart
```
Go to http://localhost/magento2/setup  
Everything should work fine.  
In case of any problems please rails issues.  
On the database setup page, fill these details:  
host: localhost  
username: root  
password: <your root password>  
database name: magento  	
