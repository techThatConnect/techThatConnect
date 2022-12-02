---
title: Static Site Generators(SSG)
subtitle: what are they and why I'm using one.
date : 2022-08-14
summary:  Before we can generate one we should first know what it is. A static webpage is one that all HTML files are rendered and ready to serve upon request. This is in contrast to dynamic websites where parts or all of the site are generated at the time of viewing. So now that's out of the way, what is an SSG? A static site generator is a tool that generates a full static HTML website based on raw data and a set of templates. They come in different flavors that have their own niche but all mostly do the same thing. Before we look at some different SSG let's first discuss why we should use one.
tags: 
 - 'posts'
 - 'feature'
 - 'Web_Development'
 - 'series_first_website'
badge: Web_Development
image: '\images\devops.jpg'
author: Oliver Lund
---

## What is a static site?
 Before we can generate one we should first know what it is. A static webpage is one that all HTML files are rendered and ready to serve upon request. This is in contrast to dynamic websites where parts or all of the site are generated at the time of viewing. So now that's out of the way, what is an SSG? A static site generator is a tool that generates a full static HTML website based on raw data and a set of templates. They come in different flavors that have their own niche but all mostly do the same thing. Before we look at some different SSG let's first discuss why we should use one.

## Why do you want a static site isn't that the old way of doing things?
Well yes it is but in terms of speed and security static sites are second to none. 
For my project which is a simple blogging website there is no sensitive data, just articles already available to the public. This means there isn't anything on the server that a hacker wouldn't already have access to, making hacking your site very pointless. There is no computing logic on the server side so static sites are fast to serve up. If having a static site will work for your project it is considered by many to be the best path. For my project speed is very important because if anyone has to wait longer than 2 seconds to read a short article they will often click away. So for my purposes a static site is ideal. 

 ---
<img src="{{image}}" class="img-fluid">  

 ---

## Ok now we know why you want a static site, How do you go about building one?
 You build a nice landing page and then an about page and a contact page and so on. You might start with the same boilerplate HTML but the content is different for each page. You make, let's say just 5 pages but then you need to update the navigation section of your site. You would have to go make the exact same update on each page.  Now imagine you have a blog with hundreds of pages, one for each article. That's a lot of your time and effort just to update a simple menu item. This is the main reason people use SSGs. You can just update the navigation sections template and then re render the site and all your pages are updated at once. The above reasoning is why I chose to use a SSG to create my site. 
While blogging sites are not all you can make with a SSG, blogging is where they really shine.

As I mentioned before SSGs come in different flavors here are a few of the most popular with a brief description.

[Jekyll](https://jekyllrb.com/) a ruby based SSG created in 2008 by GitHub co-founder Tom Preston-Werner. It gained a lot of popularity due to support on github pages.


[Hugo](https://gohugo.io/) is an open-source SSG built-in Go created back in 2013. Hugo's claim to frame is its lightning-fast build times.


[Eleventy's ](https://www.11ty.dev/) approach combines the simplicity of other traditional SSGs like Jekyll or Hugo with the popularity of JavaScript. Mozilla adopted Eleventy for sites like the Firefox extension documentation and the new version of MDN.


This is a short list of traditional(non framework based) SSGs a full list can be found at [jamstack](https://jamstack.org/generators/)

## For my project 
[I have decided to use 11ty](https://dev.to/techthatconnect/11ty-my-ssg-of-choice-and-how-use-it-in-my-blog-2f43)
 It's not tied to a framework and lets you use a few different markup languages as well as arbitrary javascript. 11ty is a node.js module that's installed locally to my working directory. Its robust while being lightweight and works well for my purposes. More on this in the next installment.  
  

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
