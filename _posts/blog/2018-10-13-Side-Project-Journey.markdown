---
layout: post
title:  "Side Porject Journey: TGP"
date:   2018-10-10 16:57:10
categories: blog
---

##### Overview

 [The Gaelic Point](https://www.thegaelicpoint.ie) is a web application for viewing Gaelic Football data. The application idea for the side project, while important, was not the primary reason for me to take on the side project or this blog. 

The goal of the side project was to go through the journey of bootstrapping an idea from start to finish. While, the goal of this blog is to share that journey, process, and thinking at different stages through the life cycle of the project.
 
##### Business Analyse & research 

The first stage is to settle on an idea. Ideas for side projects can come from anywhere. For me, it primarily comes from looking towards the interests of my life. One major requirement I have for settling on an idea is that it must be engaging to me, this is critical. A great idea that I have no interest in, is far more likely to go unfinished than I project I have interest in. The last step is some market research. This involves accessing other products and analyzing their key features.  

##### Design

The second stage is to choose a tech stack and do any application design work required.  The technologies I choose can be broken down into three sets. Those that I know suit the application, those that I have been wanting to try and completely new technologies which had been recommended. Python, Django, GIT, Heroku are my tried and tested technologies which I am very comfortable with. DRF or Django Rest Framework is a technology I want to try. It allowed me to build a single page application and avoid Django's server side templating. [Barry Owens](http://www.barryowens.net/) a close friend who I have worked with on building the [Dublin Digital Radio](https://listen.dublindigitalradio.com/)  website recommended trying Vue.JS & Nuxt.js. These JS libraries combined together neatly to solve the indexing and sharing issues crawlers have with some single page applications.

<div class="honeycombpic-short">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/system-arch.png?raw=true"/>
</div>


Once the tech stack is decided on I move onto the database design. I start by listing all the entities related to the project, along with the related attributes and finally mapping their relationships. 


<div class="honeycombpic-long">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/database-design.png?raw=true"/>
</div>


##### Development

The third stage to build out the application. The development started with building out the database models. This was followed by mapping the API's needed for reading and searching the required info. I have used Django before so creating the models was relatively easy. While I had never used the Django Rest Framework before I found creating API's with it very intuitive and painless. 

The section of the application which took the most time was, and always dose for me is the front end. I had never used the Vue.js framework, and it took some time to get used to its single-file layout and pre-defined functions. Vue.js is a very opinionated library. Everything is coded in a very strict fashion. This is great in the long term as it enforces high code quality but comes at the cost of a steep learning curve. Once, I got into Vue development I started to enjoy coding on the front end. It allows for the implementation of animations and transitions quite easily out of the box.


##### Deployment & Release

The fourth stage, deployment, and release, was relatively straightforward because of Heroku. Heroku's PAAS platform allows for easy integration with Github to build a CI pipeline. From the outset of the project, all code pushed to Github, ran through the Heroku pipeline and propagate to a staging instance. At release, I created a separate production instance. Once I validate code visually on the staging instance, I prompt code to the production instance, this all aided by Heroku's pipeline tooling. 

While staging runs on Heroku's free instance, production is running on the Hobby level, which provides insights into performance. I also connected Sentry for automated error handling and reporting, which has been extremely useful because it allows me to get email updates with errors without having to check the application logs.     

<div class="honeycombpic-long">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/sentry.png?raw=true"/>
</div>

##### SEO

The fifth stage and final piece of the puzzle for this project was search engine optimization. After finishing development and requesting indexing from Google I noticed the search performance was doing pretty poorly. I have been heavily using Googles Search console to access and optimize my site. I have added a sitemap.xml, updated the page titles and meta to be unique and useful for each page. I converted javascript URL re-direct actions to physical href links for better indexing of the entire website and I made minor performance & mobile enhance to increase the sights score. Lastly, I ensured all HTTP requests were getting redirected to https on cloud-flare. I still have a lot of work to do in this regard as it still isn't performing as well as I had originally hoped on Google search.


<div class="honeycombpic">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/google-console.png?raw=true"/>
</div>


##### Final Product


 [The Gaelic Point, test it out! ](https://www.thegaelicpoint.ie)




