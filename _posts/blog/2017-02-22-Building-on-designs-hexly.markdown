---
layout: post
title:  "Online reviews prototype: Hexly"
date:   2017-02-22 19:12:45
categories: blog
---

##### Introduction

In my "Reinventing online reviews" article I designed a unique method for categorizing and viewing online reviews. Since then, I have built a working prototype application for this design. I also added integration capabilities with Twitter to visualize sentiment for a given topic.

##### Hexagon Geometry


One of the challegening parts of this proejct was translating the vision I had of a hexagon structure into a tangiable web application. 

To achieve my grid of hexagons I need to learn how to arrange hexagons into a hexagon shape, like the image below. A blog post from Amit Patel of Red Blog Games on hexagonal design was a brilliant aid. It provided a lot of foundational knowledge and was its algorithm was used in creating the grid of hexagons. 

Within my code my I followed an object orientated approach for development. I instantiate a grid object. This grid object was assigned an array of hexagon objects, each with their own center coordinates, sentiment color, and text.

<div class="honeycombpic-small">
<img class="honeycomb-pic" src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/hexagon-layout.png?raw=true" />
</div>

Once I have my objects I assign a entity and there sentiment to each hexagon in the grid. To calculate what word should be assigned to what hexagon I use the manhathan distance. This ensures words with a higher sentiment positive or negative are further from the center. This calculation is trivial once each hexagon has its x,y coordinates for its location. I also colored the hexagons based on a normalized color spectrum to indicate the level of sentiment. 

When all the required information is gathered and structured, each hexagon in the grid can then be drawn onto the canvas. One intertesing point is that each hexagon is drawn from two hexagons. One for the outer ring, the secon, 10% smaller is filled to give the coloured bar you see in the designs. 

```javascript

function drawPloygon(hexagon) {
    ctx.beginPath();
    ctx.moveTo( cosFunction(hexagon), sinFunction(hexagon));

    for (var i = 1; i <= hexagon.numberSides; i += 1) {
        var angle = (i * 2 * Math.PI / hexagon.numberSides) + hexagon.rad;
        ctx.lineTo(cosFunction(hexagon), sinFunction(hexagon));
    }

    ctx.fillStyle = hexagon.colour;
    ctx.lineWidth = hexagon.lineWidth;
    ctx.fill();
}

function cosFunction(hexagon){
    return hexagon.x + hexagon.size * Math.cos(angle);
}

function sinFunction(hexagon){
    return hexagon.y + hexagon.size * Math.sin(angle);
}
```

<div class="honeycombpic-long">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/hexly-draw.png?raw=true"/>
</div>

##### Infrastructure



<div class="honeycombpic">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/hexly-infra.png?raw=true" />
</div>

##### Demo

<div class="honeycombpic">
<img src="https://github.com/bawn92/bawn92.github.io/blob/master/assets/img/hexly.gif?raw=true" />
</div>
