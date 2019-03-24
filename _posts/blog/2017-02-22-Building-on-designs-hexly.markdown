---
layout: post
title:  "Online reviews prototype: Hexly"
date:   2017-02-22 19:12:45
categories: blog
---

Following on from my Reinventing online reviews article I have devleoped a working prtotype of my inital design. 

##### Finshied Product

<div class="honeycombpic-long">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/hexly-draw.png?raw=true"/>
</div>

##### Hexagon Geomtry

The majority of time for this project went into understanding how to draw a hexagon with hexagons using Canvas. I have to give
a huge amount of credit here to Reb Blob Games who wrote an outstanding article on this exact topic. This article gave me 
a massive headstart in creating my libary for Canvas.

The image below is from Red Blog Games. It was the basis for the algorithm I wrote for deciding where a word should be placed in the hexagon. To calculate where a word should go I used distance metric to ensure words with a higher sentiment positive or negative are further from the center. This calculation is trivial once each hexagon has its x,y,z coordinates for its location. I also colored the hexagons based on a normalized color spectrum to indicate the level of sentiment.

<div class="honeycombpic-small">
<img class="honeycomb-pic" src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/hexagon-layout.png?raw=true" />
</div>

##### Infrasturuce

The following is the infrastructure setup.

<div class="honeycombpic">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/hexly-infra.png?raw=true" />
</div>

##### Demo

<div class="honeycombpic-long">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/hexly.gif?raw=true" />
</div>
