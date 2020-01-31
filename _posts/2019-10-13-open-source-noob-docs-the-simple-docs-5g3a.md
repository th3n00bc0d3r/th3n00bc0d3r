---
title: '[Open Source]: Noob Docs - The Simple Docs'
date: '2019-10-13T15:19:58.324Z'
excerpt: ''
thumb_img_path: >-
  https://res.cloudinary.com/practicaldev/image/fetch/s--CH6uSyuA--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://res.cloudinary.com/practicaldev/image/fetch/s--uQFYb-tu--/c_imagga_scale%2Cf_auto%2Cfl_progressive%2Ch_420%2Cq_auto%2Cw_1000/https://thepracticaldev.s3.amazonaws.com/i/c6ged1nb9u87ayl500c8.jpg
comments_count: 0
positive_reactions_count: 11
tags:
  - contributorswanted
  - javascript
  - angular
canonical_url: 'https://dev.to/th3n00bc0d3r/open-source-noob-docs-the-simple-docs-5g3a'
layout: post
---
## What is Noob Docs?

Noob Docs is a complete Git Powered Documentation System meaning it is a place where all documentations that have ever seemed make no sense become a documentation that makes sense. It is a repository for simplifying documentations and guides.

### How does it work?

![Noob Doc Concept](https://i.ibb.co/dpsFG2p/concept.jpg)

All tutorials and guides are hosted on a github repo. The website itself is hosted on github pages. Noob Docs uses Markdown as the standard for writing and publishing articles. The articles follow a simple folder based hierarchy, just like in the back of the old times where all were organized in folders. Anyone can can fork the repo and add changes to it which can later be merged into the repo. As soon as the changes are merged, Noob Docs automatically fetches them and makes them avaialble for the web. These tutorials are also available to read by just browsing the repo itself too. 

#### The Directory Structure?

You can find the repo at: https://github.com/th3n00bc0d3r/noobdocs

{% raw %}```
Guides/ ## Directory for Uploading and Structuing the Guides
Test/ ## This is just a test Directory
docs/ ## The Compiled Script for the Website
.gitignore ## Ignores Folders/Files you do not want to upload
CNAME ## Used for redirecting to Domain Web Address
README.md ## This is the Home Page
```{% endraw %}

Now If you look at: noobdocs/Guides/Databases/MySQL/Understanding Databases (Relational)/

{% raw %}```
noobdocs/Guides/Databases/MySQL/Understanding Databases (Relational)/

1. Guides is the Main Folder
2. Databases is a Category Folder
3. MySQL is a Sub-Category Folder
4. Understanding Databases (Relational) is the Article Folder
```{% endraw %}

#### The Article Directory

![Article](https://i.ibb.co/QdMQtfx/Screenshot-2019-10-13-at-3-08-33-PM.png)

{% raw %}```
links.md - This is the table of contents of your article
readme.md - This is the article itself
```{% endraw %}

#### links.md

{% raw %}```
[Introduction](# introduction)
[Features](# features)
[Primary Key](# primarykey) - 1
[Not Null](# notnull)
[Auto Increment](# autoincrement)
[CRUD](# crud)
[Excercise 1](# excercise1)
```{% endraw %}

When making links.md, please be sure the # link in this case 1 is all lowercase and without any spaces or the side table of contents will not work on the website

#### readme.md

{% raw %}```
#### Primary Key
It is a feature of a relational database, that sets to a column making sure that whatever value it contains is always unique. If no value is ever tried to insert into it, it will not allow the entry to be made.

#### Not Null
Simple, it has to have a value or do not allow any entry to enter into it. i. e. NN, Not Null, or Null
```{% endraw %}

As you can see it is very simple to link headings with the table of contents of your article.

Summary of Contribution
============

1. Fork it
2. Create Folder in noobdocs/Guides/Category/SubCategory/ArticleName
3. Create your Article branch ({% raw %}`git checkout -b my-new-feature`{% endraw %})
4. Commit your changes ({% raw %}`git commit -am 'Add some feature'`{% endraw %})
5. Push to the branch ({% raw %}`git push origin my-new-feature`{% endraw %})
6. Create new Pull Request

# Noob Docs Source
![  Preview](https://i.ibb.co/v4scjRm/Screenshot-2019-10-13-at-7-32-00-PM.png)

The frontend that is the website is made using Angular 8. Please follow the following guide to set it up locally.

{% raw %}```
git clone https://github.com/th3n00bc0d3r/noobdocs.git
cd source
npm i
ng serve
```{% endraw %}

You need to have the following for it to run;

- NodeJS and NPM
  https://nodejs.org/en/download/
- Angular 2 + and Angular CLI
  https://angular.io/guide/setup-local

I highly recommend Visual Studio Code, you can use any editor of your choice.

#### The Source Structure

source/src/app

![Source Structure](https://i.ibb.co/jJYC06K/Screenshot-2019-10-13-at-7-27-52-PM.png)

The whole application because of Angular is a module based application.

{% raw %}```
layout ## The Layout Module, think of it as a wrapper
-- frame ## This is where the content is loaded
-- header ## The Navigation of the Website
pages 
 -- article ## The Component for where your article is rendered
 -- categories ## Listing for Folders from Github
 -- home ## This is the Homepage where Readme.md is rendered
 -- wip ## Just a 404 Page not Found
services ## API List for communication
```{% endraw %}


<iframe class="liquidTag" src="https://dev.to/embed/github?args=th3n00bc0d3r%2Fnoobdocs" style="border: 0; width: 100%;"></iframe>



*[This post is also available on DEV.](https://dev.to/th3n00bc0d3r/open-source-noob-docs-the-simple-docs-5g3a)*


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
