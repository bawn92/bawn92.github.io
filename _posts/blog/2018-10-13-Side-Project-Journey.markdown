---
layout: post
title:  "The Side Project Journey"
date:   2018-10-10 16:57:10
categories: blog
---

##### Overview

 [The Gaelic Point](https://www.thegaelicpoint.ie) is a web application for viewing Gaelic football data. The application idea for the side project, while important, is not the primary reason for me to take on the side project or this blog. 

The goal of the side project is to go through the journey of bootstrapping an idea from start to finish. While, the goal of this blog is to share that journey, process, and thinking at different stages through the life cycle of the project.
 
##### Business Analyse & research 

The first stage is to settle on an idea. Ideas for side projects can come from anywhere. Generally, mine come from looking towards the interests of my life. One major requirement I have for settling on an idea is that it is engaging. A great idea that I have no interest in is more likely to go unfinished. The last step is market research. This involves accessing other products and analyzing their key features.  

##### Design

The second stage is to choose a tech stack. The technologies I choose can be broken down into three sets. Those that I know suit the application, which are Python, Django, GIT, Heroku. Those that I have been wanting to try, DRF or Django Rest Framework is one. It allows me to build a single page application and avoid Django's server-side templating, which I find very restrictive for building modern web apps. Lastly, there are completely new technologies.  [Barry Owens](http://www.barryowens.net/) a close friend who I have worked with on building the [Dublin Digital Radio](https://listen.dublindigitalradio.com/)  website recommended trying Vue.JS & Nuxt.js. These JS libraries combined together neatly to solve the indexing and sharing issues web crawlers have with some single page web frameworks.

<div class="honeycombpic-short">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/system-arch.png?raw=true"/>
</div>


Once the tech stack is decided on I move onto the database design. I start by listing all the entities related to the project, along with the related attributes and finally mapping their relationships. 


<div class="honeycombpic-long">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/database-design.png?raw=true"/>
</div>


##### Development

The third stage is to build out the application. The development starts with the database models. This was followed by mapping the API's needed for reading and searching the required info. I have used Django before so creating the models was relatively easy. While I had never used the Django Rest Framework before I found creating API's with it very intuitive. 

The section of the application, the front end, took the most of the work, and always dose for me. I had never used the Vue.js framework, and it took time to get used to its single-file layout and pre-defined functions. Vue.js is a very opinionated library. Everything is coded in a very strict fashion. This is great in the long term as it enforces high code quality but comes at the cost of a steep learning curve. Once I got into Vue development I started to enjoy coding on the front end. It allows for the implementation of animations and transitions quite easily out of the box.


##### Deployment & Release

The fourth stage is deployment and release. This is made infinitely easier because of Heroku. Heroku's PAAS platform allows for easy integration with Github to build a CI pipeline. From the outset of the project, all code pushed to Github, is ran through the Heroku pipeline and propagated to a staging instance. At release, I created a separate production instance. Once I validate code visually on the staging instance, I promote the code to the production instance, this is all aided by Heroku's pipeline tooling. 

While staging runs on Heroku's free instance, production is running on the Hobby level, which provides insights into performance. I also connected Sentry for automated error handling and reporting, which has been extremely useful because it allows me to get email updates with errors without having to check the application logs.

##### SEO

The fifth and final stage for this project was search engine optimization. After finishing development and requesting indexing from Google I noticed the search performance was doing pretty poorly. I have been heavily using Googles Search console to access and optimize my site. To improve my search ranking I have made a number of changes. I started by including a sitemap.xml file. I updated the page titles and meta to be unique and useful for each page. I converted javascript URL re-direct actions to physical href links for better indexing of the entire website. I made minor performance & mobile enhance to increase the sights web ranking score. Lastly, I ensured all HTTP requests were getting redirected to https on cloud-flare. SEO is an on-going battle and continuously needs work. For now, I am delighted to see my application at the top of Google for one keyword and with 1500 monthly users!

<div class="honeycombpic">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/growth.png?raw=true"/>
</div>

##### Final Product


Homepage

<div class="honeycombpic">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/points_homescreen.png?raw=true"/>
</div>

Fixtures

<div class="honeycombpic">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/points_brackets.png?raw=true"/>
</div>

Teamsheets

<div class="honeycombpic">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/points_teamsheets.png?raw=true"/>
</div>

Stats

<div class="honeycombpic">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/points_charts.png?raw=true"/>
</div>

 [The Gaelic Point, test it out! ](https://www.thegaelicpoint.ie)




