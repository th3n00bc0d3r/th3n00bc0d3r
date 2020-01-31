---
title: 'The Noob CMS: Bootstrap 4'
date: '2019-08-15T10:20:31.549Z'
excerpt: ''
thumb_img_path: >-
  https://res.cloudinary.com/practicaldev/image/fetch/s--lzJeQEwz--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://res.cloudinary.com/practicaldev/image/fetch/s--rm0QvUMh--/c_imagga_scale%2Cf_auto%2Cfl_progressive%2Ch_420%2Cq_auto%2Cw_1000/https://thepracticaldev.s3.amazonaws.com/i/llbzofm4icoqed5um8tn.png
comments_count: 0
positive_reactions_count: 6
tags: []
canonical_url: 'https://dev.to/th3n00bc0d3r/the-noob-cms-bootstrap-4-43i5'
layout: post
---
## Question: What is a Boostrap?

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/9yfs1forg8qzc80ljtj7.png)

Bootstrap converts these type of ugly inputs and button to the flashy type of cool inputs and buttons, so that our website looks beautiful.

Bootstrap also helps to take care of all the calculations for styling our borders and frames of the websites, so when we open it on a mobile screen, it auto adjusts and we wont have to go through the hassle of managing it.

Thank You Bootstrap, We Love you for it. 

## How do I get it into our Website?

You can download bootstrap from the following link;
[https://getbootstrap.com/docs/4.3/getting-started/download/](https://getbootstrap.com/docs/4.3/getting-started/download/)

We can use a CDN, but for things to be understandable we are going to host boostrap on our server.


![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/pognkzjg662q02m8nme4.png)

You will have a file .zip

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/nlddfgfu5mxfvx4bnkee.png)

Now we need to copy the files form the bootstrap-4.3.1-dist.zip to our noob_cms folder.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/14hmisngu2is8p2w2tos.png)

This is what we should have in our noob_cms folder.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/h8so2m0r31e36dfrmzor.png)

## How Do I use it?
{% raw %}```
    <head>
        <meta charset="UTF-8">
        <title>Login</title>

        <link href="css/bootstrap.min.css" rel="stylesheet" />

    </head>


    <style>
        .myLoginForm label {
            margin-top: 10px;
        }

        .myLoginForm button {
            margin-top: 10px;
        }
    </style>

    <body>
        <div class="container">
            <div class="row">
                <div class="col-4 offset-4">
                    <form action="" method="POST" class="myLoginForm">
                        <label>Email Address</label>
                        <input class="form-control" name="email" type="text" placeholder="Enter Email Address..." />

                        <label>Password</label>
                        <input class="form-control" name="pass" type="password" placeholder="Password..." />

                        <button class="btn btn-success" name="btnLogin">Login</button>
                    </form>            
                </div>
            </div>
        </div>
    </body>
```{% endraw %}

So This code has just converted our old login form to the new login form

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/ow4mt341dgf775wyut6t.png)

I have Updated the New Code at the Git, please feel free to look at it

You can get the code from the following Git

<iframe class="liquidTag" src="https://dev.to/embed/github?args=th3n00bc0d3r%2Fnoobcms_login" style="border: 0; width: 100%;"></iframe>



[Noob Index](https://dev.to/th3n00bc0d3r/noob-guides-index-4mne)

*[This post is also available on DEV.](https://dev.to/th3n00bc0d3r/the-noob-cms-bootstrap-4-43i5)*


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
