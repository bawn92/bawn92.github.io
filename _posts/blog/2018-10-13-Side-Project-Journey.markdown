# My side project journey.


"The Gaelic point" is a web application for viewing Gaelic Football data. Thats a very quick overview.  The application idea for the side project, while important, was not the primary reason for me to take on this side project or this blog. 

The goal of this side project was to go through the journey of boostrapping an idea from start to finish. While, the goal of this blog is to share that journey, process, and thinking at different stages through the life cycle of the project.
 
### Business Analyse & research 

Ideas for side projects can come from anywhere. For me, it primarily comes from looking towards the interests in my life, this is swiftly followed with detailed research to validate an idea. One major requirement I have for settling on an idea for a side project is primarily that it must be engaging to me, this is critical. A great idea that I have no interest in, is far more likely to go unfinished than I project I have interest in. 

### Design

Then I decide on a tech stack.  The technologies I chose can be broken down into three sets. Those that i know suit the application, those that I have been wanting to try and completely new technologies which had been recommended. Python, Django, GIT, Heroku are my tried and tested technologies which I am very comfortable with. DRF or Django Rest Framework is a technology I want to try. It allowed me to build a single page application and avoid Django's server side templating. [Barry Owens](http://www.barryowens.net/) a close friend who I have worked with on building the [Dublin Digital Radio](https://listen.dublindigitalradio.com/)  website recommended trying Vue.JS & Nuxt.js. These JS libarys combined together neatly to solve the indexing and sharing issues crawlers have with some single page applications.

This is what I settled on:

<div class="honeycombpic">
![enter image description here](https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/system-arch.png?raw=true)
</div>

Once the tech stack is decided on I move onto the database design. I start by listing all the entities related to the project and there related attributes and mapping there relationships.


<div class="honeycombpic">
![enter image description here](https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/database-design.png?raw=true)
</div>

### Development

The development starts with me building out the database models and mapping the API's needed for reading and searching the required info.




### Release

Heroku's 



USE SENTRY

<div class="honeycombpic">
![enter image description here](https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/sentry.png?raw=true)
</div>

### SEO

The last piece of the puzzle for this project has been Search Engine Optimisation. After finishing development and requesting indexing from Google I noticed the search performance was doing pretty poor. I have been heavily using Googles Search console to access and optimize my site. I have add a sitemap.xml, updated the page titles and meta to be unique and useful for each page. I converted javascript url re-direct actions to physical href links for better indexing of entire website and I made minor performance & mobile enhance to increase the sights score. Lastly I ensured all http requests were getting redirected to https on cloud-flare. I still have alot of work to do in this regard as it still isn't performing  as well as I had originally hoped on Google search.

<div class="honeycombpic">
![enter image description here](https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/google-console.png?raw=true)
</div>



 [The Gaelic Point, test it out! ](https://www.thegaelicpoint.ie)




