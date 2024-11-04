prarthana@prarthana-VirtualBox:~$ ^[[200~ssh root@your_server_ip
ssh: command not found
prarthana@prarthana-VirtualBox:~$ ~ssh root@your_server_ip
Command '~ssh' not found, did you mean:
  command 'kssh' from snap kssh (0.1.0)
  command 'ssh' from deb openssh-client (1:8.9p1-3ubuntu0.10)
  command 'zssh' from deb zssh (1.5c.debian.1-8)
  command 'cssh' from deb clusterssh (4.16-3)
  command 'bssh' from deb avahi-ui-utils (0.8-5ubuntu5.2)
  command 'mssh' from deb mssh (2.2-5)
  command 'sssh' from deb guile-ssh (0.13.1-6)
See 'snap info <snapname>' for additional versions.
prarthana@prarthana-VirtualBox:~$ ssh root@your_server_ip
ssh: Could not resolve hostname your_server_ip: Temporary failure in name resolution
prarthana@prarthana-VirtualBox:~$ ssh root@142.93.220.90
root@142.93.220.90's password: 
Welcome to Ubuntu 24.10 (GNU/Linux 6.11.0-9-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Mon Nov  4 18:58:30 UTC 2024

  System load:  0.0               Processes:             109
  Usage of /:   2.4% of 76.45GB   Users logged in:       0
  Memory usage: 5%                IPv4 address for eth0: 142.93.220.90
  Swap usage:   0%                IPv4 address for eth0: 10.47.0.5

0 updates can be applied immediately.


Last login: Mon Nov  4 06:04:05 2024 from 91.109.17.144
root@ubuntu-finalproject:~# sudo apt update && sudo apt upgrade -y
Hit:1 https://repos-droplet.digitalocean.com/apt/droplet-agent main InRelease
Hit:2 https://repos.insights.digitalocean.com/apt/do-agent main InRelease      
Hit:3 http://mirrors.digitalocean.com/ubuntu oracular InRelease                
Get:4 http://mirrors.digitalocean.com/ubuntu oracular-updates InRelease [126 kB]
Get:5 http://security.ubuntu.com/ubuntu oracular-security InRelease [126 kB]
Get:6 http://mirrors.digitalocean.com/ubuntu oracular-backports InRelease [126 kB]
Get:7 http://mirrors.digitalocean.com/ubuntu oracular-updates/main amd64 Packages [47.6 kB]
Get:8 http://mirrors.digitalocean.com/ubuntu oracular-updates/main Translation-en [14.6 kB]
Get:9 http://mirrors.digitalocean.com/ubuntu oracular-updates/main amd64 Components [208 B]
Get:10 http://mirrors.digitalocean.com/ubuntu oracular-updates/universe amd64 Packages [10.5 kB]
Get:11 http://mirrors.digitalocean.com/ubuntu oracular-updates/universe Translation-en [5660 B]
Get:12 http://mirrors.digitalocean.com/ubuntu oracular-updates/universe amd64 Components [8392 B]
Get:13 http://mirrors.digitalocean.com/ubuntu oracular-updates/restricted amd64 Components [216 B]
Get:14 http://mirrors.digitalocean.com/ubuntu oracular-updates/multiverse amd64 Components [212 B]
Get:15 http://mirrors.digitalocean.com/ubuntu oracular-backports/main amd64 Components [212 B]
Get:16 http://security.ubuntu.com/ubuntu oracular-security/main amd64 Components [208 B]
Get:17 http://mirrors.digitalocean.com/ubuntu oracular-backports/universe amd64 Components [216 B]
Get:18 http://mirrors.digitalocean.com/ubuntu oracular-backports/restricted amd64 Components [216 B]
Get:19 http://security.ubuntu.com/ubuntu oracular-security/universe amd64 Components [208 B]
Get:20 http://security.ubuntu.com/ubuntu oracular-security/restricted amd64 Components [212 B]
Get:21 http://security.ubuntu.com/ubuntu oracular-security/multiverse amd64 Components [212 B]
Get:22 http://mirrors.digitalocean.com/ubuntu oracular-backports/multiverse amd64 Components [216 B]
Fetched 468 kB in 1s (318 kB/s)     
7 packages can be upgraded. Run 'apt list --upgradable' to see them.
Not upgrading yet due to phasing:
  grub-common         grub-efi-amd64-unsigned  grub-pc-bin
  grub-efi-amd64-bin  grub-pc                  grub2-common

Not upgrading:
  grub-efi-amd64-signed

Summary:
  Upgrading: 0, Installing: 0, Removing: 0, Not Upgrading: 7
Notice: Some packages may have been kept back due to phasing.
root@ubuntu-finalproject:~# sudo apt install php php-cli php-fpm php-mbstring php-xml php-zip php-curl php-mysql -y
Installing:                     
  php  php-cli  php-curl  php-fpm  php-mbstring  php-mysql  php-xml  php-zip

Installing dependencies:
  apache2                  libaprutil1-ldap  php8.3-cli       php8.3-readline
  apache2-bin              libaprutil1t64    php8.3-common    php8.3-xml
  apache2-data             libargon2-1       php8.3-curl      php8.3-zip
  apache2-utils            liblua5.4-0       php8.3-fpm       ssl-cert
  libapache2-mod-php8.3    libzip4t64        php8.3-mbstring
  libapr1t64               php-common        php8.3-mysql
  libaprutil1-dbd-sqlite3  php8.3            php8.3-opcache

Suggested packages:
  apache2-doc              | apache2-suexec-custom  php-pear
  apache2-suexec-pristine  www-browser

Summary:
  Upgrading: 0, Installing: 33, Removing: 0, Not Upgrading: 7
  Download size: 9903 kB
  Space needed: 39.4 MB / 80.1 GB available

Get:1 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libapr1t64 amd64 1.7.2-3.2ubuntu1 [108 kB]
Get:2 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libaprutil1t64 amd64 1.6.3-3ubuntu1 [92.8 kB]
Get:3 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libaprutil1-dbd-sqlite3 amd64 1.6.3-3ubuntu1 [11.4 kB]
Get:4 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libaprutil1-ldap amd64 1.6.3-3ubuntu1 [9208 B]
Get:5 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 liblua5.4-0 amd64 5.4.6-3build2 [166 kB]
Get:6 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 apache2-bin amd64 2.4.62-1ubuntu1 [1342 kB]
Get:7 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 apache2-data all 2.4.62-1ubuntu1 [163 kB]
Get:8 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 apache2-utils amd64 2.4.62-1ubuntu1 [97.9 kB]
Get:9 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 apache2 amd64 2.4.62-1ubuntu1 [90.4 kB]
Get:10 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 php-common all 2:93ubuntu2 [13.9 kB]
Get:11 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 php8.3-common amd64 8.3.11-0ubuntu0.24.10.2 [738 kB]
Get:12 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 php8.3-opcache amd64 8.3.11-0ubuntu0.24.10.2 [375 kB]
Get:13 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 php8.3-readline amd64 8.3.11-0ubuntu0.24.10.2 [13.6 kB]
Get:14 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libargon2-1 amd64 0~20190702+dfsg-4build1 [20.8 kB]
Get:15 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 php8.3-cli amd64 8.3.11-0ubuntu0.24.10.2 [1927 kB]
Get:16 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libapache2-mod-php8.3 amd64 8.3.11-0ubuntu0.24.10.2 [1859 kB]
Get:17 http://mirrors.digitalocean.com/ubuntu oracular/universe amd64 libzip4t64 amd64 1.7.3-1.1ubuntu2 [53.6 kB]
Get:18 http://mirrors.digitalocean.com/ubuntu oracular/universe amd64 php8.3-fpm amd64 8.3.11-0ubuntu0.24.10.2 [1937 kB]
Get:19 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 php8.3 all 8.3.11-0ubuntu0.24.10.2 [9176 B]
Get:20 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 php all 2:8.3+93ubuntu2 [4076 B]
Get:21 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 php-cli all 2:8.3+93ubuntu2 [4584 B]
Get:22 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 php8.3-curl amd64 8.3.11-0ubuntu0.24.10.2 [40.2 kB]
Get:23 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 php-curl all 2:8.3+93ubuntu2 [1836 B]
Get:24 http://mirrors.digitalocean.com/ubuntu oracular/universe amd64 php-fpm all 2:8.3+93ubuntu2 [4162 B]
Get:25 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 php8.3-mbstring amd64 8.3.11-0ubuntu0.24.10.2 [512 kB]
Get:26 http://mirrors.digitalocean.com/ubuntu oracular/universe amd64 php-mbstring all 2:8.3+93ubuntu2 [1848 B]
Get:27 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 php8.3-mysql amd64 8.3.11-0ubuntu0.24.10.2 [126 kB]
Get:28 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 php-mysql all 2:8.3+93ubuntu2 [1838 B]
Get:29 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 php8.3-xml amd64 8.3.11-0ubuntu0.24.10.2 [127 kB]
Get:30 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 php-xml all 2:8.3+93ubuntu2 [1856 B]
Get:31 http://mirrors.digitalocean.com/ubuntu oracular/universe amd64 php8.3-zip amd64 8.3.11-0ubuntu0.24.10.2 [29.6 kB]
Get:32 http://mirrors.digitalocean.com/ubuntu oracular/universe amd64 php-zip all 2:8.3+93ubuntu2 [1832 B]
Get:33 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 ssl-cert all 1.1.2ubuntu2 [18.0 kB]
Fetched 9903 kB in 7s (1500 kB/s)                                              
Extracting templates from packages: 100%
Preconfiguring packages ...
Selecting previously unselected package libapr1t64:amd64.
(Reading database ... 76054 files and directories currently installed.)
Preparing to unpack .../00-libapr1t64_1.7.2-3.2ubuntu1_amd64.deb ...
Unpacking libapr1t64:amd64 (1.7.2-3.2ubuntu1) ...
Selecting previously unselected package libaprutil1t64:amd64.
Preparing to unpack .../01-libaprutil1t64_1.6.3-3ubuntu1_amd64.deb ...
Unpacking libaprutil1t64:amd64 (1.6.3-3ubuntu1) ...
Selecting previously unselected package libaprutil1-dbd-sqlite3:amd64.
Preparing to unpack .../02-libaprutil1-dbd-sqlite3_1.6.3-3ubuntu1_amd64.deb ...
Unpacking libaprutil1-dbd-sqlite3:amd64 (1.6.3-3ubuntu1) ...
Selecting previously unselected package libaprutil1-ldap:amd64.
Preparing to unpack .../03-libaprutil1-ldap_1.6.3-3ubuntu1_amd64.deb ...
Unpacking libaprutil1-ldap:amd64 (1.6.3-3ubuntu1) ...
Selecting previously unselected package liblua5.4-0:amd64.
Preparing to unpack .../04-liblua5.4-0_5.4.6-3build2_amd64.deb ...
Unpacking liblua5.4-0:amd64 (5.4.6-3build2) ...
Selecting previously unselected package apache2-bin.
Preparing to unpack .../05-apache2-bin_2.4.62-1ubuntu1_amd64.deb ...
Unpacking apache2-bin (2.4.62-1ubuntu1) ...
Selecting previously unselected package apache2-data.
Preparing to unpack .../06-apache2-data_2.4.62-1ubuntu1_all.deb ...
Unpacking apache2-data (2.4.62-1ubuntu1) ...
Selecting previously unselected package apache2-utils.
Preparing to unpack .../07-apache2-utils_2.4.62-1ubuntu1_amd64.deb ...
Unpacking apache2-utils (2.4.62-1ubuntu1) ...
Selecting previously unselected package apache2.
Preparing to unpack .../08-apache2_2.4.62-1ubuntu1_amd64.deb ...
Unpacking apache2 (2.4.62-1ubuntu1) ...
Selecting previously unselected package php-common.
Preparing to unpack .../09-php-common_2%3a93ubuntu2_all.deb ...
Unpacking php-common (2:93ubuntu2) ...
Selecting previously unselected package php8.3-common.
Preparing to unpack .../10-php8.3-common_8.3.11-0ubuntu0.24.10.2_amd64.deb ...
Unpacking php8.3-common (8.3.11-0ubuntu0.24.10.2) ...
Selecting previously unselected package php8.3-opcache.
Preparing to unpack .../11-php8.3-opcache_8.3.11-0ubuntu0.24.10.2_amd64.deb ...
Unpacking php8.3-opcache (8.3.11-0ubuntu0.24.10.2) ...
Selecting previously unselected package php8.3-readline.
Preparing to unpack .../12-php8.3-readline_8.3.11-0ubuntu0.24.10.2_amd64.deb ...
Unpacking php8.3-readline (8.3.11-0ubuntu0.24.10.2) ...
Selecting previously unselected package libargon2-1:amd64.
Preparing to unpack .../13-libargon2-1_0~20190702+dfsg-4build1_amd64.deb ...
Unpacking libargon2-1:amd64 (0~20190702+dfsg-4build1) ...
Selecting previously unselected package php8.3-cli.
Preparing to unpack .../14-php8.3-cli_8.3.11-0ubuntu0.24.10.2_amd64.deb ...
Unpacking php8.3-cli (8.3.11-0ubuntu0.24.10.2) ...
Selecting previously unselected package libapache2-mod-php8.3.
Preparing to unpack .../15-libapache2-mod-php8.3_8.3.11-0ubuntu0.24.10.2_amd64.d
eb ...
Unpacking libapache2-mod-php8.3 (8.3.11-0ubuntu0.24.10.2) ...
Selecting previously unselected package libzip4t64:amd64.
Preparing to unpack .../16-libzip4t64_1.7.3-1.1ubuntu2_amd64.deb ...
Unpacking libzip4t64:amd64 (1.7.3-1.1ubuntu2) ...
Selecting previously unselected package php8.3-fpm.
Preparing to unpack .../17-php8.3-fpm_8.3.11-0ubuntu0.24.10.2_amd64.deb ...
Unpacking php8.3-fpm (8.3.11-0ubuntu0.24.10.2) ...
Selecting previously unselected package php8.3.
Preparing to unpack .../18-php8.3_8.3.11-0ubuntu0.24.10.2_all.deb ...
Unpacking php8.3 (8.3.11-0ubuntu0.24.10.2) ...
Selecting previously unselected package php.
Preparing to unpack .../19-php_2%3a8.3+93ubuntu2_all.deb ...
Unpacking php (2:8.3+93ubuntu2) ...
Selecting previously unselected package php-cli.
Preparing to unpack .../20-php-cli_2%3a8.3+93ubuntu2_all.deb ...
Unpacking php-cli (2:8.3+93ubuntu2) ...
Selecting previously unselected package php8.3-curl.
Preparing to unpack .../21-php8.3-curl_8.3.11-0ubuntu0.24.10.2_amd64.deb ...
Unpacking php8.3-curl (8.3.11-0ubuntu0.24.10.2) ...
Selecting previously unselected package php-curl.
Preparing to unpack .../22-php-curl_2%3a8.3+93ubuntu2_all.deb ...
Unpacking php-curl (2:8.3+93ubuntu2) ...
Selecting previously unselected package php-fpm.
Preparing to unpack .../23-php-fpm_2%3a8.3+93ubuntu2_all.deb ...
Unpacking php-fpm (2:8.3+93ubuntu2) ...
Selecting previously unselected package php8.3-mbstring.
Preparing to unpack .../24-php8.3-mbstring_8.3.11-0ubuntu0.24.10.2_amd64.deb ...
Unpacking php8.3-mbstring (8.3.11-0ubuntu0.24.10.2) ...
Selecting previously unselected package php-mbstring.
Preparing to unpack .../25-php-mbstring_2%3a8.3+93ubuntu2_all.deb ...
Unpacking php-mbstring (2:8.3+93ubuntu2) ...
Selecting previously unselected package php8.3-mysql.
Preparing to unpack .../26-php8.3-mysql_8.3.11-0ubuntu0.24.10.2_amd64.deb ...
Unpacking php8.3-mysql (8.3.11-0ubuntu0.24.10.2) ...
Selecting previously unselected package php-mysql.
Preparing to unpack .../27-php-mysql_2%3a8.3+93ubuntu2_all.deb ...
Unpacking php-mysql (2:8.3+93ubuntu2) ...
Selecting previously unselected package php8.3-xml.
Preparing to unpack .../28-php8.3-xml_8.3.11-0ubuntu0.24.10.2_amd64.deb ...
Unpacking php8.3-xml (8.3.11-0ubuntu0.24.10.2) ...
Selecting previously unselected package php-xml.
Preparing to unpack .../29-php-xml_2%3a8.3+93ubuntu2_all.deb ...
Unpacking php-xml (2:8.3+93ubuntu2) ...
Selecting previously unselected package php8.3-zip.
Preparing to unpack .../30-php8.3-zip_8.3.11-0ubuntu0.24.10.2_amd64.deb ...
Unpacking php8.3-zip (8.3.11-0ubuntu0.24.10.2) ...
Selecting previously unselected package php-zip.
Preparing to unpack .../31-php-zip_2%3a8.3+93ubuntu2_all.deb ...
Unpacking php-zip (2:8.3+93ubuntu2) ...
Selecting previously unselected package ssl-cert.
Preparing to unpack .../32-ssl-cert_1.1.2ubuntu2_all.deb ...
Unpacking ssl-cert (1.1.2ubuntu2) ...
Setting up php-common (2:93ubuntu2) ...
Created symlink '/etc/systemd/system/timers.target.wants/phpsessionclean.timer' 
→ '/usr/lib/systemd/system/phpsessionclean.timer'.
Setting up libargon2-1:amd64 (0~20190702+dfsg-4build1) ...
Setting up php8.3-common (8.3.11-0ubuntu0.24.10.2) ...

Creating config file /etc/php/8.3/mods-available/calendar.ini with new version

Creating config file /etc/php/8.3/mods-available/ctype.ini with new version

Creating config file /etc/php/8.3/mods-available/exif.ini with new version

Creating config file /etc/php/8.3/mods-available/fileinfo.ini with new version

Creating config file /etc/php/8.3/mods-available/ffi.ini with new version

Creating config file /etc/php/8.3/mods-available/ftp.ini with new version

Creating config file /etc/php/8.3/mods-available/gettext.ini with new version

Creating config file /etc/php/8.3/mods-available/iconv.ini with new version

Creating config file /etc/php/8.3/mods-available/pdo.ini with new version

Creating config file /etc/php/8.3/mods-available/phar.ini with new version

Creating config file /etc/php/8.3/mods-available/posix.ini with new version

Creating config file /etc/php/8.3/mods-available/shmop.ini with new version

Creating config file /etc/php/8.3/mods-available/sockets.ini with new version

Creating config file /etc/php/8.3/mods-available/sysvmsg.ini with new version

Creating config file /etc/php/8.3/mods-available/sysvsem.ini with new version

Creating config file /etc/php/8.3/mods-available/sysvshm.ini with new version

Creating config file /etc/php/8.3/mods-available/tokenizer.ini with new version
Setting up php8.3-mysql (8.3.11-0ubuntu0.24.10.2) ...

Creating config file /etc/php/8.3/mods-available/mysqlnd.ini with new version

Creating config file /etc/php/8.3/mods-available/mysqli.ini with new version

Creating config file /etc/php/8.3/mods-available/pdo_mysql.ini with new version
Setting up php8.3-mbstring (8.3.11-0ubuntu0.24.10.2) ...

Creating config file /etc/php/8.3/mods-available/mbstring.ini with new version
Setting up php8.3-readline (8.3.11-0ubuntu0.24.10.2) ...

Creating config file /etc/php/8.3/mods-available/readline.ini with new version
Setting up ssl-cert (1.1.2ubuntu2) ...
Created symlink '/etc/systemd/system/multi-user.target.wants/ssl-cert.service' →
 '/usr/lib/systemd/system/ssl-cert.service'.
Setting up libapr1t64:amd64 (1.7.2-3.2ubuntu1) ...
Setting up liblua5.4-0:amd64 (5.4.6-3build2) ...
Setting up php8.3-xml (8.3.11-0ubuntu0.24.10.2) ...

Creating config file /etc/php/8.3/mods-available/dom.ini with new version

Creating config file /etc/php/8.3/mods-available/simplexml.ini with new version

Creating config file /etc/php/8.3/mods-available/xml.ini with new version

Creating config file /etc/php/8.3/mods-available/xmlreader.ini with new version

Creating config file /etc/php/8.3/mods-available/xmlwriter.ini with new version

Creating config file /etc/php/8.3/mods-available/xsl.ini with new version
Setting up apache2-data (2.4.62-1ubuntu1) ...
Setting up php8.3-opcache (8.3.11-0ubuntu0.24.10.2) ...

Creating config file /etc/php/8.3/mods-available/opcache.ini with new version
Setting up libzip4t64:amd64 (1.7.3-1.1ubuntu2) ...
Setting up php-xml (2:8.3+93ubuntu2) ...
Setting up libaprutil1t64:amd64 (1.6.3-3ubuntu1) ...
Setting up php-mysql (2:8.3+93ubuntu2) ...
Setting up php8.3-curl (8.3.11-0ubuntu0.24.10.2) ...

Creating config file /etc/php/8.3/mods-available/curl.ini with new version
Setting up libaprutil1-ldap:amd64 (1.6.3-3ubuntu1) ...
Setting up php8.3-cli (8.3.11-0ubuntu0.24.10.2) ...
update-alternatives: using /usr/bin/php8.3 to provide /usr/bin/php (php) in auto
 mode
update-alternatives: using /usr/bin/phar8.3 to provide /usr/bin/phar (phar) in a
uto mode
update-alternatives: using /usr/bin/phar.phar8.3 to provide /usr/bin/phar.phar (
phar.phar) in auto mode

Creating config file /etc/php/8.3/cli/php.ini with new version
Setting up php-mbstring (2:8.3+93ubuntu2) ...
Setting up libaprutil1-dbd-sqlite3:amd64 (1.6.3-3ubuntu1) ...
Setting up php8.3-zip (8.3.11-0ubuntu0.24.10.2) ...

Creating config file /etc/php/8.3/mods-available/zip.ini with new version
Setting up php-cli (2:8.3+93ubuntu2) ...
update-alternatives: using /usr/bin/php.default to provide /usr/bin/php (php) in
 auto mode
update-alternatives: using /usr/bin/phar.default to provide /usr/bin/phar (phar)
 in auto mode
update-alternatives: using /usr/bin/phar.phar.default to provide /usr/bin/phar.p
har (phar.phar) in auto mode
Setting up php-zip (2:8.3+93ubuntu2) ...
Setting up apache2-utils (2.4.62-1ubuntu1) ...
Setting up php-curl (2:8.3+93ubuntu2) ...
Setting up php8.3-fpm (8.3.11-0ubuntu0.24.10.2) ...
Package apache2 is not configured yet. Will defer actions by package php8.3-fpm.

Creating config file /etc/php/8.3/fpm/php.ini with new version
NOTICE: Not enabling PHP 8.3 FPM by default.
NOTICE: To enable PHP 8.3 FPM in Apache2 do:
NOTICE: a2enmod proxy_fcgi setenvif
NOTICE: a2enconf php8.3-fpm
NOTICE: You are seeing this message because you have apache2 package installed.
Created symlink '/etc/systemd/system/multi-user.target.wants/php8.3-fpm.service'
 → '/usr/lib/systemd/system/php8.3-fpm.service'.
Setting up apache2-bin (2.4.62-1ubuntu1) ...
Setting up php8.3 (8.3.11-0ubuntu0.24.10.2) ...
Setting up php-fpm (2:8.3+93ubuntu2) ...
Setting up libapache2-mod-php8.3 (8.3.11-0ubuntu0.24.10.2) ...
Package apache2 is not configured yet. Will defer actions by package libapache2-
mod-php8.3.

Creating config file /etc/php/8.3/apache2/php.ini with new version
No module matches 
Setting up php (2:8.3+93ubuntu2) ...
Setting up apache2 (2.4.62-1ubuntu1) ...
Enabling module mpm_event.
Enabling module authz_core.
Enabling module authz_host.
Enabling module authn_core.
Enabling module auth_basic.
Enabling module access_compat.
Enabling module authn_file.
Enabling module authz_user.
Enabling module alias.
Enabling module dir.
Enabling module autoindex.
Enabling module env.
Enabling module mime.
Enabling module negotiation.
Enabling module setenvif.
Enabling module filter.
Enabling module deflate.
Enabling module status.
Enabling module reqtimeout.
Enabling conf charset.
Enabling conf localized-error-pages.
Enabling conf other-vhosts-access-log.
Enabling conf security.
Enabling conf serve-cgi-bin.
Enabling site 000-default.
info: Switch to mpm prefork for package libapache2-mod-php8.3
Module mpm_event disabled.
Enabling module mpm_prefork.
info: Executing deferred 'a2enmod php8.3' for package libapache2-mod-php8.3
Enabling module php8.3.
Created symlink '/etc/systemd/system/multi-user.target.wants/apache2.service' → 
'/usr/lib/systemd/system/apache2.service'.
Created symlink '/etc/systemd/system/multi-user.target.wants/apache-htcacheclean
.service' → '/usr/lib/systemd/system/apache-htcacheclean.service'.
Processing triggers for ufw (0.36.2-6) ...
Processing triggers for man-db (2.12.1-3) ...
Processing triggers for libc-bin (2.40-1ubuntu3) ...
Processing triggers for php8.3-cli (8.3.11-0ubuntu0.24.10.2) ...
Processing triggers for php8.3-fpm (8.3.11-0ubuntu0.24.10.2) ...
NOTICE: Not enabling PHP 8.3 FPM by default.
NOTICE: To enable PHP 8.3 FPM in Apache2 do:
NOTICE: a2enmod proxy_fcgi setenvif
NOTICE: a2enconf php8.3-fpm
NOTICE: You are seeing this message because you have apache2 package installed.
Processing triggers for libapache2-mod-php8.3 (8.3.11-0ubuntu0.24.10.2) ...
Scanning processes...                                                           
Scanning linux images...                                                        

Running kernel seems to be up-to-date.

No services need to be restarted.

No containers need to be restarted.

No user sessions are running outdated binaries.

No VM guests are running outdated hypervisor (qemu) binaries on this host.
root@ubuntu-finalproject:~# sudo apt install mysql-server -y
Installing:                     
  mysql-server

Installing dependencies:
  libcgi-fast-perl            libhtml-tagset-perl     liburi-perl
  libcgi-pm-perl              libhtml-template-perl   mecab-ipadic
  libclone-perl               libhttp-date-perl       mecab-ipadic-utf8
  libencode-locale-perl       libhttp-message-perl    mecab-utils
  libevent-pthreads-2.1-7t64  libio-html-perl         mysql-client-8.0
  libfcgi-bin                 liblwp-mediatypes-perl  mysql-client-core-8.0
  libfcgi-perl                libmecab2               mysql-common
  libfcgi0t64                 libprotobuf-lite32t64   mysql-server-8.0
  libhtml-parser-perl         libtimedate-perl        mysql-server-core-8.0

Suggested packages:
  libdata-dump-perl           libbusiness-isbn-perl  mailx
  libipc-sharedcache-perl     libregexp-ipv6-perl    tinyca
  libio-compress-brotli-perl  libwww-perl

Summary:
  Upgrading: 0, Installing: 28, Removing: 0, Not Upgrading: 7
  Download size: 29.4 MB
  Space needed: 244 MB / 80.1 GB available

Get:1 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 mysql-common all 5.8+1.1.1 [6800 B]
Get:2 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 mysql-client-core-8.0 amd64 8.0.39-1 [2549 kB]
Get:3 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 mysql-client-8.0 amd64 8.0.39-1 [22.4 kB]
Get:4 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libevent-pthreads-2.1-7t64 amd64 2.1.12-stable-10 [7966 B]
Get:5 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libmecab2 amd64 0.996-14ubuntu5 [206 kB]
Get:6 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libprotobuf-lite32t64 amd64 3.21.12-9ubuntu1 [238 kB]
Get:7 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 mysql-server-core-8.0 amd64 8.0.39-1 [17.5 MB]
Get:8 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 mysql-server-8.0 amd64 8.0.39-1 [1430 kB]
Get:9 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libhtml-tagset-perl all 3.24-1 [14.1 kB]
Get:10 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 liburi-perl all 5.28-1 [88.1 kB]
Get:11 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libhtml-parser-perl amd64 3.83-1 [86.1 kB]
Get:12 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libcgi-pm-perl all 4.66-1 [185 kB]
Get:13 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libfcgi0t64 amd64 2.4.2-2.1build1 [26.8 kB]
Get:14 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libfcgi-perl amd64 0.82+ds-3build2 [21.7 kB]
Get:15 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libcgi-fast-perl all 1:2.17-1 [10.3 kB]
Get:16 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libclone-perl amd64 0.46-1build3 [10.7 kB]
Get:17 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libencode-locale-perl all 1.05-3 [11.6 kB]
Get:18 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libfcgi-bin amd64 2.4.2-2.1build1 [11.2 kB]
Get:19 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libhtml-template-perl all 2.97-2 [60.2 kB]
Get:20 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libtimedate-perl all 2.3300-2 [34.0 kB]
Get:21 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libhttp-date-perl all 6.06-1 [10.2 kB]
Get:22 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libio-html-perl all 1.004-3 [15.9 kB]
Get:23 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 liblwp-mediatypes-perl all 6.04-2 [20.1 kB]
Get:24 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 libhttp-message-perl all 6.46-1ubuntu1 [75.9 kB]
Get:25 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 mecab-utils amd64 0.996-14ubuntu5 [4876 B]
Get:26 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 mecab-ipadic all 2.7.0-20070801+main-3 [6718 kB]
Get:27 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 mecab-ipadic-utf8 all 2.7.0-20070801+main-3 [4384 B]
Get:28 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 mysql-server all 8.0.39-1 [9502 B]
Fetched 29.4 MB in 7s (4484 kB/s)                                              
Preconfiguring packages ...
Selecting previously unselected package mysql-common.
(Reading database ... 77026 files and directories currently installed.)
Preparing to unpack .../0-mysql-common_5.8+1.1.1_all.deb ...
Unpacking mysql-common (5.8+1.1.1) ...
Selecting previously unselected package mysql-client-core-8.0.
Preparing to unpack .../1-mysql-client-core-8.0_8.0.39-1_amd64.deb ...
Unpacking mysql-client-core-8.0 (8.0.39-1) ...
Selecting previously unselected package mysql-client-8.0.
Preparing to unpack .../2-mysql-client-8.0_8.0.39-1_amd64.deb ...
Unpacking mysql-client-8.0 (8.0.39-1) ...
Selecting previously unselected package libevent-pthreads-2.1-7t64:amd64.
Preparing to unpack .../3-libevent-pthreads-2.1-7t64_2.1.12-stable-10_amd64.deb 
...
Unpacking libevent-pthreads-2.1-7t64:amd64 (2.1.12-stable-10) ...
Selecting previously unselected package libmecab2:amd64.
Preparing to unpack .../4-libmecab2_0.996-14ubuntu5_amd64.deb ...
Unpacking libmecab2:amd64 (0.996-14ubuntu5) ...
Selecting previously unselected package libprotobuf-lite32t64:amd64.
Preparing to unpack .../5-libprotobuf-lite32t64_3.21.12-9ubuntu1_amd64.deb ...
Unpacking libprotobuf-lite32t64:amd64 (3.21.12-9ubuntu1) ...
Selecting previously unselected package mysql-server-core-8.0.
Preparing to unpack .../6-mysql-server-core-8.0_8.0.39-1_amd64.deb ...
Unpacking mysql-server-core-8.0 (8.0.39-1) ...
Setting up mysql-common (5.8+1.1.1) ...
update-alternatives: using /etc/mysql/my.cnf.fallback to provide /etc/mysql/my.c
nf (my.cnf) in auto mode
Selecting previously unselected package mysql-server-8.0.
(Reading database ... 77245 files and directories currently installed.)
Preparing to unpack .../00-mysql-server-8.0_8.0.39-1_amd64.deb ...
Unpacking mysql-server-8.0 (8.0.39-1) ...
Selecting previously unselected package libhtml-tagset-perl.
Preparing to unpack .../01-libhtml-tagset-perl_3.24-1_all.deb ...
Unpacking libhtml-tagset-perl (3.24-1) ...
Selecting previously unselected package liburi-perl.
Preparing to unpack .../02-liburi-perl_5.28-1_all.deb ...
Unpacking liburi-perl (5.28-1) ...
Selecting previously unselected package libhtml-parser-perl:amd64.
Preparing to unpack .../03-libhtml-parser-perl_3.83-1_amd64.deb ...
Unpacking libhtml-parser-perl:amd64 (3.83-1) ...
Selecting previously unselected package libcgi-pm-perl.
Preparing to unpack .../04-libcgi-pm-perl_4.66-1_all.deb ...
Unpacking libcgi-pm-perl (4.66-1) ...
Selecting previously unselected package libfcgi0t64:amd64.
Preparing to unpack .../05-libfcgi0t64_2.4.2-2.1build1_amd64.deb ...
Unpacking libfcgi0t64:amd64 (2.4.2-2.1build1) ...
Selecting previously unselected package libfcgi-perl.
Preparing to unpack .../06-libfcgi-perl_0.82+ds-3build2_amd64.deb ...
Unpacking libfcgi-perl (0.82+ds-3build2) ...
Selecting previously unselected package libcgi-fast-perl.
Preparing to unpack .../07-libcgi-fast-perl_1%3a2.17-1_all.deb ...
Unpacking libcgi-fast-perl (1:2.17-1) ...
Selecting previously unselected package libclone-perl:amd64.
Preparing to unpack .../08-libclone-perl_0.46-1build3_amd64.deb ...
Unpacking libclone-perl:amd64 (0.46-1build3) ...
Selecting previously unselected package libencode-locale-perl.
Preparing to unpack .../09-libencode-locale-perl_1.05-3_all.deb ...
Unpacking libencode-locale-perl (1.05-3) ...
Selecting previously unselected package libfcgi-bin.
Preparing to unpack .../10-libfcgi-bin_2.4.2-2.1build1_amd64.deb ...
Unpacking libfcgi-bin (2.4.2-2.1build1) ...
Selecting previously unselected package libhtml-template-perl.
Preparing to unpack .../11-libhtml-template-perl_2.97-2_all.deb ...
Unpacking libhtml-template-perl (2.97-2) ...
Selecting previously unselected package libtimedate-perl.
Preparing to unpack .../12-libtimedate-perl_2.3300-2_all.deb ...
Unpacking libtimedate-perl (2.3300-2) ...
Selecting previously unselected package libhttp-date-perl.
Preparing to unpack .../13-libhttp-date-perl_6.06-1_all.deb ...
Unpacking libhttp-date-perl (6.06-1) ...
Selecting previously unselected package libio-html-perl.
Preparing to unpack .../14-libio-html-perl_1.004-3_all.deb ...
Unpacking libio-html-perl (1.004-3) ...
Selecting previously unselected package liblwp-mediatypes-perl.
Preparing to unpack .../15-liblwp-mediatypes-perl_6.04-2_all.deb ...
Unpacking liblwp-mediatypes-perl (6.04-2) ...
Selecting previously unselected package libhttp-message-perl.
Preparing to unpack .../16-libhttp-message-perl_6.46-1ubuntu1_all.deb ...
Unpacking libhttp-message-perl (6.46-1ubuntu1) ...
Selecting previously unselected package mecab-utils.
Preparing to unpack .../17-mecab-utils_0.996-14ubuntu5_amd64.deb ...
Unpacking mecab-utils (0.996-14ubuntu5) ...
Selecting previously unselected package mecab-ipadic.
Preparing to unpack .../18-mecab-ipadic_2.7.0-20070801+main-3_all.deb ...
Unpacking mecab-ipadic (2.7.0-20070801+main-3) ...
Selecting previously unselected package mecab-ipadic-utf8.
Preparing to unpack .../19-mecab-ipadic-utf8_2.7.0-20070801+main-3_all.deb ...
Unpacking mecab-ipadic-utf8 (2.7.0-20070801+main-3) ...
Selecting previously unselected package mysql-server.
Preparing to unpack .../20-mysql-server_8.0.39-1_all.deb ...
Unpacking mysql-server (8.0.39-1) ...
Setting up libprotobuf-lite32t64:amd64 (3.21.12-9ubuntu1) ...
Setting up libmecab2:amd64 (0.996-14ubuntu5) ...
Setting up mysql-client-core-8.0 (8.0.39-1) ...
Setting up libclone-perl:amd64 (0.46-1build3) ...
Setting up libevent-pthreads-2.1-7t64:amd64 (2.1.12-stable-10) ...
Setting up libfcgi0t64:amd64 (2.4.2-2.1build1) ...
Setting up libhtml-tagset-perl (3.24-1) ...
Setting up liblwp-mediatypes-perl (6.04-2) ...
Setting up libfcgi-bin (2.4.2-2.1build1) ...
Setting up libencode-locale-perl (1.05-3) ...
Setting up mecab-utils (0.996-14ubuntu5) ...
Setting up libio-html-perl (1.004-3) ...
Setting up mysql-server-core-8.0 (8.0.39-1) ...
Setting up libtimedate-perl (2.3300-2) ...
Setting up mysql-client-8.0 (8.0.39-1) ...
Setting up libfcgi-perl (0.82+ds-3build2) ...
Setting up liburi-perl (5.28-1) ...
Setting up mysql-server-8.0 (8.0.39-1) ...
update-alternatives: using /etc/mysql/mysql.cnf to provide /etc/mysql/my.cnf (my
.cnf) in auto mode
Renaming removed key_buffer and myisam-recover options (if present)
mysqld will log errors to /var/log/mysql/error.log
mysqld is running as pid 24480
Created symlink '/etc/systemd/system/multi-user.target.wants/mysql.service' → '/
usr/lib/systemd/system/mysql.service'.
Setting up libhttp-date-perl (6.06-1) ...
Setting up mecab-ipadic (2.7.0-20070801+main-3) ...
Compiling IPA dictionary for Mecab.  This takes long time...
reading /usr/share/mecab/dic/ipadic/unk.def ... 40
emitting double-array: 100% |###########################################| 
/usr/share/mecab/dic/ipadic/model.def is not found. skipped.
reading /usr/share/mecab/dic/ipadic/Adverb.csv ... 3032
reading /usr/share/mecab/dic/ipadic/Auxil.csv ... 199
reading /usr/share/mecab/dic/ipadic/Noun.csv ... 60477
reading /usr/share/mecab/dic/ipadic/Postp.csv ... 146
reading /usr/share/mecab/dic/ipadic/Conjunction.csv ... 171
reading /usr/share/mecab/dic/ipadic/Adnominal.csv ... 135
reading /usr/share/mecab/dic/ipadic/Interjection.csv ... 252
reading /usr/share/mecab/dic/ipadic/Filler.csv ... 19
reading /usr/share/mecab/dic/ipadic/Noun.nai.csv ... 42
reading /usr/share/mecab/dic/ipadic/Verb.csv ... 130750
reading /usr/share/mecab/dic/ipadic/Noun.name.csv ... 34202
reading /usr/share/mecab/dic/ipadic/Adj.csv ... 27210
reading /usr/share/mecab/dic/ipadic/Noun.verbal.csv ... 12146
reading /usr/share/mecab/dic/ipadic/Others.csv ... 2
reading /usr/share/mecab/dic/ipadic/Noun.adverbal.csv ... 795
reading /usr/share/mecab/dic/ipadic/Noun.demonst.csv ... 120
reading /usr/share/mecab/dic/ipadic/Suffix.csv ... 1393
reading /usr/share/mecab/dic/ipadic/Noun.org.csv ... 16668
reading /usr/share/mecab/dic/ipadic/Postp-col.csv ... 91
reading /usr/share/mecab/dic/ipadic/Noun.others.csv ... 151
reading /usr/share/mecab/dic/ipadic/Prefix.csv ... 221
reading /usr/share/mecab/dic/ipadic/Noun.number.csv ... 42
reading /usr/share/mecab/dic/ipadic/Symbol.csv ... 208
reading /usr/share/mecab/dic/ipadic/Noun.adjv.csv ... 3328
reading /usr/share/mecab/dic/ipadic/Noun.place.csv ... 72999
reading /usr/share/mecab/dic/ipadic/Noun.proper.csv ... 27328
emitting double-array: 100% |###########################################| 
reading /usr/share/mecab/dic/ipadic/matrix.def ... 1316x1316
emitting matrix      : 100% |###########################################| 

done!
update-alternatives: using /var/lib/mecab/dic/ipadic to provide /var/lib/mecab/d
ic/debian (mecab-dictionary) in auto mode
Setting up mecab-ipadic-utf8 (2.7.0-20070801+main-3) ...
Compiling IPA dictionary for Mecab.  This takes long time...
reading /usr/share/mecab/dic/ipadic/unk.def ... 40
emitting double-array: 100% |###########################################| 
/usr/share/mecab/dic/ipadic/model.def is not found. skipped.
reading /usr/share/mecab/dic/ipadic/Adverb.csv ... 3032
reading /usr/share/mecab/dic/ipadic/Auxil.csv ... 199
reading /usr/share/mecab/dic/ipadic/Noun.csv ... 60477
reading /usr/share/mecab/dic/ipadic/Postp.csv ... 146
reading /usr/share/mecab/dic/ipadic/Conjunction.csv ... 171
reading /usr/share/mecab/dic/ipadic/Adnominal.csv ... 135
reading /usr/share/mecab/dic/ipadic/Interjection.csv ... 252
reading /usr/share/mecab/dic/ipadic/Filler.csv ... 19
reading /usr/share/mecab/dic/ipadic/Noun.nai.csv ... 42
reading /usr/share/mecab/dic/ipadic/Verb.csv ... 130750
reading /usr/share/mecab/dic/ipadic/Noun.name.csv ... 34202
reading /usr/share/mecab/dic/ipadic/Adj.csv ... 27210
reading /usr/share/mecab/dic/ipadic/Noun.verbal.csv ... 12146
reading /usr/share/mecab/dic/ipadic/Others.csv ... 2
reading /usr/share/mecab/dic/ipadic/Noun.adverbal.csv ... 795
reading /usr/share/mecab/dic/ipadic/Noun.demonst.csv ... 120
reading /usr/share/mecab/dic/ipadic/Suffix.csv ... 1393
reading /usr/share/mecab/dic/ipadic/Noun.org.csv ... 16668
reading /usr/share/mecab/dic/ipadic/Postp-col.csv ... 91
reading /usr/share/mecab/dic/ipadic/Noun.others.csv ... 151
reading /usr/share/mecab/dic/ipadic/Prefix.csv ... 221
reading /usr/share/mecab/dic/ipadic/Noun.number.csv ... 42
reading /usr/share/mecab/dic/ipadic/Symbol.csv ... 208
reading /usr/share/mecab/dic/ipadic/Noun.adjv.csv ... 3328
reading /usr/share/mecab/dic/ipadic/Noun.place.csv ... 72999
reading /usr/share/mecab/dic/ipadic/Noun.proper.csv ... 27328
emitting double-array: 100% |###########################################| 
reading /usr/share/mecab/dic/ipadic/matrix.def ... 1316x1316
emitting matrix      : 100% |###########################################| 

done!
update-alternatives: using /var/lib/mecab/dic/ipadic-utf8 to provide /var/lib/me
cab/dic/debian (mecab-dictionary) in auto mode
Setting up libhtml-parser-perl:amd64 (3.83-1) ...
Setting up libhttp-message-perl (6.46-1ubuntu1) ...
Setting up mysql-server (8.0.39-1) ...
Setting up libcgi-pm-perl (4.66-1) ...
Setting up libhtml-template-perl (2.97-2) ...
Setting up libcgi-fast-perl (1:2.17-1) ...
Processing triggers for man-db (2.12.1-3) ...
Processing triggers for libc-bin (2.40-1ubuntu3) ...
Scanning processes...                                                           
Scanning linux images...                                                        

Running kernel seems to be up-to-date.

No services need to be restarted.

No containers need to be restarted.

No user sessions are running outdated binaries.

No VM guests are running outdated hypervisor (qemu) binaries on this host.
root@ubuntu-finalproject:~# sudo mysql_secure_installation

Securing the MySQL server deployment.

Connecting to MySQL using a blank password.

VALIDATE PASSWORD COMPONENT can be used to test passwords
and improve security. It checks the strength of password
and allows the users to set only those passwords which are
secure enough. Would you like to setup VALIDATE PASSWORD component?

Press y|Y for Yes, any other key for No: Y

There are three levels of password validation policy:

LOW    Length >= 8
MEDIUM Length >= 8, numeric, mixed case, and special characters
STRONG Length >= 8, numeric, mixed case, special characters and dictionary                  file

Please enter 0 = LOW, 1 = MEDIUM and 2 = STRONG: 1

Skipping password set for root as authentication with auth_socket is used by default.
If you would like to use password authentication instead, this can be done with the "ALTER_USER" command.
See https://dev.mysql.com/doc/refman/8.0/en/alter-user.html#alter-user-password-management for more information.

By default, a MySQL installation has an anonymous user,
allowing anyone to log into MySQL without having to have
a user account created for them. This is intended only for
testing, and to make the installation go a bit smoother.
You should remove them before moving into a production
environment.

Remove anonymous users? (Press y|Y for Yes, any other key for No) : y
Success.


Normally, root should only be allowed to connect from
'localhost'. This ensures that someone cannot guess at
the root password from the network.

Disallow root login remotely? (Press y|Y for Yes, any other key for No) : m

 ... skipping.
By default, MySQL comes with a database named 'test' that
anyone can access. This is also intended only for testing,
and should be removed before moving into a production
environment.


Remove test database and access to it? (Press y|Y for Yes, any other key for No) : y
 - Dropping test database...
Success.

 - Removing privileges on test database...
Success.

Reloading the privilege tables will ensure that all changes
made so far will take effect immediately.

Reload privilege tables now? (Press y|Y for Yes, any other key for No) : y
Success.

All done! 
root@ubuntu-finalproject:~# curl -sS https://getcomposer.org/installer | php
sudo mv composer.phar /usr/local/bin/composer
All settings correct for using Composer
Downloading...

Composer (version 2.8.2) successfully installed to: /root/composer.phar
Use it: php composer.phar

root@ubuntu-finalproject:~# ^[[200~git clone https://github.com/krayin/laravel-crm.git
git: command not found
root@ubuntu-finalproject:~# cd laravel-crm
-bash: cd: laravel-crm: No such file or directory
root@ubuntu-finalproject:~# git clone https://github.com/krayin/laravel-crm.git
cd laravel-crm
Cloning into 'laravel-crm'...
remote: Enumerating objects: 41973, done.
remote: Counting objects: 100% (3614/3614), done.
remote: Compressing objects: 100% (475/475), done.
remote: Total 41973 (delta 3368), reused 3195 (delta 3128), pack-reused 38359 (from 1)
Receiving objects: 100% (41973/41973), 39.17 MiB | 12.50 MiB/s, done.
Resolving deltas: 100% (26311/26311), done.
root@ubuntu-finalproject:~/laravel-crm# git clone https://github.com/krayin/laravel-crm.git
cd laravel-crm
Cloning into 'laravel-crm'...
remote: Enumerating objects: 41973, done.
remote: Counting objects: 100% (3614/3614), done.
remote: Compressing objects: 100% (475/475), done.
remote: Total 41973 (delta 3368), reused 3195 (delta 3128), pack-reused 38359 (from 1)
Receiving objects: 100% (41973/41973), 39.17 MiB | 19.63 MiB/s, done.
Resolving deltas: 100% (26311/26311), done.
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# cp .env.example .env
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# mysql -u root -p
CREATE DATABASE krayin;
exit;
Enter password: 
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 10
Server version: 8.0.39-1 (Ubuntu)

Copyright (c) 2000, 2024, Oracle and/or its affiliates.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> php artisan key:generate
    -> 
    -> php artisan key:generate
    -> 
    -> exit;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'php artisan key:generate

php artisan key:generate

exit' at line 1
mysql> php artisan key:generate
    -> 
    -> sudo apt install nginx -y
    -> 
    -> exit
    -> exit;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'php artisan key:generate

sudo apt install nginx -y

exit
exit' at line 1
mysql> php artisan key:ge
[1]+  Stopped                 mysql -u root -p
CREATE: command not found
logout
There are stopped jobs.
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# php artisan key:generate
PHP Warning:  require(/root/laravel-crm/laravel-crm/vendor/autoload.php): Failed to open stream: No such file or directory in /root/laravel-crm/laravel-crm/artisan on line 18
PHP Fatal error:  Uncaught Error: Failed opening required '/root/laravel-crm/laravel-crm/vendor/autoload.php' (include_path='.:/usr/share/php') in /root/laravel-crm/laravel-crm/artisan:18
Stack trace:
#0 {main}
  thrown in /root/laravel-crm/laravel-crm/artisan on line 18
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# mysql -u root -p
Enter password: 
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 11
Server version: 8.0.39-1 (Ubuntu)

Copyright (c) 2000, 2024, Oracle and/or its affiliates.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> CREATE DATABASE krayin;
Query OK, 1 row affected (0.01 sec)

mysql> exit;
Bye
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# php artisan key:generate
PHP Warning:  require(/root/laravel-crm/laravel-crm/vendor/autoload.php): Failed to open stream: No such file or directory in /root/laravel-crm/laravel-crm/artisan on line 18
PHP Fatal error:  Uncaught Error: Failed opening required '/root/laravel-crm/laravel-crm/vendor/autoload.php' (include_path='.:/usr/share/php') in /root/laravel-crm/laravel-crm/artisan:18
Stack trace:
#0 {main}
  thrown in /root/laravel-crm/laravel-crm/artisan on line 18
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# sudo apt install nginx -y
Installing:                     
  nginx

Installing dependencies:
  nginx-common

Suggested packages:
  fcgiwrap  nginx-doc

Summary:
  Upgrading: 0, Installing: 2, Removing: 0, Not Upgrading: 7
  Download size: 631 kB
  Space needed: 1811 kB / 79.3 GB available

Get:1 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 nginx-common all 1.26.0-2ubuntu3 [30.7 kB]
Get:2 http://mirrors.digitalocean.com/ubuntu oracular/main amd64 nginx amd64 1.26.0-2ubuntu3 [600 kB]
Fetched 631 kB in 1s (501 kB/s)
Preconfiguring packages ...
Selecting previously unselected package nginx-common.
(Reading database ... 77641 files and directories currently installed.)
Preparing to unpack .../nginx-common_1.26.0-2ubuntu3_all.deb ...
Unpacking nginx-common (1.26.0-2ubuntu3) ...
Selecting previously unselected package nginx.
Preparing to unpack .../nginx_1.26.0-2ubuntu3_amd64.deb ...
Unpacking nginx (1.26.0-2ubuntu3) ...
Setting up nginx (1.26.0-2ubuntu3) ...
Not attempting to start NGINX, port 80 is already in use.
Setting up nginx-common (1.26.0-2ubuntu3) ...
Created symlink '/etc/systemd/system/multi-user.target.wants/nginx.service' → '/
usr/lib/systemd/system/nginx.service'.
Could not execute systemctl:  at /usr/bin/deb-systemd-invoke line 148.
Processing triggers for ufw (0.36.2-6) ...
Processing triggers for man-db (2.12.1-3) ...
Scanning processes...                                                           
Scanning linux images...                                                        

Running kernel seems to be up-to-date.

No services need to be restarted.

No containers need to be restarted.

No user sessions are running outdated binaries.

No VM guests are running outdated hypervisor (qemu) binaries on this host.
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# server {
    listen 80;
    server_name your_domain_or_ip;

    root /path/to/krayin/public;
    index index.php index.html;

    location / {
        try_files $uri $uri/ /index.php?$query_string;
    }

    location ~ \.php$ {
        include snippets/fastcgi-php.conf;
        fastcgi_pass unix:/var/run/php/php7.4-fpm.sock;
    }
}
Command 'server' not found, did you mean:
  command 'serve' from snap serve (0.3.0)
  command 'serveo' from snap serveo (0.0.10)
  command 'kserver' from deb freewnn-kserver (1.1.1~a021+cvs20130302-8build1)
  command 'cserver' from deb freewnn-cserver (1.1.1~a021+cvs20130302-8build1)
  command 'jserver' from deb freewnn-jserver (1.1.1~a021+cvs20130302-8build1)
  command 'semver' from deb node-semver (7.6.1+~7.5.8-1)
See 'snap info <snapname>' for additional versions.
Command 'listen' not found, but can be installed with:
apt install ruby-listen
server_name: command not found
Command 'root' not found, but can be installed with:
snap install root-framework
Command 'index' not found, did you mean:
  command 'sindex' from deb biosquid (1.9g+cvs20050121-15.1build1)
  command 'xindex' from deb texlive-extra-utils (2024.20240706-2)
  command 'cindex' from deb codesearch (0.0~hg20120502-3build3)
Try: apt install <deb name>
Command 'location' not found, but can be installed with:
apt install location
try_files: command not found
-bash: syntax error near unexpected token `}'
Command 'location' not found, but can be installed with:
apt install location
include: command not found
fastcgi_pass: command not found
-bash: syntax error near unexpected token `}'
-bash: syntax error near unexpected token `}'
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# sudo systemctl restart nginx 
Job for nginx.service failed because the control process exited with error code.
See "systemctl status nginx.service" and "journalctl -xeu nginx.service" for details.
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# sudo systemctl restart nginx 
Job for nginx.service failed because the control process exited with error code.
See "systemctl status nginx.service" and "journalctl -xeu nginx.service" for details.
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# server {
    listen 80;
    server_name your_domain_or_ip;

    root /path/to/krayin/public;
    index index.php index.html;

    location / {
        try_files $uri $uri/ /index.php?$query_string;
    }

    location ~ \.php$ {
        include snippets/fastcgi-php.conf;
        fastcgi_pass unix:/var/run/php/php7.4-fpm.sock;
    }
}
Command 'server' not found, did you mean:
  command 'serveo' from snap serveo (0.0.10)
  command 'serve' from snap serve (0.3.0)
  command 'semver' from deb node-semver (7.6.1+~7.5.8-1)
  command 'jserver' from deb freewnn-jserver (1.1.1~a021+cvs20130302-8build1)
  command 'cserver' from deb freewnn-cserver (1.1.1~a021+cvs20130302-8build1)
  command 'kserver' from deb freewnn-kserver (1.1.1~a021+cvs20130302-8build1)
See 'snap info <snapname>' for additional versions.
Command 'listen' not found, but can be installed with:
apt install ruby-listen
server_name: command not found
Command 'root' not found, but can be installed with:
snap install root-framework
Command 'index' not found, did you mean:
  command 'cindex' from deb codesearch (0.0~hg20120502-3build3)
  command 'sindex' from deb biosquid (1.9g+cvs20050121-15.1build1)
  command 'xindex' from deb texlive-extra-utils (2024.20240706-2)
Try: apt install <deb name>
Command 'location' not found, but can be installed with:
apt install location
try_files: command not found
-bash: syntax error near unexpected token `}'
Command 'location' not found, but can be installed with:
apt install location
include: command not found
fastcgi_pass: command not found
-bash: syntax error near unexpected token `}'
-bash: syntax error near unexpected token `}'
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# sudo systemctl restart nginx
Job for nginx.service failed because the control process exited with error code.
See "systemctl status nginx.service" and "journalctl -xeu nginx.service" for details.
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# sudo nginx -t
nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
nginx: configuration file /etc/nginx/nginx.conf test is successful
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# sudo systemctl status nginx.service
× nginx.service - A high performance web server and a reverse proxy server
     Loaded: loaded (/usr/lib/systemd/system/nginx.service; enabled; preset: en>
     Active: failed (Result: exit-code) since Mon 2024-11-04 19:13:24 UTC; 40s >
 Invocation: 4f1f3fe647c8430d9148cd5df66586b8
       Docs: man:nginx(8)
    Process: 25351 ExecStartPre=/usr/sbin/nginx -t -q -g daemon on; master_proc>
    Process: 25353 ExecStart=/usr/sbin/nginx -g daemon on; master_process on; (>
   Mem peak: 1.7M
        CPU: 34ms
...skipping...
× nginx.service - A high performance web server and a reverse proxy server
     Loaded: loaded (/usr/lib/systemd/system/nginx.service; enabled; preset: en>
     Active: failed (Result: exit-code) since Mon 2024-11-04 19:13:24 UTC; 40s >
 Invocation: 4f1f3fe647c8430d9148cd5df66586b8
       Docs: man:nginx(8)
    Process: 25351 ExecStartPre=/usr/sbin/nginx -t -q -g daemon on; master_proc>
    Process: 25353 ExecStart=/usr/sbin/nginx -g daemon on; master_process on; (>
   Mem peak: 1.7M
        CPU: 34ms
~
~
~
~
~
~
~
~
~
~
~
~
~
~

root@ubuntu-finalproject:~/laravel-crm/laravel-crm# root /path/to/krayin/public; 
Command 'root' not found, but can be installed with:
snap install root-framework
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# root /path/to/krayin/public; 
Command 'root' not found, but can be installed with:
snap install root-framework
root@ubuntu-finalproject:~/laravel-crm/laravel-crm#  /path/to/krayin/public;
-bash: /path/to/krayin/public: No such file or directory
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# fastcgi_pass unix:/var/run/php/php7.4-fpm.sock;
fastcgi_pass: command not found
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# ^[[200~sudo nano /etc/nginx/sites-available/krayin
sudo: command not found
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# sudo nano /etc/nginx/sites-available/krayin
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# sudo ln -s /etc/nginx/sites-available/krayin /etc/nginx/sites-enabled/
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# sudo systemctl restart nginx
Job for nginx.service failed because the control process exited with error code.
See "systemctl status nginx.service" and "journalctl -xeu nginx.service" for details.
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# sudo nginx -t
nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
nginx: configuration file /etc/nginx/nginx.conf test is successful
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# ^C
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# sudo systemctl status php7.4-fpm
Unit php7.4-fpm.service could not be found.
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# sudo systemctl start php7.4-fpm
Failed to start php7.4-fpm.service: Unit php7.4-fpm.service not found.
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# fastcgi_pass unix:/var/run/php/php8.0-fpm.sock;
fastcgi_pass: command not found
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# php -v
PHP 8.3.11 (cli) (built: Sep 30 2024 12:07:44) (NTS)
Copyright (c) The PHP Group
Zend Engine v4.3.11, Copyright (c) Zend Technologies
    with Zend OPcache v8.3.11, Copyright (c), by Zend Technologies
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# sudo apt install php8.0-fpm
Error: Unable to locate package php8.0-fpm
Error: Couldn't find any package by glob 'php8.0-fpm'
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# sudo apt update
Hit:1 https://repos-droplet.digitalocean.com/apt/droplet-agent main InRelease
Hit:2 https://repos.insights.digitalocean.com/apt/do-agent main InRelease                          
Hit:3 http://mirrors.digitalocean.com/ubuntu oracular InRelease                                    
Hit:4 http://mirrors.digitalocean.com/ubuntu oracular-updates InRelease      
Hit:5 http://security.ubuntu.com/ubuntu oracular-security InRelease
Hit:6 http://mirrors.digitalocean.com/ubuntu oracular-backports InRelease
7 packages can be upgraded. Run 'apt list --upgradable' to see them.
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# sudo apt install software-properties-common -y
sudo add-apt-repository ppa:ondrej/php -y
sudo apt update
software-properties-common is already the newest version (0.102).
software-properties-common set to manually installed.
Summary:
  Upgrading: 0, Installing: 0, Removing: 0, Not Upgrading: 7
PPA publishes dbgsym, you may need to include 'main/debug' component
Repository: 'Types: deb
URIs: https://ppa.launchpadcontent.net/ondrej/php/ubuntu/
Suites: oracular
Components: main
'
Description:
Co-installable PHP versions: PHP 5.6, PHP 7.x, PHP 8.x and most requested extensions are included. Only Supported Ubuntu Releases (https://wiki.ubuntu.com/Releases) are provided.

Debian oldstable and stable packages are provided as well: https://deb.sury.org/#debian-dpa

You can get more information about the packages at https://deb.sury.org

BUGS&FEATURES: This PPA now has a issue tracker:
https://deb.sury.org/#bug-reporting

CAVEATS:
1. If you are using php-gearman, you need to add ppa:ondrej/pkg-gearman
2. If you are using apache2, you are advised to add ppa:ondrej/apache2
3. If you are using nginx, you are advised to add ppa:ondrej/nginx-mainline
   or ppa:ondrej/nginx

PLEASE READ: If you like my work and want to give me a little motivation, please consider donating regularly: https://donate.sury.org/

WARNING: add-apt-repository is broken with non-UTF-8 locales, see
https://github.com/oerdnj/deb.sury.org/issues/56 for workaround:

# LC_ALL=C.UTF-8 add-apt-repository ppa:ondrej/php
More info: https://launchpad.net/~ondrej/+archive/ubuntu/php
Adding repository.
Hit:1 https://repos-droplet.digitalocean.com/apt/droplet-agent main InRelease
Hit:2 https://repos.insights.digitalocean.com/apt/do-agent main InRelease                                                                                    
Hit:3 http://security.ubuntu.com/ubuntu oracular-security InRelease                                                                                          
Hit:4 http://mirrors.digitalocean.com/ubuntu oracular InRelease                                        
Hit:5 http://mirrors.digitalocean.com/ubuntu oracular-updates InRelease          
Ign:6 https://ppa.launchpadcontent.net/ondrej/php/ubuntu oracular InRelease
Hit:7 http://mirrors.digitalocean.com/ubuntu oracular-backports InRelease
Err:8 https://ppa.launchpadcontent.net/ondrej/php/ubuntu oracular Release
  404  Not Found [IP: 185.125.190.80 443]
Reading package lists... Done
E: The repository 'https://ppa.launchpadcontent.net/ondrej/php/ubuntu oracular Release' does not have a Release file.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.
Hit:1 https://repos-droplet.digitalocean.com/apt/droplet-agent main InRelease
Hit:2 https://repos.insights.digitalocean.com/apt/do-agent main InRelease                                                                                    
Hit:3 http://mirrors.digitalocean.com/ubuntu oracular InRelease                                                                                              
Hit:4 http://security.ubuntu.com/ubuntu oracular-security InRelease                                    
Hit:5 http://mirrors.digitalocean.com/ubuntu oracular-updates InRelease          
Hit:6 http://mirrors.digitalocean.com/ubuntu oracular-backports InRelease
Ign:7 https://ppa.launchpadcontent.net/ondrej/php/ubuntu oracular InRelease
Err:8 https://ppa.launchpadcontent.net/ondrej/php/ubuntu oracular Release
  404  Not Found [IP: 185.125.190.80 443]
Error: The repository 'https://ppa.launchpadcontent.net/ondrej/php/ubuntu oracular Release' does not have a Release file.
Notice: Updating from such a repository can't be done securely, and is therefore disabled by default.
Notice: See apt-secure(8) manpage for repository creation and user configuration details.
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# ^C
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# sudo apt install software-properties-common -y
software-properties-common is already the newest version (0.102).
Summary:
  Upgrading: 0, Installing: 0, Removing: 0, Not Upgrading: 7
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# sudo add-apt-repository ppa:ondrej/php -y
PPA publishes dbgsym, you may need to include 'main/debug' component
Repository: 'Types: deb
URIs: https://ppa.launchpadcontent.net/ondrej/php/ubuntu/
Suites: oracular
Components: main
'
Description:
Co-installable PHP versions: PHP 5.6, PHP 7.x, PHP 8.x and most requested extensions are included. Only Supported Ubuntu Releases (https://wiki.ubuntu.com/Releases) are provided.

Debian oldstable and stable packages are provided as well: https://deb.sury.org/#debian-dpa

You can get more information about the packages at https://deb.sury.org

BUGS&FEATURES: This PPA now has a issue tracker:
https://deb.sury.org/#bug-reporting

CAVEATS:
1. If you are using php-gearman, you need to add ppa:ondrej/pkg-gearman
2. If you are using apache2, you are advised to add ppa:ondrej/apache2
3. If you are using nginx, you are advised to add ppa:ondrej/nginx-mainline
   or ppa:ondrej/nginx

PLEASE READ: If you like my work and want to give me a little motivation, please consider donating regularly: https://donate.sury.org/

WARNING: add-apt-repository is broken with non-UTF-8 locales, see
https://github.com/oerdnj/deb.sury.org/issues/56 for workaround:

# LC_ALL=C.UTF-8 add-apt-repository ppa:ondrej/php
More info: https://launchpad.net/~ondrej/+archive/ubuntu/php
Adding repository.
Found existing deb entry in /etc/apt/sources.list.d/ondrej-ubuntu-php-oracular.sources
Hit:1 https://repos-droplet.digitalocean.com/apt/droplet-agent main InRelease
Hit:2 https://repos.insights.digitalocean.com/apt/do-agent main InRelease                                                                                  
Hit:3 http://mirrors.digitalocean.com/ubuntu oracular InRelease                                                                                            
Hit:4 http://mirrors.digitalocean.com/ubuntu oracular-updates InRelease                                                              
Hit:5 http://mirrors.digitalocean.com/ubuntu oracular-backports InRelease                              
Hit:6 http://security.ubuntu.com/ubuntu oracular-security InRelease 
Ign:7 https://ppa.launchpadcontent.net/ondrej/php/ubuntu oracular InRelease
Err:8 https://ppa.launchpadcontent.net/ondrej/php/ubuntu oracular Release
  404  Not Found [IP: 185.125.190.80 443]
Reading package lists... Done
E: The repository 'https://ppa.launchpadcontent.net/ondrej/php/ubuntu oracular Release' does not have a Release file.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# sudo apt update
Hit:1 https://repos-droplet.digitalocean.com/apt/droplet-agent main InRelease
Hit:2 https://repos.insights.digitalocean.com/apt/do-agent main InRelease                                                                                    
Hit:3 http://mirrors.digitalocean.com/ubuntu oracular InRelease                                                                                              
Hit:4 http://security.ubuntu.com/ubuntu oracular-security InRelease                                    
Hit:5 http://mirrors.digitalocean.com/ubuntu oracular-updates InRelease                                
Hit:6 http://mirrors.digitalocean.com/ubuntu oracular-backports InRelease
Ign:7 https://ppa.launchpadcontent.net/ondrej/php/ubuntu oracular InRelease
Err:8 https://ppa.launchpadcontent.net/ondrej/php/ubuntu oracular Release
  404  Not Found [IP: 185.125.190.80 443]
Error: The repository 'https://ppa.launchpadcontent.net/ondrej/php/ubuntu oracular Release' does not have a Release file.
Notice: Updating from such a repository can't be done securely, and is therefore disabled by default.
Notice: See apt-secure(8) manpage for repository creation and user configuration details.
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# sudo apt update^C
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# lsb_release -c
Codename:	oracular
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# sudo nano /etc/apt/sources.list.d/ondrej-ubuntu-php-*.list
root@ubuntu-finalproject:~/laravel-crm/laravel-crm# 

