**1. Project Overview :**
   - Goal: Host the open-source CRM software Krayin on a cloud provider so that it can be accessed and operated from another laptop.
   - Software Used: Krayin (an open-source Laravel-based CRM application).
   - Cloud Provider: Choosen cloud provider is DigitalOcean.
   - Target Audience: People who want to use Krayin CRM remotely.
   - Done By : Krish and Prarthana

**2. App Name:Krayin
     App description:
     github link:- https://github.com/krayin/laravel-crm
     hardware requirements:-Droplet with at least 1 vCPU, 1GB RAM, and 25GB SSD storage
     Local Machine with 4GB RAM and 10GB storage
     software requirements:-Server Software: Ubuntu 20.04+
                                             Apache2
                                             MySQL 8.0+
                                             PHP 8.0+ with required extensions
                                             Composer
                                             Let’s Encrypt SSL (optional for HTTPS)
                            Development Tools: Git
                                             SSH Client (OpenSSH, PuTTY)
                                             Text Editor (VS Code, Nano)
                           Dependencies (Handled by Composer):
                                             Laravel Framework
                                             MPDF
                                             PHPSpreadsheet
    flowchart on how the app works:-
       +----------------------+        +------------------------+        +--------------------+
   |                      |        |                        |        |                    |
   |       User           |        |      Apache Web       |        |  Application       |
   |  (Browser Client)    | <----> |        Server         | <----> |   Backend (PHP)    |
   |                      |        |    (HTTP/HTTPS)       |        |    Laravel         |
   +----------------------+        +------------------------+        +--------------------+
             |                                     |                           |
             |                                     |                           |
             v                                     v                           v
   +----------------------+         +-----------------------+       +-----------------------+
   |    SSL/HTTPS        |         |    Configuration      |       |    Application        |
   |   (Secure Access)   |         |      Files (.env)     |       |    Logic/Controllers  |
   |                     |         |                       |       |    (Krayin CRM)       |
   +----------------------+         +-----------------------+       +-----------------------+
             |                                     |                           |
             |                                     |                           |
             v                                     v                           v
   +-----------------------+        +-------------------------+     +-------------------------+
   |   MySQL Database      | <----> |    Eloquent ORM        |     |       Storage           |
   | (Data Storage Layer)  |        |   (Laravel DB Layer)   |     |  (File Uploads, Logs)   |
   +-----------------------+        +-------------------------+     +-------------------------+


**3. Steps Followed :**

**Step 1: Connect to the Droplet** 
Command:  
`ssh root@your_droplet_ip`  
Purpose: This command establishes an SSH connection to the DigitalOcean droplet, allowing direct command-line access to the server.

**Step 2: Install Apache Web Server**  
Commands:  
`sudo apt update`  
`sudo apt install apache2 -y`  
`sudo systemctl start apache2`  
`sudo systemctl enable apache2`  
Purpose:  
- `sudo apt update` refreshes the package lists for the system to make sure you are installing the latest versions of software.  
- `sudo apt install apache2 -y` installs the Apache web server.  
- `sudo systemctl start apache2` starts the Apache service.  
- `sudo systemctl enable apache2` enables Apache to start automatically on system reboot.

**Step 3: Install Composer (PHP Dependency Manager)**  
Commands:  
`sudo apt install curl -y`  
`curl -sS https://getcomposer.org/installer | php`  
`sudo mv composer.phar /usr/local/bin/composer`  
Purpose:  
- `sudo apt install curl -y` installs `curl`, which is needed to download Composer.  
- `curl -sS https://getcomposer.org/installer | php` downloads and installs Composer, a PHP dependency manager.  
- `sudo mv composer.phar /usr/local/bin/composer` moves the Composer file to a globally accessible directory so it can be run from any terminal.

**Step 4: Install MySQL Database Server**  
Commands:  
`sudo apt install mysql-server -y`  
`sudo mysql_secure_installation`  
Purpose:  
- `sudo apt install mysql-server -y` installs the MySQL server on your droplet.  
- `sudo mysql_secure_installation` runs a script to secure the MySQL installation by setting the root password and removing unnecessary accounts.

