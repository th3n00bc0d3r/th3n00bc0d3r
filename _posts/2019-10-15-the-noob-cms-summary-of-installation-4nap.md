---
title: 'The Noob CMS: Summary of Installation'
date: '2019-10-15T13:11:43.361Z'
excerpt: ''
thumb_img_path: >-
  https://res.cloudinary.com/practicaldev/image/fetch/s--ddUpIzYs--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://res.cloudinary.com/practicaldev/image/fetch/s--RItxH-h1--/c_imagga_scale%2Cf_auto%2Cfl_progressive%2Ch_420%2Cq_auto%2Cw_1000/https://thepracticaldev.s3.amazonaws.com/i/w61bl5muzsmoyi0akhs3.png
comments_count: 0
positive_reactions_count: 4
tags:
  - noobcms
  - beginners
  - tutorial
canonical_url: 'https://dev.to/th3n00bc0d3r/the-noob-cms-summary-of-installation-4nap'
layout: post
---
This is a summary of Installation for all to continue where we left. 

### How to Install
- Download http://www.wampserver.com/en/ or any other supported PHP 7+ and Install
- Go to http://localhost/phpmyadmin/index.php and Login with default credentials
  - Username: root
  - Password: **Blank**
  - ![](https://i.ibb.co/gm8VGDz/Image-067.png)
- Once logged in, Click on **Database** and then Create a New Database by the name of noob_db
  - ![](https://i.ibb.co/znXDWfR/Image-001.png)
- Now goto Import and click on Choose File and Select ./repo/db/noob_cms.sql.gz and Scroll down and click on Go
- You should successfully have imported the DB
  - ![](https://i.ibb.co/YW16psr/Image-002.png)
- Take your Favorite Editor and open ./repo/config/config.php and make sure the configuration matches
  - ![](https://i.ibb.co/VDMYBN6/Image-003.png)


<iframe class="liquidTag" src="https://dev.to/embed/github?args=th3n00bc0d3r%2Fnoobcms" style="border: 0; width: 100%;"></iframe>


[Noob Index](https://dev.to/th3n00bc0d3r/noob-guides-index-4mne)


*[This post is also available on DEV.](https://dev.to/th3n00bc0d3r/the-noob-cms-summary-of-installation-4nap)*


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
