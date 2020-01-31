---
title: Recovery and USB Boot
date: '2019-08-16T08:39:51.131Z'
excerpt: ''
thumb_img_path: >-
  https://res.cloudinary.com/practicaldev/image/fetch/s--WRp9cjQO--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://res.cloudinary.com/practicaldev/image/fetch/s--YwzyEoNp--/c_imagga_scale%2Cf_auto%2Cfl_progressive%2Ch_420%2Cq_auto%2Cw_1000/https://thepracticaldev.s3.amazonaws.com/i/g1wejq935kekkfbhoaoc.jpg
comments_count: 0
positive_reactions_count: 4
tags:
  - beginners
  - tutorial
canonical_url: 'https://dev.to/th3n00bc0d3r/recovery-and-usb-boot-2ck'
layout: post
---
Now we are going to clean install MacOS, therefore we need the image from Apple and then we will create a USB to boot from it.

Open App Store and Search for Mojave.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/n1c7f2u7znwsl2mpge2r.jpg)

Click Oo Get and it should start downloading it.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/l9f0hthqjuoeaa3jj6oe.jpg)

Mine, took me to the update section and started downloading the image.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/9vqdc9ysgto17w483lkk.jpg)

Once that is done, connect a USB to your Mac and Open Disk Utility.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/oyw867rijcb0hfs4sxk3.jpg)

Now select the USB and Click on Erase Partition and Name is USB

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/0lw2rnrhbaq66huvpx04.jpg)

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/xsw6tl2797fc25cwqa8b.jpg)

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/w4gtx78tmr2qx50tr492.jpg)

Next open Terminal and paste the Following Command

{% raw %}```
sudo /Applications/Install\ macOS\ Mojave.app/Contents/Resources/createinstallmedia --volume /Volumes/USB--nointeraction && say Mojave Drive Created
```{% endraw %}
![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/5u2fdozc3yu9vq7n8cw3.jpg)

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/pwlc3stakj81t8ekt0xj.jpg)

Once Complete You have the USB Ready.


*[This post is also available on DEV.](https://dev.to/th3n00bc0d3r/recovery-and-usb-boot-2ck)*


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
