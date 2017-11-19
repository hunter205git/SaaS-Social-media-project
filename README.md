mkdir ~/ossn_data
sudo 777 chmod ~/ossn_data/
sudo a2enmod rewrite
sudo nano /etc/apache2/sites-enabled/000-default.conf
<Directory /var/www/html>
                Options Indexes FollowSymLinks MultiViews
                AllowOverride All
                Order allow,deny
                allow from all
</Directory>
sudo nano /var/www/html/.htaccess
RewriteEngine on
sudo chmod 644 /var/www/html/.htaccess
sudo apt-get install php7.0-curl
sudo apt-get install php7.0-gd
sudo apt-get install php7.0-zip
sudo service apache2 restart