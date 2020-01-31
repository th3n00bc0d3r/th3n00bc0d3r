---
title: Understanding Databases (Relational)
date: '2019-08-11T10:44:41.178Z'
excerpt: ''
thumb_img_path: >-
  https://res.cloudinary.com/practicaldev/image/fetch/s--CDjObBPL--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://res.cloudinary.com/practicaldev/image/fetch/s--MbATSXlL--/c_imagga_scale%2Cf_auto%2Cfl_progressive%2Ch_420%2Cq_auto%2Cw_1000/https://thepracticaldev.s3.amazonaws.com/i/21fobiu95ep5hioptj2h.png
comments_count: 0
positive_reactions_count: 13
tags:
  - sql
  - tutorial
  - beginners
canonical_url: 'https://dev.to/th3n00bc0d3r/understanding-databases-relational-jhn'
layout: post
---
In life, one of the simplest questions are by far the hardest to understand and perhaps define as well but they hold the universal truth, one has always been seeking. Let's talk a little about databases. The word data would mean, a statistical collection of references in a storage where they can be further analyzed and deduced in a resulted manner. When data is analyzed, it becomes information that has value to it. 

So, when we talk about a database, in general we will be speaking of the following;

*   A Database also known as a Schema
*   Tables
*   Rows

Now this is an excel sheet prepared using Google Docs.

![](https://thepracticaldev.s3.amazonaws.com/i/rdis27xt0r1t7ckqn4mo.png)

The name of my file myfirstdb is called a Database or a Schema. The sheet is known as users which we call a table. The more sheets, the more the tables. The A,B,C... are known as columns which are horizontal, and the 1,2,3... are known as rows which are vertical.

Now lets see, a visual representation of the same excel sheet in a database visualizer.

![](https://thepracticaldev.s3.amazonaws.com/i/yeogkokzysgqfh8vxzdh.png)

Now lets talk about some terms and what they mean, these features are like helpes that facilitate us in designing and storing entries in the database;

* Primary Key
* NN or Not Null or Null
* Auto-increment or AI

**Primary Key**
It is a feature of a relational database, that sets to a column making sure that whatever value it contains is always unique. If no value is ever tried to insert into it, it will not allow the entry to be made.

**NN or Not Null or Null**
Simple, it has to have a value or do not allow any entry to enter into it.

**Auto-increment or AI**
Now you really dont want to keep calculations of the number of rows inserted and what row numbers are to be stored and improved, so this one helps in it, it automatically keeps a record of previous entry counts and adds one to the next where necessary.

Now there are four basic operations that can be done on any relational database, which are;
* INSERT or CREATE - Inserts Data into a row in the Table
* SELECT or READ - Brings back Data form the Table
* UPDATE - Updates a Row in the Table
* DELETE or REMOVE - Deletes a Row

There is a short form to it known as **CRUD** (CREATE, READ, UPDATE, DELETE), i wanna create my own, lets say **SIDU** (SELECT, INSERT, DELETE, UPDATE)

Now lets create a database, if you have been following the tutorial so far, you should have a basic webserver running on your computer and a database server, with phpMyAdmin or MySQL Workbench as a Data Administrator tool installed. Make sure your webserver is running.

Open your browser and type: http://localhost/ or http://127.0.0.1/, you should be displayed by a WampServer page in Windows case, in other cases just follow to the phpMyAdmin page. Click on phpMyAdmin

![](https://i.ibb.co/VC7VXLQ/Image-004.png)

You should now come up with a login screen.
Username: root
Password: 

The password is blank, none and empty. 

![](https://i.ibb.co/hRdbM2S/Image-005.png)

Click on Go.

Dont worry, about all the tabs and things. Click on Databases on the upper left corner.

![](https://i.ibb.co/kSn1btc/Image-006.png)


Now lets create a database. Type in myfirstdb and just click on Create.

![](https://i.ibb.co/5xCZM61/Image-007.png)

The structure tab is where we define, what columns we will be using.

![](https://i.ibb.co/b2q2fNh/Image-008.png)

Set number of columns to 3 and type in users, this is the table we are creating. Click on Go

![](https://i.ibb.co/tJ8FKqT/Image-009.png)

Now it will create, 3 empty fields where we will input the column names. See picture for reference. The primary is the primary key and AI is the autoincrement. Click on Save.

![](https://i.ibb.co/J2s7kN3/Image-010.png)

Now, the structure is created, if you go through the text, i am sure it will now start making sense. Click on Insert Tab

![](https://i.ibb.co/259hjYL/Image-011.png)

Lets enter some rows, and also uncheck ignore because we are entering 2 rows. Click on Go. Now the query is run and two rows are inserted into it. Click on Browse

![](https://i.ibb.co/mhgkmdt/Image-012.png)

![](https://i.ibb.co/TMdsd9G/Image-013.png)

![](https://i.ibb.co/V9ckWmV/Image-014.png)

Now, you can see the similarity in between the excel sheet and the MySQL Database we have created.

![](https://i.ibb.co/VHBDDJb/Image-015.png)

[Noob Index](https://dev.to/th3n00bc0d3r/noob-guides-index-4mne)

*[This post is also available on DEV.](https://dev.to/th3n00bc0d3r/understanding-databases-relational-jhn)*


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
