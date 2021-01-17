---
layout: post
title:  "The side project journey"
date:   2018-10-10 16:57:10
categories: blog
---

##### Overview

 The Gaelic Point was a small web application I developed for viewing Gaelic football data. The idea for the application, while important, was not the primary reason for taking on a new side project. The goal was to go through the process of bootstrapping a web application from start to finish. 

This blog will share that journey and process, along with my thinking at the various stages throughout the development life cycle.

##### Research & Analyse

The first step is to choose an idea. One major requirement I have for settling on an idea is that it is engaging to me. Once I have chosen an idea, I go through the visualization process of imagining what the functionality and design of the application will be. I then sketch some rough wireframes as a guide.

##### Design

The second stage is to choose a tech stack. CRUD and ACID functionality was core to the project. These were the primary reasons for choosing Django and Postgres. I wanted to experiment with a new UI framework, which is why I selected Vue.JS.

<div class="honeycombpic-short">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/system-arch.png?raw=true"/>
</div>

I then started the database design. I listed all the entities related to the project, defining attributes and types, and finally mapping the relationships.


<div class="honeycombpic-long">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/database-design.png?raw=true"/>
</div>


##### Development

The third stage was to scaffold the application. I started the development with the database infrastructure. Then I built the accompanying Rest API's. Modeling the database entities and API creation was effortless using Django and the Django Rest Framework. Django has a mature database migrations tool that allows for fast entity creation. The Django Rest Framework has well-established patterns for building API's which I utilized.

The next section of the application was the front end. This part was the most labor-intensive. I had never used the Vue.js framework before. It took some time to grasp the patterns and layouts. Vue has a unique single file layout where HTML, CSS, and JS all live inside the same file. Vue is a very opinionated library. It has pre-defined functions that enable specific tasks. Calling external services via its annotated method for server-side rendering is a prime example. This pattern was great in the long term as it enforces high code quality.

##### Deployment & Release

The fourth stage was the deployment and release. The cloud platform I chose was Heroku. Heroku’s PAAS allows for easy integration with Github to build a CI pipeline. The pipeline automatically propagates the code to the staging instance for every commit. Once tested and verified I push to the production instance.

I then connected Sentry for automated error handling and reporting. Sentry is extremely useful because it sends weekly email reports on errors seen and alerts for specific issues.

##### SEO

The fifth and final stage for this project was search engine optimization. I took a number of steps to optimize my website for Google's PagfeRank.

1. Included a sitemap.xml file.
2. Updated the page titles and meta to be unique and relevant for each page.
3. Converted javascript URL re-direct actions to physical HREF links for better indexing of the entire website.
4. Made minor performance & mobile enhance.
5. Ensured all HTTP requests were getting redirected to https on cloud-flare.

SEO is an on-going battle and continuously needs work. I am delighted to see my application at the top of Google for one keyword and with 1500 monthly users!

<div class="honeycombpic-small">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/growth.png?raw=true"/>
</div>

##### Final Product

The following is a series of screenshots from the website.

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