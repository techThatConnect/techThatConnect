---
title: 11ty my SSG of choice 
subtitle: and how I use it in my blog
date : 2022-08-16
summary:  Eleventy was originally pitched as a javascript alternative to jekyll. The site generator is created using node.js by Zach Leatherman who is currently maintaining the project. There are 2 main things that set 11ty apart from other SSGs in my opinion anyways 
tags: 
  - 'Web_Development'
  - 'series_first_website'
badge: Web_Development
image: '/images/hero.jpg'
author: Oliver Lund
url: '/posts/webdev/11ty_my_SSG_of_choice'
---
## So last time we covered what an SSG is and why you might want to use one.  
Now let's get more specific and talk about 11ty. Eleventy was originally pitched as a javascript alternative to jekyll. The site generator is created using node.js by Zach Leatherman who is currently maintaining the project. There are 2 main things that set 11ty apart from other SSGs in my opinion anyways 

## First is flexibility.   
Eleventy uses multiple templating engines in a mix and match fashion. Currently supporting the following
Markdown, Liquid (used by Jekyll), Nunjucks, Handlebars ,Mustache, EJS, Haml, Pug, JavaScript Template Literals (ES2015). Since you can use different syntaxes in the same project
I use a mix of markdown and nunjucks. Mostly markdown for the actual posts themselves as it's simple and since I'm currently posting these articles on dev.to they are already in markdown. I use nunjucks for templating the reason being nunjucks is more robust and I use 'for' loops in my templates to iterate through my posts categories.
With a few exceptions Eleventy has a flexible directory structure. You can organize your folder almost however you would like. I chose for my project to have a pages folder with my about and contact pages. A posts folder which is then organized by category into subfolders containing each individual markdown file.

 ---
<img src="{{image}}" class="art-pic">  
---

## Second is the use of javascript and the absence of it. 
I know that doesnt make a lot of sense but let me explain. Eleventy is built with node.js This gives you access to hundreds of thousands of modules you can use in conjunction with Eleventy. You can also write your own arbitrary javascript and insert into any template. This is the use of javascript.
It's absence is that while 11ty is written in javascript it is not a framework. Requiring no Eleventy specific client side javascript in the final product. You can still use a framework if you wish and add as much client side javascript as you want. But none of that is required. In an effort to keep my site as lightweight as possible I have decided not to add any modules to my build. The goal I have is to do as much as possible with HTML and CSS then add javascript as required. This might change as my site grows in the future.

## A few other great points about eleventy  
lightning  fast build times. The fact they link to all their competitors on their site, letting the work speak for itself. I found this very encouraging. And it's also important to note that the project is being maintained by Zach. Very few other site generators are being constantly monitored and updated like this which Gives 11ty much hope for the future.

## So now we know a bit about 11ty and the ways in which I have utilized it.  
If you want to know more about the 11ty project check out their [documentation](https://www.11ty.dev/docs/). If you like the project give them a star on github. I would like to be transparent here and say that I have not used another static site generator besides Eleventy. I did some research about the different types of SSGs and Eleventy stuck out as the choice for me and my project. 
Next time I'll talk about bootstrap and the importance of responsive design in the modern web.



