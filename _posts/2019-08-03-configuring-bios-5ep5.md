---
title: Configuring BIOS
date: '2019-08-03T05:50:26.707Z'
excerpt: ''
thumb_img_path: null
comments_count: 0
positive_reactions_count: 5
tags:
  - tutorial
  - beginners
canonical_url: 'https://dev.to/th3n00bc0d3r/configuring-bios-5ep5'
layout: post
---
Great, now we have a USB, that has a windows installer on it. Now this is the part, I support in my experience where people are most scared of, which i think they shouldn't be.

“Man always fears, that which it does not understand””

So, you just understand it, i think we are way better than apes in intelligence. Now you need to completely shutdown your laptop or computer. All manufacturers have sort of the same and different way of going into bios. You should try one of the following after turning on the computer;

*   Press DEL button repeatedly on your Keyboard when your power On
*   Press F2 repeatedly  On your Keyboard when your power On
*   Press TAB on your Keyboard when your power On
*   Sony Laptops have an ASSIST RED Button but Press that when computer is completely powered off.

I was welcomed with a Boot Menu Like this, it will be different for you guys but similar in many ways. We just need to go to BIOS Setup

![](https://thepracticaldev.s3.amazonaws.com/i/7tt2q84z9ikdtlf81d96.jpg)

So this is like a BIOS setup screen, that you should be welcomed.

![](https://thepracticaldev.s3.amazonaws.com/i/m0eit3xs2cfcm7e6icig.jpg)

Now, got to the Exit menu first, highly recommended, and for this Computer it has Get Default Values, for some it will be Load Setup Defaults. I think you should start with a clean factory reset, just select that option. Once select go back to the Main Tab.

![](https://thepracticaldev.s3.amazonaws.com/i/aqi6v3s137g87s5zkmqe.jpg)

Now we go in to the Advanced Menu for this BIO and in some it will be Configuration TAB and enable Intel(R) Virtualization Technology or Intel Virtual Technology, in some computers it will be in the CPU management tab, I say just Explorer it. This option is used for virtualization which we will be using when we get to the coding part of the tutorial.

![](https://thepracticaldev.s3.amazonaws.com/i/uqpv6jt9pz7ovtfulnyn.jpg)

Now try to FIND either in Hard Drive or something, where it says, SATA Controller Mode, make sure it should be set to AHCI, and NOT ATA, RTSR or some RAID 0.

![](https://thepracticaldev.s3.amazonaws.com/i/gecochpwwt55viiq49h4.jpg)

There should be some Security settings in the BIOS, i like to disable Secure Boot, makes it kinda faster.

![](https://thepracticaldev.s3.amazonaws.com/i/hukvk5ayt3e7g21qyjbb.jpg)

Now either in the Boot Menu, make sure External Device boot is enabled, here it is USB Boot so that we can boot the windows installer from the USB, or else it wont allow to boot from USB.

![](https://thepracticaldev.s3.amazonaws.com/i/zkg9rc7r4r1l1i32i9pc.jpg)

And yes, the Boot Mode, so in some old computers, you might not find it don't worry, You will just make the Installer in MBR Mode, but in most now, Select UEFI. 

![](https://thepracticaldev.s3.amazonaws.com/i/zkg9rc7r4r1l1i32i9pc.jpg)

Now you can go into the Exit Tab, and Exit Saving Changes, before you do that

![](https://thepracticaldev.s3.amazonaws.com/i/7sb3h4spd1209tjjhkof.jpg)

Now, we sort of need the BOOT menu again, so perhaps in some its F12 on the Keyboard and in some its F8, either you will have an option or you will be directly sent into a boot menu.

![](https://thepracticaldev.s3.amazonaws.com/i/7tt2q84z9ikdtlf81d96.jpg)

Once you select that you will see your pretty USB with its device name, something like this in the menu to select. Select it and Lets Move On

![](https://thepracticaldev.s3.amazonaws.com/i/go3z1gptyoam63j9xg29.jpg)

[Next: Installing Windows](https://dev.to/th3n00bc0d3r/installing-windows-3837)

[Noob Index](https://dev.to/th3n00bc0d3r/noob-guides-index-4mne)

*[This post is also available on DEV.](https://dev.to/th3n00bc0d3r/configuring-bios-5ep5)*


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
