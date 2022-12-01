---
title: I built a website
subtitle: This website
date : 2022-08-06
summary:  I had been learning web development, on my own for about a year, and want to see a project through from start to finish. I always loved writing as a kid and a blog site appeared simple enough. Since I am starting a blog, why not write about the process? I am fairly new to development, so this is a great way for me to document my development as a developer(say that five times fast). 
tags: 
  - 'Web_Development'
  - 'feature'
  - 'buildseries'
  - 'series_first_website'
badge: Web_Development
image: '/images/picture1.png'
author: Oliver Lund
---

## Create a site from start to finish
 I had been learning web development, on my own for about a year, and want to see a project through from start to finish. I always loved writing as a kid and a blog site appeared simple enough. It will be a place to collect my thoughts and hopefully help someone else along the way. Since I am starting a blog, why not write about the process? I am fairly new to development, so this is a great way for me to document my development as a developer(say that five times fast). I put this series on the site as its first set of archives. I’ll walk you through the tools I used why I made the decisions I did and how they affected the final product.
 
## So what’s important for a blog site?
 Easy to update, fast to load and has a well organized content filing system that’s searchable. After looking at different site architectures I decided to construct the site using a JAM (javascript, apis and markup) stack with a SSG or static site generator.  For this I chose 11ty, a node package installed locally in my working directory. Each article will be a markdown file that will be rendered as its own html page. For more information on what an SSG is and why I chose 11ty stay tuned for the next installment of this series.


 ---
<img src="{{image}}" class="img-fluid">  


---
## Now let's talk about hosting
 There are lots of hosting services out there, you can also host in house if you’re savvy enough. For a simple blog site I’m going with a hosting service. I have chosen Netlify for my project. I have chosen them for a few reasons. First of all, a great free tier. It is important to me that this series remains as accessible as possible. Netlify also offers continuous deployment from a github repo making this one a no brainer.

## git and github for version control.
They are well documented, widely used and they integrate well with each other as well as netlify. While not necessary github plays an integral role in how the hosting service and updating will work for this project specifically.  It is a best practice to use version control for any type of serious development. Having the project on github is also integral to how the site will be updated. Netlify will rebuild your site everytime you update the repo on github. This will be linked to netlify CMS. I can then create new posts from an admin panel in a browser anywhere in the world.

 
 ---
## That wraps up the basics
Why I am doing this and how I plan to do it. See you next time when we talk in depth about [static site generators](https://dev.to/techthatconnect/static-site-generatorsssg-what-are-they-and-why-im-using-one-2i8h) and the JAM stack.


*This article is part 1 of a series*
*select from all additional installments below*
<ol>
{%for post in collections.series_first_website%}

<li>
<div class="card border d-inline m-2">
<a href="{{post.url}}" class="text-decoration-none">{{post.data.title}}</a>
</div>
</li>

{% endfor %}
</ol>
