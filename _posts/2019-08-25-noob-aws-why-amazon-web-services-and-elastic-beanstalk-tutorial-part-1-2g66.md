---
title: 'Noob AWS: Why Amazon Web Services and Elastic Beanstalk Tutorial - Part 1'
date: '2019-08-25T21:18:14.079Z'
excerpt: ''
thumb_img_path: >-
  https://res.cloudinary.com/practicaldev/image/fetch/s--Q5QqeJON--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://res.cloudinary.com/practicaldev/image/fetch/s--htqRuI8G--/c_imagga_scale%2Cf_auto%2Cfl_progressive%2Ch_420%2Cq_auto%2Cw_1000/https://thepracticaldev.s3.amazonaws.com/i/47rjqr99qlg0ysdmkc7w.jpg
comments_count: 0
positive_reactions_count: 9
tags:
  - beginners
  - tutorial
  - aws
  - javascript
canonical_url: >-
  https://dev.to/th3n00bc0d3r/noob-aws-why-amazon-web-services-and-elastic-beanstalk-tutorial-part-1-2g66
layout: post
---
## What is Amazon Web Services?
AWS (Amazon Web Services) is a collection of a set number of computers spread around the world. The set number of computers in a fixed area can be called a data center. The data center is connected through high speed internet that allows each data center to contribute its resource mainly space, ram and computing power to a single point that we call Amazon Web Services. This AWS further distributes these resources as per required capacity to its users who are you and me. 

## What was I doing before I discovered AWS?
I was managing servers. I was developing applications, deploying applications and then day/night managing servers. Its been 5 years, i have been going through the headache of managing it. I once remember a setup for one of my client, where I took 3 servers from different locations and using the WHM/Cpanel Cloud connecting them through IPs, was a real relief in knowing. I think it was 2-3 years back.

## Why AWS Now?
I have been working on two of my projects, one that i deployed about 4 years back, it was never able to persist and not because of the deployment, it was the damn server, that always used to run out. It cost me a project, was a beautiful one, but a loss, so what do you do when things go like that, you follow a concept known as insanity. As someone said, "Insanity is the process of repeating something again and again and expecting a different result". Well I disagree to it, i think insanity is obsession, abyss to all the failures, one should never give up, so AWS has given me that new hope which i want to share.

### 3 Things to Know about AWS
* EC2 - This is the Compute and RAM of your setup
* S3 - This is the Hard drive or storage of your setup
* Route53 - This is the Domain Management System
* RDS - This is the Database of your System

## What will AWS Do for me?
It will take the headache for me to stabilize the environment, it will give me a stable environment and all i need to do is work on my application. It will handle all the traffic issues as it will autoscale based on my traffic, it will charge me based on my usage and not fixate me to monthly retention. 

## What about alternatives to AWS?
Yes, there is google cloud and ali baba cloud but I think AWS has the market lead with have more than 1400+ services by start of 2019. Now these services are a mix and match of their basic service, providing usability based on a different use cases and it is likely you will fall in one.

## What service I want to share, and what does it do?
Its called __Elastic Beanstalk__. EB is 1-2-3 deployment for my node projects. It also supports PHP, Ruby and .NEt. I just have to upload my code using a command line tool and amazingly after all the setup, its just one line and it handles the rest. It restarts my machine, gets my modules and makes sure it serves to my links aka APIs. In the meanwhile, I do have full control of the environment to make further tweaks.

# Lets Start

## Create a NOOB Node API Project

