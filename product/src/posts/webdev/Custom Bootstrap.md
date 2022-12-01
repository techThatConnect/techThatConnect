---
title: Customize Bootstrap
subtitle: with your own sass pipeline
date : 2022-09-15 
summary: I am in the process of creating a website that is all static html, css maybe some javascript. I want to use some functionality of bootstrap but don't need the full thing.
tags: 
  - 'Web_Development'
  - 'posts'
badge: web development 
image: 
author: Oliver Lund
---

I am in the process of creating a website that is all static html, css maybe some javascript. I want to use some functionality of bootstrap but don't need the full thing as it's a large file. So how do I get just the bits I need without having to manually go through source code, delete stuff and risk creating bugs. You create your own sass pipeline and a custom version of bootstrap.  I didn't find any tutorials that covered the aspects of this I was struggling with. Now that I have made it out the other side I can help you do the same. The instructions listed here are for Windows users that understand how to use a terminal (Powershell in my case as it's the default terminal for VScode)

## What is sass?
Sass is a superset of css. Sass adds a lot of functionality found in standard programming languages. Variables, inheritance and other such things. It is then compiled or more accurately transpiled into css so that it can be interpreted by the browser. Sass is to css what typescript is to javascript, as they are both popular examples of supersets.

## First let's get sass installed.
We will be installing using a terminal and chocolaty but you can find additional instructions for alternative ways to install at [sass-lang.com](https://sass-lang.com/install)
I installed dart sass using [chocolaty package manager](https://chocolatey.org/) which you will have to install first. Once you have chocolaty installed go to powershell and run the following command.

> choco install sass  

That's it, now run the following command to make sure the installation worked.  

>  <p class="text-warning d-inline">sass</p> --version 

If the terminal outputs a version number you are ready to go. 

## make a custom.scss file
Inside of the folder containing your websites files which from here on out we will call the working directory. Create a new  folder labeled 'scss' and a new file named custom.scss inside that folder. To avoid modifying any of bootstraps sass files we will import what modules we need and overwrite any variables we want to change. There is a file labeled bootstrap.scss inside of the following path /node_modules/bootstrap/scss copy its contents to my custom.scss file and then remove any @import's I am not using.
 There are a few modules that are required when doing this. 

## what's required 
Bootstrap requires certain style sheet imports. Functions, variables and mixins. They give the following starting template in their documentation.

><p class="text-green">// 1. Include functions first (so you can manipulate colors, SVGs, calc, etc) </p>   
><p class="text-danger d-inline">@import</p> <p class="text-primary d-inline">"../node_modules/bootstrap/scss/functions";</p>  
>  
> <p class="text-green">// 2. Include any default variable overrides here  </p> 
>    
> <p class="text-green">// 3. Include remainder of required Bootstrap stylesheets   </p> 
>   
> <p class="text-danger d-inline">@import</p> <p class="text-primary d-inline">"../node_modules/bootstrap/scss/variables";</p> 
> <br>
> <p class="text-danger d-inline">@import</p> <p class="text-primary d-inline">"../node_modules/bootstrap/scss/mixins";</p>   
> <br> 
> <p class="text-green">// 4. Include any optional Bootstrap components as you like </p> 
>  
> <p class="text-danger d-inline">@import</p>  <p class="text-primary d-inline">"../node_modules/bootstrap/scss/root"; </p>  
>  <br>   
> <p class="text-danger d-inline">@import</p>  <p class="text-primary d-inline">"../node_modules/bootstrap/scss/reboot";</p>
> <br>    
> <p class="text-danger d-inline">@import</p>  <p class="text-primary d-inline">"../node_modules/bootstrap/scss/type"; </p>  
> <br> 
> <p class="text-danger d-inline">@import</p>  <p class="text-primary d-inline">"../node_modules/bootstrap/scss/images";</p> 
> <br>   
> <p class="text-danger d-inline">@import</p>  <p class="text-primary d-inline">"../node_modules/bootstrap/scss/containers"; </p>  
> <br> 
> <p class="text-danger d-inline">@import</p>  <p class="text-primary d-inline">"../node_modules/bootstrap/scss/grid";</p>    
>    <br> 
> <p class="text-green">// 5. Add additional custom code here  </p> 

now you can use as much or as little of bootstrap as you would like. You can really customize a it to fit your project, changing the default colors to fit your brand and so much more.

## Compile/Transpile to css 

Now you have your custom.scss all finished (at least for now) its time to make it plain old css that a browser can understand. Open a new terminal and make sure you are in your working directory(the root of your file system) when you run the following command.

> sass *your_project_name*/scss/custom.scss *your_project_name*/custom.css

This command can be broken down into three components seperated by spaces. Sass being the program we would like to run. the second to being files paths. The first is what file you would like to compile/transpile and the second being where you would like the new css file to go.
As you can see the above command will output a css file in the root of your working directory. You can have the css file render inside of a nested folder just remember you are writing the file path from the root of the working directory because thats where you will be running the command from. The big mistake I had made when first trying this was running the compile command from insidethe scss folder containing my custom.scss file. This will result in errors, make sure you run it from the working directory of your project and that all file paths are relative to that location.

## there you have it
Go have fun customizing bootstrap and really making it your own.  



