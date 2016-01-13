---
layout: post
title: Why I chose Jekyll
tags:
- jekyll
- Technical 
published: true
---

As the new year rolled in just like many people on this earth, I reflected on the previous year and thought about some of the things I would like to accomplish in the new year. I don't have a long list, because I don't believe that ever works. Rather I'm focusing on a select few items, one of them being to write more this year. I've been writing quite a few blog posts for work and I found that I really do enjoy writing. I always seem to be  working on or doing exciting things that I would like to document to look back on. Hopefully one or two more people will find some of these posts helpful along the way.

So, this is the first post 

### Why I chose Jekyll for my blog and not WordPress

My initial instinct for a blog was to use WordPress. I sat down, excited about the new project only to find myself quickly disheartened by how bloated and complex WordPress really is. It's great if you need all those plug-ins and additional functionality but not when all you need is a place to put text on, which is my case. Also, I couldn't get anything up and running in a couple of hours, if I can't click on something within the first hour I'm out. 

Another requirement of mine is to be able to customize every aspect of my blog and be able to add my own unique functionality which didn't seem as straightforward with WordPress. The templates I looked at were all too restrictive and of course there's the PHP and a database requirement which isn't the worse but validated my "this is overkill" reaction.

### Jekyll

I did some research and came across [Jekyll](http://jekyllrb.com/) which is a static site generator with the ability to serve all its content right out of a Github repository. This means that you can host your blog right from Github's servers for free by using [Github pages](https://pages.github.com/). 

So far, I'm finding Jekyll and the [Hyde](http://hyde.getpoole.com/) theme incredibly simple and easy to use:
 
  * A database is not required as all posts and pages are converted to static HTML
  * I write my posts in Markdown which Jekyll generates the static HTML from. I find that much easier than using a CMS
  * I have full control over what's on my blog and I don't need to include functionality I'm not using
  * I was able to customize my own theme pretty quickly and didn't have to deal with anyone's bad CSS
  * Github hosts my blog for free!

### Up and Running in Under an Hour

 1. Create a repository that will host your blog, this is really easy to do and is documented [here](https://pages.github.com/)
 2. Install [Jekyll](http://jekyllrb.com/) from a terminal (Mac)
 	``gem install jekyll``
 3. Update the _config.yml file with your desired configurations and to resolve a couple of things (See issues below)
 4. I used [Hyde](http://hyde.getpoole.com/) for my theme, so I cloned the repository and served the site from the directory I cloned. `jekyll serve`
 5. Access your blog locally from localhost:4000 or commit your changes to see it live! 
 6. Write a post, play around with the CSS, commit your changes and repeat.

### Issues

 I ran into a couple of issues which I needed to resolve before being able to get the blog to run locally
 
 1. `Ensure you have gems: [jekyll-paginate] in your configuration file.` 

    I resolved the error by adding the following to my _config.yml file:
  		
          gems: [jekyll-paginate]

          paginate: 5
  	
          paginate_path: "page:num"

 2. `Since v3.0, permalinks for pages in subfolders must be relative to the site source directory` 

    I resolved the error by removing the following line from my _config.yml file: `relative_permalinks: true`

### Final Thoughts

That's it! I found it incredibly easy to get up and started with something that looks pretty decent. I'm also excited about working on some custom functionality and having complete control over how that will be implemented. More on that later. 
 
  	



