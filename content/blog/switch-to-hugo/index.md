---
title: I finally decided on a software framework for my website
summary: Levelling up my personal website game by switching to Hugo
date: 2026-01-06
draft: false
authors:
  - admin
tags:
  - Programming
  - Personal Site

---

I recently switched from using plain HTML and CSS files to using the Hugo framework for nkeiru.com/nkeirucu.com.  
In this post, I will talk briefly about why I made the switch, the process of switching and what I like and dislike so far.
I want to document the technical steps of switching to Hugo for my own reference and others including mistakes I made.


Deciding to want to have a personal website was easy.
Its is a place on the internet to tell my own professional story
rather than have random social media  profiles and articles tell an incomplete story.  Deciding, however, what software or framework to use is not easy.
There is an overwheming amount of options even among the free stuff. Since I have some programming literacy and often like to 
see how things work from the ground up, I decided to play around with some HTML and CSS files hosted in an eponymous github repo
which also takes care of hosting and publishing site on the internet. As my site grew, that became cumbersome so I looked around for something free, lightweight and well documented.
Hugo was my final choice. I can write content in markdown, configure page settings yaml/toml  in the header and get a static site generator. There is the added benefit that it is fast.

**Overview of my process**

- Clean up files from the old site by putting into a folder in existing Github repo dedicated to the site. I probably put too much thought into how I could preserve my hosting set up (or workflow?) with Github. Either set up
a new project in a new repo or preserve the old one. I went with the latter because while it was a new framework, this was not an entirely
new project.
- Download [https://gohugo.io/installation/](Hugo)
- Choose a theme (the fun part!). This took some time but eventually settled on[hugoblox.com](Hugo Blox) because of the variety of customization and embed options.
- To add a theme, I had  to add a submodule, a Github  concept to me that I am still hazy on. Essentially, it is cloning another  Github repo within a repo of your own.  I ended up moving the site files out of submodule because I was having issues with publishing the site. Later, I came to the conclusion that it may have been  due to the extraneous old_site folder that I added to the submodule. I think the downside of removing the submodule is that I cannot receive updates from the theme's original Github repo.

- Then I got to customizing.  Blocks, simply being UI features, are added by copy and pasting YAML templates into the front matter. I plan to find excuses to use as many block as I can!

**A selection of the most frustrating mistakes I made and their simple fixes**
- Installing the wrong version of Hugo: I originally downloaded Hugo Basic and the theme I downloaded required Hugo Extended. This is probably a hyperspecific mistake that only I could make but if you run into issues publishing the site, its worth checking.
- Blox not showing up: Hugo automatically "refreshes" when you make a change. I tried add a new block to the landing page and I kept getting error after error in the browser. Eventually I stopped the server and restarted the site and the changes appeared. Moral of the story is don't pay too much attention to the error messages in the local Hugo server.

**What I dislike**
- I can't find documrnation about the yaml/toml keywords. It is possible I haven't look hard enough.
- Using toml/yaml. I need to switch to yaml/toml. I love me some Python but it doesn't make relying on indentation any less painful. ~Oh how we have regressed since Fortran~

**What I like**
- With options to embed audio, video, Latex and even minmaps with Mermaid, Hugo Blox theme allows various ways to showcase your work and receive comments (with Disqus). You can write a blog, make a mini course or showcase your code by embedding a Jupyter notebook. I can't wait to see what I come up with.
