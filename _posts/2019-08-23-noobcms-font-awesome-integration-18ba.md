---
title: 'NoobCMS: Font Awesome Integration'
date: '2019-08-23T13:58:57.797Z'
excerpt: ''
thumb_img_path: >-
  https://res.cloudinary.com/practicaldev/image/fetch/s--0O4fuy44--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://res.cloudinary.com/practicaldev/image/fetch/s--y-n4DqVm--/c_imagga_scale%2Cf_auto%2Cfl_progressive%2Ch_420%2Cq_auto%2Cw_1000/https://thepracticaldev.s3.amazonaws.com/i/6lsnixvu99a2eqxpb2s9.png
comments_count: 0
positive_reactions_count: 4
tags:
  - beginners
  - tutorial
  - noobcms
canonical_url: 'https://dev.to/th3n00bc0d3r/noobcms-font-awesome-integration-18ba'
layout: post
---
## What is Font Awesome?
Font awesome is a library of icons compiled to help you make integrate icons in your project very fast, easily and without a need to store or edit images. 

[http://www.fontawesome.com](http://www.fontawesome.com)

![Font Awesome Website](https://thepracticaldev.s3.amazonaws.com/i/98n1ae0g0c3nu1sbg9of.png)

Now once you register, you can only use 1 free kit to integrate, into your website which comes with 1500+ icons, so that does give you all what you need.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/mvonl940zd0to5s7gr24.png)

Now once you open the kit, you will have an integration URL, something like this.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/jujwi38sz4gkb2tm26sm.png)

We copy this URL and paste it into the HEAD tag of our login.php

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/ov7x20j1r1yiirn7um26.png)

Now lets get to font awesome icon and integrate an icon for our login button.

[https://fontawesome.com/icons?d=gallery](https://fontawesome.com/icons?d=gallery)

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/vxo3bpqqr6p60nsmqtk1.png)

Click on the __sign-in-alt__ icon

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/f01u8027e434seb7egjm.png)

Now you see the <i> tag, this is the code to call the icon. Paste it in between the button.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/et4ljg96ha3l1gcg7wd2.png)

Lets save and refresh our browser

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/l27qam78avz867l6z2wt.png)

We have an icon. Cheers... :)

[Noob Index](https://dev.to/th3n00bc0d3r/noob-guides-index-4mne)

*[This post is also available on DEV.](https://dev.to/th3n00bc0d3r/noobcms-font-awesome-integration-18ba)*


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
