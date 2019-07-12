---
layout: post
title:  "The side project journey"
date:   2018-10-10 16:57:10
categories: blog
---

##### Overview

 [The Gaelic Point](https://www.thegaelicpoint.ie) is a web application I developed for viewing Gaelic football data. The idea for the application, while important, was not the primary reason for taking on a new side project. The goal was to go through the journey and process of bootstrapping an idea from start to finish. 

This blog will share that journey and process, along with my thinking at the various stages throughout the development life cycle.

##### Research & Analyse 

The first step is to choose an Idea. One major requirement I have for settling on an idea is that it is engaging to me. A great idea that I have no interest in is likely to go unfinished. Once I have chosen an idea I go through the visualization process of imagining what the functionality and design of the application will be. I then sketch some rough wireframes, more as a guide rather than a fixed implementation.

##### Design

The second stage is to choose a tech stack. The technologies I choose for this project can be broken down into three sets. Those that I comfortable with and will allow me to work at a high velocity, which are Python, Django, GIT, Heroku. There are technologies which I have been wanting to try, for example, the Django Rest Framework. Lastly, there are the latest technologies, which help push the boundaries of my knowledge. [Barry Owens](http://www.barryowens.net/) a close friend who I have worked with on building the [Dublin Digital Radio](https://listen.dublindigitalradio.com/) website recommended trying Vue.JS & Nuxt.js. These JS libraries combined together neatly to solve the indexing and social sharing issues web crawlers have with some single page web frameworks.

Once the tech stack is decided on I move onto the database design. I started by listing all the entities related to the project, along with the related attributes and finally mapping their relationships.

<div class="honeycombpic-short">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/system-arch.png?raw=true"/>
</div>


Once the tech stack is decided on I move onto the database design. I started by listing all the entities related to the project, along with the related attributes and finally mapping their relationships. 


<div class="honeycombpic-long">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/database-design.png?raw=true"/>
</div>


##### Development

The third stage is to scaffold out the application. The development starts with the database infrastructure. Then the accompanying CRUD API's for the entities. Both DB modeling and API creation were effortless using Django and the Django Rest Framework.

The next section of the application was the front end. This part was the most labor intensive. I had never used the Vue.js framework before. It took quite some time to grasp the patterns and layouts. Vue has a unique single-file layout where HTML, CSS, and JS all live inside the same file. Vue is a very opinionated library. It has pre-defined functions which must be utilized to complete specific tasks. Calling external services via its annotated method for server-side rendering is a prime example of this opinionated style. This was great in the long term as it enforces high code quality. The steep learning curve definitely paid dividend.


##### Deployment & Release

The fourth stage was the deployment and release. The cloud platform I chose was Heroku. Heroku’s PAAS allows for easy integration with Github to build a CI pipeline. From the outset of the project, all the code was pushed to Github. The code goes through the Heroku pipeline and propagates to a staging instance. At release, I created a separate production instance. Once I validate the code on the staging instance, I promote the code to production. This is all aided by Heroku’s pipeline tooling.

While staging runs on Heroku’s free instance, production is running on the Hobby level, which provides insights into performance. I also connected Sentry for automated error handling and reporting. Sentry is extremely useful because it allows for weekly email reports on errors seen along with alerts for specific issues.

##### SEO

The fifth and final stage for this project was search engine optimization. I requested Google to index my website. To my disappointment, it received a low score. The search performance was taking a hit. To improve my search ranking I took a number of steps.

1. Included a sitemap.xml file.
2. Updated the page titles and meta to be unique and relevant for each page.
3. Converted javascript URL re-direct actions to physical HREF links for better indexing of the entire website.
4. Made minor performance & mobile enhance.
5. Ensured all HTTP requests were getting redirected to https on cloud-flare.

SEO is an on-going battle and continuously needs work. For now, I am delighted to see my application at the top of Google for one keyword and with 1500 monthly users!

<div class="honeycombpic-small">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/growth.png?raw=true"/>
</div>

##### Final Product

The following is a series of screenshots from the website. Enjoy!

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




