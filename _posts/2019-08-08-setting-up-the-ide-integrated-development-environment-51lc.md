---
title: Setting up the IDE (Integrated Development Environment)
date: '2019-08-08T22:23:16.153Z'
excerpt: ''
thumb_img_path: >-
  https://res.cloudinary.com/practicaldev/image/fetch/s--pQNJ5tkB--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://res.cloudinary.com/practicaldev/image/fetch/s--gBJ5mPfj--/c_imagga_scale%2Cf_auto%2Cfl_progressive%2Ch_420%2Cq_auto%2Cw_1000/https://thepracticaldev.s3.amazonaws.com/i/m2freqpn96ttbus51zm0.jpg
comments_count: 8
positive_reactions_count: 4
tags:
  - linux
  - ubuntu
  - beginners
  - tutorial
canonical_url: >-
  https://dev.to/th3n00bc0d3r/setting-up-the-ide-integrated-development-environment-51lc
layout: post
---
Welcome to Linux, let's start making this environment work for us, and make us do miracles. So on the upper right corner of the screen click the taskbar and connect to the internet. 

![](https://i.ibb.co/hXjBZn2/lin-0001-Screenshot-from-2019-08-09-01-21-49-png.jpg)

Next click on activities on the upper left, and you have firefox, but we need chrome, so open firefox and go to.[https://www.google.com/chrome/](https://www.google.com/chrome/) and click on Download Chrome.

![](https://i.ibb.co/Z63Z8qD/lin-0002-Screenshot-from-2019-08-09-01-22-26-png.jpg)

![](https://i.ibb.co/QryGCHp/lin-0003-Screenshot-from-2019-08-09-01-22-38-png.jpg)

![](https://i.ibb.co/VmGScQP/lin-0004-Screenshot-from-2019-08-09-01-22-43-png.jpg)

You will be given with an option to select the type of file, so we are on a Debian Based and the .deb file is just like an .exe file. Download it and Click on it and the installer will start.

![](https://i.ibb.co/LkNTB0J/lin-0005-Screenshot-from-2019-08-09-01-22-46-png.jpg)

![](https://i.ibb.co/M1g1wkt/lin-0006-Screenshot-from-2019-08-09-01-22-51-png.jpg)

![](https://i.ibb.co/RTSLbsX/lin-0007-Screenshot-from-2019-08-09-01-23-04-png.jpg)

Now Eddy will open which is an installer for all deb files, isn't it simple. Just click install and you have chrome.

![](https://i.ibb.co/g4td9xg/lin-0008-Screenshot-from-2019-08-09-01-23-12-png.jpg)

![](https://i.ibb.co/n0DbrMB/lin-0009-Screenshot-from-2019-08-09-01-23-49-png.jpg)

Next lets install visual studio code, so head to [https://code.visualstudio.com/download](https://code.visualstudio.com/download) and click on the .deb file and repeat the process.

![](https://i.ibb.co/FK716GG/lin-0010-Screenshot-from-2019-08-09-01-25-52-png.jpg)

Next we need MySQL Workbench, head over to [https://dev.mysql.com/downloads/workbench/](https://dev.mysql.com/downloads/workbench/) and from the dropdown select Ubuntu Linux.

![](https://i.ibb.co/tQmxncN/lin-0011-Screenshot-from-2019-08-09-01-26-37-png.jpg)

![](https://i.ibb.co/BBgtttt/lin-0012-Screenshot-from-2019-08-09-01-26-48-png.jpg)

Next select the Deb Package and click on download.

Yes, it asks to register, forget it, just click on No Thanks, just start my download.

![](https://i.ibb.co/VH0fhRS/lin-0013-Screenshot-from-2019-08-09-01-26-52-png.jpg)

![](https://i.ibb.co/zRMYzxF/lin-0014-Screenshot-from-2019-08-09-01-27-03-png.jpg)

Now you can click on Deb file and the installer will start, if you click on 2 files individually it queues up and you can multiple install files, how wonderful it is.

![](https://i.ibb.co/PwvWb5D/lin-0015-Screenshot-from-2019-08-09-01-27-12-png.jpg)

![](https://i.ibb.co/xqf7T9s/lin-0016-Screenshot-from-2019-08-09-01-27-42-png.jpg)

Now if you click on activities, and select the dotted icon, you can see we have the programs installed to us.

One last thing we need is a dependency, so use the following link and install the .deb file.

[https://packages.sury.org/php/pool/main/libz/libzip/libzip5-dbgsym_1.3.2-1%2B0~20180714172643.1%2Bstretch~1.gbp053542_amd64.deb](https://packages.sury.org/php/pool/main/libz/libzip/libzip5-dbgsym_1.3.2-1%2B0~20180714172643.1%2Bstretch~1.gbp053542_amd64.deb)

**Setting up a Local Server for Developer**

Now we are going to install a local web server with php and a database server for local development and testing. Right click on the desktop and click open in Terminal. We need to add in some remote repositories so that we can get the additional files for installation. In the terminal copy paste the following code, one by one.

![](https://i.ibb.co/qrDnMdy/lin-0017-Screenshot-from-2019-08-09-01-29-00-png.jpg)

{% raw %}```
sudo apt-get install software-properties-common

sudo add-apt-repository ppa:ondrej/php

sudo apt-get update
```{% endraw %}

![](https://i.ibb.co/mGbM1mp/lin-0021-Screenshot-from-2019-08-09-01-31-40-png.jpg)

Now the following command will install Nginx as the Webserver and PHP 7.3

sudo apt-get install nginx php7.3-fpm php7.3-cli php7.3-mysql php7.3-gd php7.3-imagick php7.3-recode php7.3-tidy php7.3-xmlrpc php7.3-common php7.3-curl php7.3-mbstring php7.3-xml php7.3-bcmath php7.3-bz2 php7.3-intl php7.3-json php7.3-readline php7.3-zip

Now lets see if all is good, use the following command to check. Open Chrome and goto [http://localhost/](http://localhost/) which is your own computer.

![](https://i.ibb.co/t4FhKCQ/lin-0023-Screenshot-from-2019-08-09-01-45-30-png.jpg)

Next lets test PHP, in the terminal type

{% raw %}```
sudo php -v
```{% endraw %}

![](https://i.ibb.co/nbvR065/lin-0024-Screenshot-from-2019-08-09-01-45-54-png.jpg)

Now we need to tweak Nginx a little so in the terminal type

{% raw %}```
sudo nano /etc/nginx/nginx.conf
```{% endraw %}

![](https://i.ibb.co/FBMntZR/lin-0025-Screenshot-from-2019-08-09-01-47-04-png.jpg)

Use arrows to move down to user and replace www-data with your username in my case it was darkside. Also set worker_processes to 1.

![](https://i.ibb.co/CBq5htH/lin-0026-Screenshot-from-2019-08-09-01-47-15-png.jpg)

![](https://i.ibb.co/tp7W8BB/lin-0027-Screenshot-from-2019-08-09-01-47-25-png.jpg)

Now to save press the Ctrl + O on your keyboard and press enter, then press Ctrl + X to exit.

Next we need to fix a couple of things in PHP so in terminal type

{% raw %}```
sudo nano /etc/php/7.3/fpm/pool.d/www.conf
```{% endraw %}

Now scroll down and in the user = www-data replace it www-data with your username, in my case it was darkside, do the same for group.

![](https://i.ibb.co/XCZJBxq/lin-0033-Screenshot-from-2019-08-09-01-52-37-png.jpg)

![](https://i.ibb.co/QDsYmtr/lin-0034-Screenshot-from-2019-08-09-01-52-59-png.jpg)

Scroll down a little more and you{% raw %}`ll find listen.owner and listen.group and set them to your username, in my case it is darkside. Now press Ctrl + O to save and then Ctrl + X to exit.

![](https://i.ibb.co/YP47gHq/lin-0035-Screenshot-from-2019-08-09-01-53-03-png.jpg)

Next type in the following;
```{% endraw %}
sudo nano /etc/nginx/sites-available/default
{% raw %}```


Scroll down a bit and add index.php to the index tag, also set server_name to localhost, as shown in the screen.

![](https://i.ibb.co/C2dRJ2G/lin-0029-Screenshot-from-2019-08-09-01-48-32-png.jpg)

Next scroll down a little and remove the # tag from the location ~\.php$ {, this is uncommenting the lines. Also from the include snippets and the fastcgi_pass. The fastcgi_pass is set to 7.0 so we need to set it to 7.3, just go to the end of the line and set it as follows

![](https://i.ibb.co/2yfXrZx/lin-0028-Screenshot-from-2019-08-09-01-48-24-png.jpg)

Fastcgi_pass unix://var/run/php/php7.3-fpm.sock

Also uncomment the braces (}) where it closes. Next press Ctrl + O to save and Ctrl +X to exit.

Now lets restart PHP and NGINX and test it before it.

```{% endraw %}
sudo nginx -t

sudo service nginx restart

sudo php-fpm7.3 -t 

sudo service php7.3-fpm restart
{% raw %}```

![](https://i.ibb.co/gMbsCYF/lin-0036-Screenshot-from-2019-08-09-01-53-27-png.jpg)

Run the next command to fix some permissions The $(whoami) variable will take the value of the user you are currently logged in.

```{% endraw %}
sudo chown -R $(whoami):$(whoami) /var/www/html/

sudo chmod -R 755 /var/www
{% raw %}```
Now lets create a quick shortcut to our desktop for the www directory we will be working. Type the following in terminal.

```{% endraw %}
sudo ln -s /var/www/ ~/Desktop/
{% raw %}```

![](https://i.ibb.co/6Fw486t/lin-0030-Screenshot-from-2019-08-09-01-49-57-png.jpg)

A folder will appear on the desktop, this is our web directory to work. Lets open it up.

Now from the activities, let open visual studio code and test a couple of things. Open it up and change the theme if you want to. Drag and drop the folder into visual studio code and remove the index.nginx-debian.html file.

![](https://i.ibb.co/vxKN4Sc/lin-0031-Screenshot-from-2019-08-09-01-50-06-png.jpg)

![](https://i.ibb.co/QJYBk1X/lin-0032-Screenshot-from-2019-08-09-01-50-50-png.jpg)

Create a new file index.html and type in anything. Now if you refresh the browser for [http://localhost/](http://localhost/) it will start displaying that.

Create a new file test.php and add the following code

```{% endraw %}
<?php phpinfo();?>
{% raw %}```

Now open [http://localhost/test.php](http://localhost/test.php) and you should have this screen, great php is all up and running.

![](https://i.ibb.co/tBmbLqc/lin-0037-Screenshot-from-2019-08-09-01-53-40-png.jpg)

Now we need the database server so we are going to install mariadb. Type the following in terminal.

```{% endraw %}
sudo apt-key adv --recv-keys --keyserver hkp://keyserver.ubuntu.com:80 0xF1656F24C74CD1D8
{% raw %}```

![](https://i.ibb.co/CBRYykJ/lin-0038-Screenshot-from-2019-08-09-01-54-14-png.jpg)

sudo nano /etc/apt/sources.list.d/mariadb.list

Paste the following
```{% endraw %}
# MariaDB 10.3 Repository

deb [arch=amd64,arm64,ppc64el] http://sfo1.mirrors.digitalocean.com/mariadb/repo/10.3/ubuntu bionic main

deb-src http://sfo1.mirrors.digitalocean.com/mariadb/repo/10.3/ubuntu bionic main

{% raw %}```

![](https://i.ibb.co/g4fXJ1c/lin-0039-Screenshot-from-2019-08-09-01-54-24-png.jpg)

Press Ctrl + O to save and Ctrl + X to exit.

Next type the following;

```{% endraw %}
sudo apt update

sudo apt install mariadb-server

{% raw %}```

Now the installation will start and you will be prompted somewhere in between with a password. Type in anything, i type noob. It will ask again retype it.

![](https://i.ibb.co/vDhFXL8/lin-0040-Screenshot-from-2019-08-09-01-56-38-png.jpg)

Once done, type the following to check the database server 

```{% endraw %}
sudo systmectl status mariadb

{% raw %}```

![](https://i.ibb.co/mtQXFfV/lin-0041-Screenshot-from-2019-08-09-01-57-42-png.jpg)

It should be active running in green. Good work! Pat yourself now. Now type the following command to connect to the database server

```{% endraw %}
mysql -u root -p

{% raw %}```{% endraw %}

![](https://i.ibb.co/hgcCXXb/lin-0042-Screenshot-from-2019-08-09-01-57-55-png.jpg)

![](https://i.ibb.co/C5j4gGV/lin-0043-Screenshot-from-2019-08-09-01-57-58-png.jpg)

Press Ctrl + C to exit.

Now open MySQL workbench and you can configure the settings there, by creating a New Connection by Clicking the Plus Sign. 

![](https://i.ibb.co/TR7hfv2/lin-0044-Screenshot-from-2019-08-09-01-59-15-png.jpg)

![](https://i.ibb.co/2yVF7nC/lin-0045-Screenshot-from-2019-08-09-01-59-22-png.jpg)

Click on Test Connection and input the password, in my case 

Username: root

Password: noob

![](https://i.ibb.co/JCMxQTK/lin-0046-Screenshot-from-2019-08-09-01-59-30-png.jpg)

Save the password in keychain and click Ok

Delete the Default connection, it sometimes gives errors.

![](https://i.ibb.co/djF0npM/lin-0047-Screenshot-from-2019-08-09-01-59-34-png.jpg)

Now double click it and check Don't show this again, and click on Continue anyway.

The last thing we would like to do, is also install a famous database tool by the name of phpmyadmin.  Open chrome and head over to [http://phpmyadmin.net/downloads/](http://phpmyadmin.net/downloads/) and click on Download 4.9. It will download a compressed file. 

Extract it to the www/html directory.

![](https://i.ibb.co/qr5wGfs/lin-0048-Screenshot-from-2019-08-09-02-00-29-png.jpg)

![](https://i.ibb.co/NnZtYb7/lin-0049-Screenshot-from-2019-08-09-02-00-35-png.jpg)

![](https://i.ibb.co/1qzg84R/lin-0050-Screenshot-from-2019-08-09-02-00-44-png.jpg)

![](https://i.ibb.co/bmKfL5P/lin-0051-Screenshot-from-2019-08-09-02-01-08-png.jpg)

Now rename is to phpmyadmin.

![](https://i.ibb.co/HKk8JB8/lin-0052-Screenshot-from-2019-08-09-02-01-16-png.jpg)

![](https://i.ibb.co/w0HXh6N/lin-0053-Screenshot-from-2019-08-09-02-01-28-png.jpg)

Now if you open [http://localhost/phpmyadmin](http://localhost/phpmyadmin) you should see this page, your database credentials will work over here.

![](https://i.ibb.co/ysDtHLn/lin-0054-Screenshot-from-2019-08-09-02-01-31-png.jpg)

Great guys! Cheers get yourself a Beer, Coffee, Tea and celebrate we have now a fully development environment setup for linux.

[Noob Index](https://dev.to/th3n00bc0d3r/noob-guides-index-4mne)


*[This post is also available on DEV.](https://dev.to/th3n00bc0d3r/setting-up-the-ide-integrated-development-environment-51lc)*


<script>
const parent = document.getElementsByTagName('head')[0];
const script = document.createElement('script');
script.type = 'text/javascript';
script.src = 'https://cdnjs.cloudflare.com/ajax/libs/iframe-resizer/4.1.1/iframeResizer.min.js';
script.charset = 'utf-8';
script.onload = function() {
    window.iFrameResize({}, '.liquidTag');
};
parent.appendChild(script);
</script>    