**Step 5: Set Up MySQL Database and User**  
Commands:  
`mysql -u root -p`  
In MySQL shell:  
`CREATE DATABASE krayin_db;`  
`CREATE USER 'krayin_user'@'localhost' IDENTIFIED BY 'strong_password';`  
`GRANT ALL PRIVILEGES ON krayin_db.* TO 'krayin_user'@'localhost';`  
`FLUSH PRIVILEGES;`  
`EXIT;`  
Purpose:  
- `mysql -u root -p` connects to the MySQL server as the root user.  
- `CREATE DATABASE krayin_db;` creates a new database named `krayin_db`.  
- `CREATE USER 'krayin_user'@'localhost' IDENTIFIED BY 'strong_password';` creates a new MySQL user `krayin_user` with the specified password.  
- `GRANT ALL PRIVILEGES ON krayin_db.* TO 'krayin_user'@'localhost';` grants all privileges on the `krayin_db` database to the user `krayin_user`.  
- `FLUSH PRIVILEGES;` reloads the privileges to ensure they take effect.  
- `EXIT;` exits the MySQL shell.

**Step 6: Clone Krayin CRM Repository**  
Commands:  
`cd /var/www/html`  
`git clone https://github.com/krayin/laravel-crm.git krayin`  
Purpose:  
- `cd /var/www/html` navigates to the web root directory.  
- `git clone https://github.com/krayin/laravel-crm.git krayin` clones the Krayin CRM repository from GitHub into the `krayin` directory.

**Step 7: Set Up Permissions**  
Commands:  
`sudo chown -R www-data:www-data /var/www/html/krayin`  
`sudo chmod -R 775 /var/www/html/krayin/storage`  
`sudo chmod -R 775 /var/www/html/krayin/bootstrap/cache`  
Purpose:  
- `sudo chown -R www-data:www-data /var/www/html/krayin` ensures Apache has ownership over the Krayin directory.  
- `sudo chmod -R 775 /var/www/html/krayin/storage` and `sudo chmod -R 775 /var/www/html/krayin/bootstrap/cache` ensure the `storage` and `bootstrap/cache` directories are writable by the web server.

**Step 8: Install Project Dependencies**  
Commands:  
`cd /var/www/html/krayin`  
`composer install`  
Purpose:  
- `cd /var/www/html/krayin` navigates to the Krayin project directory.  
- `composer install` installs the required PHP dependencies listed in the `composer.json` file.

**Step 9: Set Up the Environment File**  
Commands:  
`cp .env.example .env`  
`nano .env`  
Purpose:  
- `cp .env.example .env` copies the example environment file to a new `.env` file.  
- `nano .env` opens the `.env` file in the text editor for you to configure the database connection and other environment variables.

Modified Environment Variables:  
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=krayin_db
DB_USERNAME=krayin_user
DB_PASSWORD=strong_password
```

**Step 10: Generate Application Key**  
Command:  
`php artisan key:generate`  
Purpose: This command generates a unique application key for the Laravel app, which is essential for securing user sessions and application data.

**Step 11: Run Database Migrations**  
Command:  
`php artisan migrate`  
Purpose: This command runs the database migrations to create the necessary tables in the `krayin_db` database.

**Step 12: Configure Apache for Krayin**  
Commands:  
`sudo nano /etc/apache2/sites-available/krayin.conf`  

Configuration content:  
```
<VirtualHost *:80>
    ServerAdmin admin@yourdomain.com
    DocumentRoot /var/www/html/krayin/public
    ServerName your_droplet_ip

    <Directory /var/www/html/krayin>
        AllowOverride All
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/krayin_error.log
    CustomLog ${APACHE_LOG_DIR}/krayin_access.log combined
</VirtualHost>
```  
Commands:  
`sudo a2ensite krayin.conf`  
`sudo a2enmod rewrite`  
`sudo systemctl restart apache2`  
Purpose:  
- `sudo nano /etc/apache2/sites-available/krayin.conf` opens the Apache configuration file for Krayin.  
- The configuration content defines the site settings like the document root, error logs, and access logs.  
- `sudo a2ensite krayin.conf` enables the Krayin site configuration in Apache.  
- `sudo a2enmod rewrite` enables the Apache mod_rewrite module, required for URL rewriting.  
- `sudo systemctl restart apache2` restarts Apache to apply the new configuration.

**Final Step: Access Your Application**  
Open your browser and navigate to `http://your_droplet_ip` to access your Krayin CRM application.
