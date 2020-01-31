---
title: 'Contrib: Using Nodemailer with Express and Templating'
date: '2019-08-05T05:00:49.646Z'
excerpt: ''
thumb_img_path: >-
  https://res.cloudinary.com/practicaldev/image/fetch/s--a6A4ufhp--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://res.cloudinary.com/practicaldev/image/fetch/s--ERHgt_V1--/c_imagga_scale%2Cf_auto%2Cfl_progressive%2Ch_420%2Cq_auto%2Cw_1000/https://thepracticaldev.s3.amazonaws.com/i/6d56qwuou3egvbrzgmco.jpg
comments_count: 2
positive_reactions_count: 3
tags:
  - node
  - javascript
  - tutorial
canonical_url: >-
  https://dev.to/th3n00bc0d3r/contrib-using-nodemailer-with-express-and-templating-3o68
layout: post
---
Hello Viewer, 

I recently stumbled upon a user of dev.to, who wanted help in getting nodemailer to work with express. As a beginner sometimes all that documentation is a bit confusing and you only need that is required to get the thing going, so i thought i{% raw %}`d share this with you guys. I made a little github, hope it is helpful.

## Required
* Node and NPM
* Email Account with SMTP

[Github: https://github.com/th3n00bc0d3r/Nodemailer-Express-Node](https://github.com/th3n00bc0d3r/Nodemailer-Express-Node)

From Command Line

```{% endraw %}
git clone https://github.com/th3n00bc0d3r/Nodemailer-Express-Node
cd Nodemailer-Express-Node
npm install
open app.js in your Editor and change smtp settings

node app.js
{% raw %}```{% endraw %}

You will need to initiate a GET Call to http://localhost:3000/send/mail or just open it in the browser that should work as well.


*[This post is also available on DEV.](https://dev.to/th3n00bc0d3r/contrib-using-nodemailer-with-express-and-templating-3o68)*


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
