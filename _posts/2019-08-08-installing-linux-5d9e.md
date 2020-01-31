---
title: Installing Linux
date: '2019-08-08T10:48:36.564Z'
excerpt: ''
thumb_img_path: >-
  https://res.cloudinary.com/practicaldev/image/fetch/s--31eikhE0--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://res.cloudinary.com/practicaldev/image/fetch/s--FYYoJMUd--/c_imagga_scale%2Cf_auto%2Cfl_progressive%2Ch_420%2Cq_auto%2Cw_1000/https://thepracticaldev.s3.amazonaws.com/i/tm4q7g5s7c4r4rcsg13w.jpg
comments_count: 0
positive_reactions_count: 7
tags:
  - tutorial
  - beginners
  - ubuntu
  - linux
canonical_url: 'https://dev.to/th3n00bc0d3r/installing-linux-5d9e'
layout: post
---
Great Guyz, let's get ready to enjoy what linux is really. I specifically chose PopOS by System76, after experimenting installs of up to 8 Distributions. The purpose was to select a distribution, that would underlay the minimal of the simplest principles upon which the concepts can be made on because once you simplify things, possibilities start to spin up.

Put in that USB of Linux, restart your computer or turn it on and start pressing F12 or F8 in some cases to bring about the boot menu. Once the boot menu is there, select your USB.

![](https://i.ibb.co/bKFV2Zh/IMG-20190807-102903.jpg)

Now you will be brought upon a screen, lets press enter and Try or Install Pop_OS.

![](https://i.ibb.co/sWhvjDd/IMG-20190807-102911.jpg)

Now that fancy prodev text starts running down, its called a terminal.

![](https://i.ibb.co/KW9h07B/IMG-20190807-102915.jpg)

You will be taken directly to the Desktop, let select English and Press Select.

![](https://i.ibb.co/K9yPDWD/IMG-20190807-102932.jpg)

You can select the language over here.

![](https://i.ibb.co/VBcLDCc/IMG-20190807-102943.jpg)

Then the keyboard layout.

![](https://i.ibb.co/B2rBYRj/IMG-20190807-102950.jpg)

![](https://i.ibb.co/FKmfwGg/IMG-20190807-103005.jpg)

Now the default keyboard layout screen 2.

Ok, now comes the fun part, we are going to go advanced on the install section, and partition our own operating system scheme. Select Custom (Advanced).

![](https://i.ibb.co/QKRWmF7/IMG-20190807-103012.jpg)

Now look at all those fancy colors, click on modify partitions.

![](https://i.ibb.co/PFfTsKk/IMG-20190807-103023.jpg)

As we installed windows before, so we will make this dual boot, therefore you should have a greyed on area on the upper right. Click on the Unallocated Partition.

![](https://i.ibb.co/GvNCVsf/IMG-20190807-103109.jpg)

Now click that Black Document icon on the upper left.

![](https://i.ibb.co/SwJDJHH/IMG-20190807-103123.jpg)

Type in 1000 in the New Size (MiB) and name it Boot. Then Click Add

![](https://i.ibb.co/5kBkVZ8/IMG-20190807-103513.jpg)

Now click on the Unallocated Partition once again, and click on the New Blank Document Icon. Now type in 2000 in the New Size (MiB) and name it Swap also from the File System Dropdown, select linux-swap. Click Add

![](https://i.ibb.co/N39fX8h/IMG-20190807-103534.jpg)

Now this is the last one, repeat the process and dont change anything leave to whatever amount is the New Size (MiB), name is Root and set the File System to ext4. Click Add

![](https://i.ibb.co/NSmt9JS/IMG-20190807-103621.jpg)

It should be something similar to what you see now. Now click the Green Tick to Apply all operations.

![](https://i.ibb.co/h16YQp5/IMG-20190807-103629.jpg)

You should be back to the colorful strip, and it should be something like this.

Now click on the First Green Bar, and select Use Partition, and set it to Use as Boot (/boot/efi).

![](https://i.ibb.co/fF26KD9/IMG-20190807-103651.jpg)

Select the Orangish Red right next to it, and select Use Partition and set it to Use as: Swap.

![](https://i.ibb.co/vcbbGPg/IMG-20190807-103959.jpg)

Now select the last big green bar, select Use Partition, Format and Use as: Root (/).

![](https://i.ibb.co/GMmJdG3/IMG-20190807-104005.jpg)

Once you do that you will have check marks and the Erase and Install button will lit up.

![](https://i.ibb.co/Yp5Jm2D/IMG-20190807-104023.jpg)

![](https://i.ibb.co/Js1Tc7T/IMG-20190807-104033.jpg)

Short Summary of Linux Partition Scheme



*   Boot Partition: Mounted as: /boot/efi - Used to place the bootloader which helps in loading the operating system.
*   Swap Partition: Mounted as: linux-swap - Used to increase the amount of virtual memory available to a host if ram runs out.
*   Root Partition: Mounted as (/) - Used just like C Drive on windows, stores all the operating system files.

Now sit back and get yourself a coffee, although this is going to be really quick.

![](https://i.ibb.co/7byYRT9/IMG-20190807-104038.jpg)

Ok, now plug out the USB and click on Restart Device.

![](https://i.ibb.co/mH4gtYD/IMG-20190807-104419.jpg)

Great Giuyz, at this stage, your not noobs anymore. Rejoice for the happiness shall stay with your forever.

[Next: Setting up the IDE for Linux](https://dev.to/th3n00bc0d3r/setting-up-the-ide-integrated-development-environment-51lc)

[Noob Index](https://dev.to/th3n00bc0d3r/noob-guides-index-4mne)



*[This post is also available on DEV.](https://dev.to/th3n00bc0d3r/installing-linux-5d9e)*


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
