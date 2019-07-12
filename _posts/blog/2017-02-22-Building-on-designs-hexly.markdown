---
layout: post
title:  "Online reviews prototype: Hexly"
date:   2017-02-22 19:12:45
categories: blog
---

##### Introduction

In my “Reinventing online reviews” article I designed a unique method for categorizing and viewing online reviews. Since then, I have built a working prototype application for this design. I also added integration capabilities with Twitter to visualize sentiment for a given topic.
Hexagon Geometry

##### Hexagon Geometry


One of the challenging parts of this project was translating the vision I had of a hexagon structure into a tangible web application.

To achieve the the hexagon design I needed to figure out how to arrange hexagons such that the collection of them layout made a hexagon. A blog post from Amit Patel of Red Blog Games on hexagonal design provided the grounding information on drawing and arranging hexagons. The image below was the foundation for how I layed them out.

<div class="honeycombpic-square-small">
<img class="honeycomb-pic" src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/hexagon-layout.png?raw=true" />
</div>


I utilzied an object orientated approach for development. I instantiated a grid object. This grid object was assigned an array of hexagon objects, each with their own center coordinates.

Once I had my grid of hexagons, I assigned them an entity and a sentiment score. To calculate what word should be assigned to what hexagon I use a distance formula. This ensured words with a higher sentiment, either positive or negative were further from the center. This calculation is trivial once each hexagon has its x,y coordinates for its location. I also colored the hexagons based on a normalized color spectrum to indicate the level of sentiment.

When all the required information is gathered and structured, I then draw the hexagons onto the canvas. One interesting point is that each hexagon is drawn from two separate hexagons. Using two hexagons gives the bar hexagon seen in the images.

The following is a snippet of how the hexagons are drawn onto the canvas.

```javascript
function drawPloygon(hexagon) {
    ctx.beginPath();
    ctx.lineWidth = hexagon.lineWidth;
    ctx.moveTo(hexagon.points[0].x, hexagon.points[0].y);
	for(var i = 1; i < hexagon.points.length; i++)
	{
		var point = hexagon.points[i];
		ctx.lineTo(point.x, point.y);
	}
    ctx.fillStyle = hexagon.colour;
    ctx.lineWidth = hexagon.lineWidth;
    ctx.fill();
}
```

The follwoing is screenshot of the application of the finished design.

<div class="honeycombpic-long">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/hexly-draw.png?raw=true"/>
</div>

##### Infrastructure

Access to data is key for any modern web application. For this reason I allowed the latest trending hashtags to be analyized and visualized through the application. I feed a significant number of tweets from twitter into Watson API's and then visualized the results. This was all deployed on IBM Cloud using Cloud Foundry and its python runtime environment. 

<div class="honeycombpic">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/hexly-infra.png?raw=true" />
</div>

##### Demo

<div class="honeycombpic">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/hexly.gif?raw=true" />
</div>
