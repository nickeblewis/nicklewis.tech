---
title: How I built this site
layout: Post
---

I have for so many years been running my [nicklewis.net](http://www.nicklewis.net) website which is built using Wordpress. It has been a lot of fun running that and I shall carry on with it for my photography, travel and more casual writing interests. However it was time to start building some more sites, to move away from the constraints of the Wordpress templating engine, the dreaded loop and especially as there are now better ways of doing all of this!! C'mon Nick keep up with the times!

If I am being totally honest most of my professional work does not involve Wordpress. I am working more with cutting edge technology and it is time to share some of that knowledge in terms of developing this business a great deal more.

So here we are, a new website with the domain of [nicklewis.tech](http://nicklewis.tech) which is built in the following way:

* Content is written in MarkDown and there is absolutely no database in use here at all, which is a little bit revolutionary hey?
* [Phenomic](http://phenomic.io) which is a 'static generator' and we shall talk more about these at some point later, but why not follow the aforementioned link and have a read, you will be hooked!
* ReactJS is used for building the components of this site
* Maybe a little Redux can be used, the facility is there to add it and I shall explore that asap, as that will allow us to do some adventurous things
* Github
* Netlify

**Ok so how does this work precisely?**

If we ignore the setup and configuration of Phenomic for the moment, what we end up is a project folder that contains a number of sub-folders:

* content - consists of it's own set of nested subfolders and .md files which are later compiled into working HTML files
* web_modules - consist of the application's ReactJS plugins
* assets - contains images etc

We can trigger off a site build and then a watch process which monitors for any changes that you make and automatically refreshes your browser courtesy of hot-reloading.

In order to deploy, we push all changes to the Github repo and this in turn triggers a build on the Netlify server via means of continuous integration. 

If other people were to contribute to the site, all they need to do is submit a pull-request on the code, we merge their changes in and that will also trigger a rebuild of the live site. 

It is an awesome workflow and in many ways so much easier than working the old fashioned way with LAMP!!!