---
layout: post
title: "Dynamic Websites are an Efficiency Nightmare"
author: vaibhav
categories: [WebDev, Tech, Rant]
tags: [sticky]
image: assets/images/serverfarm.jpg
---
More than 455 million websites use WordPress as their CMS, that's more than 60% of the world's websites, and 90% of these are single page websites serving static content and these fucking websites are running on their overkill private servers, running 1000 lines of php code just to render a single page website of contact details of your business. Not only this, frontends of most websites are loaded with 100 pounds of fucking javascript libraries, css libraries, remote fonts, huge ass images, popups, shit ton of ads and what not.

I just opened an article on a news website, and it required 13 MB of assets and 700 requests to load. That's more than the entire collection of Shakespeare.

The internet is not crashing beacuse of all this thanks to the increasing network bandwidth and increasing performance of devices. But, this is like the worst solution to this problem, most of the time you don't have access to a high speed network connection and the huge website load times are just killing. According to a research conducted by the Ericsson ConsumerLab, level of stress caused by mobile delays could be compared to watching a horror movie or solving a maths problem. 
![research_graph](/assets/images/errcison_website_research.webp){:class="img-responsive"} 
These heavy websites are the reason because of which your browser eats up all the ram on your computer, and all the network congestion in the world.

Another very important issue is it's effect on global warming, all this extra computing power, network bandwidth, storage demands more resources and that is a huge contribution to the increasing global warming.
All this is being caused because of the ease of website creation today, arrival of lots of new frameworks, libraries, no-code tools everyday, but the main reason is lack of proper planning/architecture and lack of required knowledge. A developer should know where to use a dynamic website, where to use a static, where to use libraries and where not, what all you should use external services for and what is the best toolset for your requirement.

## How to decide what's best for you?
To decide the best for your website you need to know about the 3 basic types of websites-
+ Static Websites- the browsers on your computers can only understand only 3 languages, html for structure, css for design, js for scripts and nothing else. Static websites just serve these 3 files, and the content in these stays static.
+ Dynamic Websites- whenever you visit a dynamic website, a backend server receives the request and generates the required html  file by using a html template and fitting data into it from the database on the server and then sends it to you also attaching required css and js files. These types of websites should be used when the content on your website is dynamic and keeps changing all the time, for example a social media website. These types of websites require a backend server which runs on php, ruby, python, js etc.
+ Modern Static Websites- these are also known as serverless websites, at first the client receives the 3 html, css and js files and then the javascript runs on the client's machine and fetches only the required data from the server(which keeps changing) and then renders it onto your machine.

Websites made using wordpress are php based, so everytime you visit a website, it generates the website on demand and then sends it to user even if the content on the website never updates. This is a waste of a lot of computing power. Also, to host this kind of website, a private server is required on which runs a mysql server and a php server, using a shitload of resources just to render simple static websites. Yes, there are shared hostings but those are also terribly inefficient for use case of a simple website.

90% dynamic websites can easily be implemented as static websites and A LOT OF RESOURCES!! can be saved. 

A hybrid architecture is the best solution for a efficient website, the stuff that stays constant for everyone is generated server side and cached and delivered via a CDN, and the dynamic content is served in a serverless style, this makes for optimum utilisation of resources and a faster performance. A dynamic website with it's own private server runs idle most of the time with occasional traffic but if you switcht to serverless you pay per function call or database accesses, and you can save a lot of money this way. Also, this way your website is infinitely scaleable, it can handle a million users right away, while in case of a website with private server, it will crash right away, in order to scale it you'll have to switch it to bigger servers and do complex load balancing stuff and what not.

A website with a hybrid architecture also makes up for the best experience for the users, i.e. the page will not reload again when you do something thanks to AJAX. For ex - on the amazon website if you apply one filter then the page will reload and if you want to apply another you will again have to scroll downwards and click again then it will reload again. A user generally wants to apply more than one filter and this experience is terribly annoying. This would have not been a problem if they had gone for a hybrid architecture, where new products are loaded with ajax or if they want to fix it in this way only just add a apply button which you press after selecting everything, I wonder why is amazon still not fixing it.

<video width="320" height="240" autoplay>
  <source src="/assets/images/amazon.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

In today's websites, the problem is not just in the backend architecture of them, but also the frontend architecture. Since the past few years, we have witnessed an arrival of a lot of fronted frameworks like react, angular, vue, svelte etc. Yes, these frameworks make it a lot easier to make complex websites and webapps, but make no sense when used for simple websites since they are very heavy make your website needlessly slow. Also using a lot of remote libraries for minor tasks and all also makes no sense, this combined with remote fonts and analytics tracking scripts make your website a terrible experience on slow devices and networks.

If you are planning to build a single page website for a business, club, company, university etc. please don't make it using wordpress or something similar, make it a simple static website and just host it on github, bitbucket or aws for completely free. And if you're planning to make something like a blog, try static site frameworks like jekyll or hugo, they are really easy to work with and there are a lot of templates and tutorials available and to upload a new blogpost, you just have to write it in markdown and commit to github, github will build it automatically and deploy it withing seconds, no need to worry about complex deployment pipelines and all. And, if you want to want to make a complex webapp like a social media or e commerce website, then try going for a hybrid website framework like next.js or gatsby. You can host these too for free with pretty generous quotas and scaling is also very cheap and affordable.

Well, even when so many tools and techniques for making efficient, faster and cheap websites exist, wordpress will still thrive, because of just one reason, ease-of-use, any person can create a website with wordpress, wix or squarespace easily or atleast maintain it and this is the reason it isn't dead. 

To bring the revolution of efficienct and better websites in this space, we need something like wordpress for static websites, an easy to use web based editor, free/cheap hosting, good looking easy to start templates, and fast performance. What do you think about such a platform and will it work?