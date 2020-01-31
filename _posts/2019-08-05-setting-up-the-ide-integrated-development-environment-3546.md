---
title: Setting up the IDE (Integrated Development Environment)
date: '2019-08-05T10:00:30.244Z'
excerpt: ''
thumb_img_path: null
comments_count: 0
positive_reactions_count: 7
tags:
  - beginners
  - tutorial
  - servers
  - ide
canonical_url: >-
  https://dev.to/th3n00bc0d3r/setting-up-the-ide-integrated-development-environment-3546
layout: post
---
Great Guys, so we finally have a clean bloatware free windows at our disposal, let get into setting up the basic development environment, therefore necessitating our needs. First and foremost, we want is JAVA. Now getting it from Oracle.com, they have added some sign up first and then they give the link. It's just bogus, so I found another place where you can directly download it, although if you want to go through the hassle you can go to oracle.com. I will be sticking to JDK8, because i find it just adjusts better with most applications we use later on.

**Java Development Kit 64-bit **8 Update 181 \
[https://filehippo.com/download_java_development_kit_64/86378/](https://filehippo.com/download_java_development_kit_64/86378/)

Download and install it.

![](https://i.ibb.co/qMWm08t/Screenshot-71.png)

![](https://i.ibb.co/fHKbkhG/Screenshot-72.png)

![](https://i.ibb.co/CHWxcL0/Screenshot-73.png)

![](https://i.ibb.co/RjXq9yw/Screenshot-74.png)

Now we are going to install an editor, i personally recommend visual studio code.

[https://code.visualstudio.com/](https://code.visualstudio.com/)

Download and install it.

![](https://i.ibb.co/zZjnLRf/Screenshot-75.png)

![](https://i.ibb.co/cJstZzp/Screenshot-76.png)

![](https://i.ibb.co/y5FRXSH/Screenshot-77.png)

![](https://i.ibb.co/n6RvL0T/Screenshot-78.png)

![](https://i.ibb.co/FsmHNt2/Screenshot-79.png)

![](https://i.ibb.co/pwH8D5C/Screenshot-80.png)

Once you have installed it, run it, lets customize it a bit. The first screen that you come up with is the welcome screen with the dark mode. A lot of people do like it, but I have always had a liking the white background, so I will be changing the theme.

Click on File → Preferences → Color Theme

Shortcut: Ctrl + K

![](https://i.ibb.co/mbNGDzr/Screenshot-81.png)

![](https://i.ibb.co/gm9Ct0x/Screenshot-82.png)

Now from the dropdown list, select Light + , remember the plus else you wont get the fancy highlighting. 

Next we will install some extensions which are a must. Click on the Box withing a Box icon on the left hand side, this is where all extensions are installed for vscode.

![](https://i.ibb.co/CVjGtYK/Screenshot-83.png)

Now search for Notepad, and click on Notepad++ keymap and Install. Now i came from Notepad++ a great editor of its time, and i am really used to its keymapping which really helps me accelerate my work. 

Ex. 

Duplicate Line: Ctrl + D

MultiLine Select Mode: Alt + Shift + Arrow Down

And much more…

![](https://i.ibb.co/3RHLcf2/Screenshot-84.png)

![](https://i.ibb.co/p0wp8PB/Screenshot-85.png)

Next Search for Beautify and install it, another great tool for making your code more cleaner to read and eventually debug if something wrong happens. The thing I found with most people is that if you keep your code clean you can easily find and fix bugs but a bad graphical version of the code is really hard to fix.

Now we are going to install Node. Yes Node. 

Direct Link

[https://nodejs.org/dist/v10.16.1/node-v10.16.1-x64.msi](https://nodejs.org/dist/v10.16.1/node-v10.16.1-x64.msi)

Now start the installation and check all the boxes, we want the documentation shortcuts and important Add to Path, else it won't be available globally.

![](https://i.ibb.co/7ySTTMd/Screenshot-86.png)

![](https://i.ibb.co/NVrLjFZ/Screenshot-87.png)

![](https://i.ibb.co/txy7p5G/Screenshot-88.png)

![](https://i.ibb.co/Tt440VG/Screenshot-89.png)

Next we need is Git for windows.

Direct Link

[https://git-scm.com/download/win](https://git-scm.com/download/win)

Follow the installer and check box all as you see in the screen.

![](https://i.ibb.co/7KyrTb8/Screenshot-90.png)

![](https://i.ibb.co/9ng71fF/Screenshot-91.png)

![](https://i.ibb.co/XkZg1gV/Screenshot-92.png)

![](https://i.ibb.co/SsBC03r/Screenshot-93.png)

Next we need to set visual studio code as GITs default editor, so select drop and select the Use Visual Studio Code as Gits default editor.

![](https://i.ibb.co/MgNPTQ0/Screenshot-94.png)

![](https://i.ibb.co/BsbC5qV/Screenshot-95.png)

Everything else is the thumb rule with installers, Next, Next Next, Finish.

Now lets test if all is good. Go to start Programs → Windows System → Command Prompt

![](https://i.ibb.co/6gzZjy1/Screenshot-96.png)

c:\>git

![](https://i.ibb.co/7zmk776/Screenshot-97.png)

And it should show you its documentation, you should go through it.

Next type in the following;

c:\>node -v

Shows the node version

c:\>npm -v

Shows the npm version

![](https://i.ibb.co/wNWM4VM/Screenshot-98.png)

Next we need to make our computer a temporary webserver, so we are going to install the famous Wamp Server. Now wamps server is sometimes a pain in the you know what, so to fix that we need some runtime libraries from windows to get that running. Download each of the following and install them. I have included all the libraries in this git link. Some you will have some will just install, so dont worry.

[https://github.com/th3n00bc0d3r/wamp-vcruntime-installers](https://github.com/th3n00bc0d3r/wamp-vcruntime-installers)

![](https://i.ibb.co/WfHq5QV/Screenshot-103.png)

![](https://i.ibb.co/Nt8n1f4/Screenshot-104.png)

Next we download wamp server

[https://sourceforge.net/projects/wampserver/files/WampServer%203/WampServer%203.0.0/wampserver3.1.9_x64.exe/download](https://sourceforge.net/projects/wampserver/files/WampServer%203/WampServer%203.0.0/wampserver3.1.9_x64.exe/download)

![](https://i.ibb.co/Y2wz6gq/Screenshot-99.png)

![](https://i.ibb.co/w0G2Jwb/Screenshot-105.png)

Ok, now lets start the installer and move on with it.

![](https://i.ibb.co/JjSXr3k/Screenshot-114.png)

Yes, we will keep it in c:\wamp64

![](https://i.ibb.co/wWbzZcS/Screenshot-115.png)

![](https://i.ibb.co/ZJhHwH9/Screenshot-116.png)

It will ask for default browser you can specify chrome, i just like to hurry up with it so just click open.

Ok, now double click and run the WAMP icon and lets start the server. Now once you start it you might see an orange icon, don't worry, lets try to fix it. Left click in the icon and a menu will appear, use that menu to go to Apache → Service administration → and click on Install service. If it pops some issue, click on stop service and then Install Service  A command prompt will pop up, you just have to press enter to continue. 

![](https://i.ibb.co/QX4PxGP/Screenshot-120.png)

![](https://i.ibb.co/s59N223/Screenshot-121.png)

![](https://i.ibb.co/TBdrW4d/Screenshot-122.png)

Next we are going to select the icon again but this time, right click it and in the wamp settings click on Allow MySQL. This will disable MySQL for we are going to be using MariaDB. 

Now click on the click and go to MariaDB and click on test port 3306. It should show a command prompt stating that 3306 is not in use. We are good to go.

![](https://i.ibb.co/gRRg0m7/Screenshot-124.png)

![](https://i.ibb.co/q7DMH30/Screenshot-125.png)

Now click on the menu again and in MariaDB click on Use a port other than 3307 and set it to 3306. These are basically the default values on which all other things are set at , once set to default everything works like butter.

![](https://i.ibb.co/dWVfQCJ/Screenshot-126.png)

![](https://i.ibb.co/9sH1L0J/Screenshot-127.png)

Now if you open up a browser [http://localhost/](http://localhost/) you will be greeted by the page, the server is running. 

![](https://i.ibb.co/QMPHVDG/Screenshot-129.png)

Another thing we will be downloading is the MySQL Workbench, all time favs, 

[https://dev.mysql.com/downloads/windows/installer/8.0.html](https://dev.mysql.com/downloads/windows/installer/8.0.html)

Go to the link and click Download.Run and install using the installer.

![](https://i.ibb.co/5hGZ1J4/Screenshot-106.png)

![](https://i.ibb.co/RTdW7SR/Screenshot-107.png)

![](https://i.ibb.co/rvX8vhx/Screenshot-108.png)

## We are all don't here. Great Jobs Guys.
# Windows is Ready to Code!


[Noob Index](https://dev.to/th3n00bc0d3r/noob-guides-index-4mne)


*[This post is also available on DEV.](https://dev.to/th3n00bc0d3r/setting-up-the-ide-integrated-development-environment-3546)*


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
