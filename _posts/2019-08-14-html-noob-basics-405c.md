---
title: HTML Noob Basics
date: '2019-08-14T10:34:50.996Z'
excerpt: ''
thumb_img_path: >-
  https://res.cloudinary.com/practicaldev/image/fetch/s--YKT6gTUv--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://res.cloudinary.com/practicaldev/image/fetch/s--mWw6ztaU--/c_imagga_scale%2Cf_auto%2Cfl_progressive%2Ch_420%2Cq_auto%2Cw_1000/https://thepracticaldev.s3.amazonaws.com/i/02vcg74mnl3xbd1c1q7p.png
comments_count: 0
positive_reactions_count: 8
tags: []
canonical_url: 'https://dev.to/th3n00bc0d3r/html-noob-basics-405c'
layout: post
---
## What is HTML?
It is a language that is represented by **<>** tags. HTML is where we decide what to make bold, italic, justified paragraphs and images. 

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/rv6gh7mag3aux2kij2pa.png)

Lets put it into action, create a test.html file in the php_start directory that we have been following. Write the following piece of code.

{% raw %}```
<h1>Hello Noobs</h1>
```{% endraw %}
![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/krdngi5tpusg4m2xq9qx.png)

Now lets run the file, Great.

This is a heading tag, its starts with <h1> and ends with a forward slash </h1>

Now here is how a proper html file will start 

{% raw %}```
<!DOCTYPE html>
<html lang="en">
   <head>
     <title>Page Title</title>
   </head>

   <body>
      <h1>This is a Heading</h1>
      <p>This is a paragraph.</p>
      <p>This is another paragraph.</p>
   </body>
</html>
```{% endraw %}
* __<!DOCTYPE html>__ This defines that this is now HTML5 (It is a latest version of HTML)
* __<html lang="en">__ This defines that it is the base where we start the file, we have also defined the language in it. 
* __<head>__ This section is where we define the title add styles, add scripts and add the meta of the file where we get search engine optimized pages.
* __<body>__ This is where everything becomes beautiful, by styling that which we want to display.

Now lets see some more codes

{% raw %}```
//LINKS
<a href="url">link text</a>

//IMAGES
<img src="path/to/your/image.jpg" alt="title">

//LISTS
<ul>
  <li>Happy</li>
  <li>Still Happy</li>
  <li>Way Happy</li>
</ul>

//PARAGRAPHS
<p>This is the Noob World</p>

//EMBED YOUTUBE
<iframe width="500" height="500" src="https://www.youtube.com/watch?v=dT4A3rttrs8" />
```{% endraw %}
[Noob Index](https://dev.to/th3n00bc0d3r/noob-guides-index-4mne)


*[This post is also available on DEV.](https://dev.to/th3n00bc0d3r/html-noob-basics-405c)*


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