Create a Directory and Initialize a Package.json in it. 
![](https://i.ibb.co/kK6QR3B/Image-001.png)

Lets install a couple of Modules we will be using

{% raw %}```
npm i -S express express mysql body-parser
```{% endraw %}

* ExpressJS - A framework we will use for our API Building Process
* MySQL - A module driver to connect to MySQL
* Body Parser - Help us send data to our API Post Calls

Next create an app.js file within the project.

{% raw %}```
const express       = require('express')
const bodyParser    = require('body-parser');
const app           = express()
const port          = 3000

app.get('/', (req, res) => {
    res.send("Welcome to the Noob API");
});

app.get('/test', (req, res) => {
    var response = {
        "success": true,
        "message": "Welcome to Mars"
    }
    res.json(response);
});

app.listen(port, function() {
    console.log("Listening to " + port);
});
```{% endraw %}

Now to run the project simple type
{% raw %}```
node app.js
```{% endraw %}

It should start listening to port 3000, and now if you open the browser and type in http://localhost:3000/ you should have a simpler output

![](https://i.ibb.co/WvT9ZX0/Image-002.png)

__WE HAVE A WORKING NOOB API__

## Lets get this over to AWS

First of all, we need the AWS Command Line tool and then we need the Elastic Beanstalk Command Line tool. 

__Installing AWS CLI__
Now windows has an installer.
[https://s3.amazonaws.com/aws-cli/AWSCLISetup.exe](https://s3.amazonaws.com/aws-cli/AWSCLISetup.exe)

![](https://i.ibb.co/Dz7B6mZ/Image-003.png)

And for Linux and MacOS, you can refer to this, if you dont get it, let me know, i{% raw %}`ll help you with it. It uses PIP, its just a package manager.
[https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html][https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html]

Once installed, you can confirm as follows;
![](https://i.ibb.co/Fwf9LH9/Image-004.png)

__Installing EB CLI__

Install Python
[https://www.python.org/ftp/python/3.7.4/python-3.7.4.exe](https://www.python.org/ftp/python/3.7.4/python-3.7.4.exe)

Remember to Check Add to Path

![](https://i.ibb.co/Zfs5vR6/Image-006.png)

[https://github.com/aws/aws-elastic-beanstalk-cli-setup](https://github.com/aws/aws-elastic-beanstalk-cli-setup)


We should now have PIP in the Command Prompt, We install virtualenv, pyenv

```{% endraw %}
pip install virtualenv

git clone https://github.com/pyenv/pyenv.git ~/.pyenv
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bash_profile
echo 'export PATH="$PYENV_ROOT/libexec:$PATH"' >> ~/.bash_profile
echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.bash_profile
{% raw %}```

Install CYGWIN and Install it in FULL
[https://cygwin.com/setup-x86_64.exe](https://cygwin.com/setup-x86_64.exe)



Now goto the aws-elastic-beanstalk-cli-setup/scripts/

```{% endraw %}
python ebcli_installer.py
{% raw %}```

Now open Run from Windows and Paste this replacing your username
```{% endraw %}
 cmd.exe /c "C:\Users\<YOURUSERNAME>\.ebcli-virtual-env\executables\path_exporter.bat"
{% raw %}```{% endraw %}

Restart Computer. HIGHLY RECOMMENDED

Then open terminal and type __eb --version__

![](https://i.ibb.co/sH9gBdy/Image-007.png)


## LETS GO TO AWS 

You should now register an account with AWS. Then login to the following link
[https://aws.amazon.com/console/](https://aws.amazon.com/console/)

![](https://i.ibb.co/DQySQMz/Image-008.png)

Welcome to the AWS Console and Dont Worry.

![](https://i.ibb.co/NxxNDsh/Image-009.png)


Type in IAM (Identity Access Management)

![](https://i.ibb.co/9nKmwZ2/Image-011.png)

We need to create a user and connect it to our CLI, so we can access the AWS Cloud functions in our Command Line.

Click on User and Then Click on Add User

![](https://i.ibb.co/mT1ny95/Image-012.png)
![](https://i.ibb.co/vkfp8Fd/Image-013.png)

I am going to name my user __win_cli__ and will only give it programmatic access. Click Next, lower bottom right of the screen

![](https://i.ibb.co/TcXbQYx/Image-014.png)

Next, Click on Attach Existing Policies Directory and Check Administrative Access. Then Click Next Tags

![](https://i.ibb.co/HpfhjK2/Image-015.png)

Tagging is a Good way, but i am not using it now, so leave it blank and click next, now you should have a review of you settings. 

![](https://i.ibb.co/7Nqt4Qv/Image-016.png)

Click the Create User Button Now

![](https://i.ibb.co/s9KnKW1/Image-017.png)

Great, now copy your __Access key ID__ and __Secret access key__ . This is used to connect from the CLI to the Cloud of AWS. Now lets go back to the Command Prompt and type as follows;

![](https://i.ibb.co/w4YX7Cx/Image-018.png)

Now to check it, type __aws s3 ls__ in the command prompt and it shouldnt through any error.

![](https://i.ibb.co/ftPtH21/Image-019.png)

# PART 2 COMING REALLY REALLY SOON

*[This post is also available on DEV.](https://dev.to/th3n00bc0d3r/noob-aws-why-amazon-web-services-and-elastic-beanstalk-tutorial-part-1-2g66)*


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
