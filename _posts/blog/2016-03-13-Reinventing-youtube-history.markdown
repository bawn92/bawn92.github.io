---
layout: post
title:  "Reinventing: Youtube History Page"
date:   2016-03-03 20:11:16
categories: blog
---

I love Youtube, and I have spent a crazy amount of hours on the platform as you will see soon. The
quality of the content is consistently getting better and I'm always finding new
channels which I immediately love. However I do have some
issues with the platform itself. The main issue I have is with the history page for users. There is a
lack of proper analysis on the videos you have watched.

I feel people would love to know the total number of hours they have spent on the platform, average
view count and video length of videos they have watched and also information regarding there top channels
and how much time they have sent on each.

I became very interested in finding out this informtion about my own history so I search for tools and methods
of obtainning the infromation I desired. I soon realizd they was no avaible method to obtain the information I seeked.
I set out to develop a chrome extension which provides the statistics and information I felt are missing from the Youtube history page.


The tool works by automatically selecting the load more button on the history page until it has eached the end.
It then parses the data pulling the channels, title, video length and places
these into a hashmap. Once parsed into a hashmap, it is saved to local storage.

The following image is an example of the extension in action.

<div class="honeycombpic">
<img src="https://raw.githubusercontent.com/bawn92/bawn92.github.io/master/assets/img/feature-extraction.png"/>
</div>

The first time you run the tool it can take up too ten minutes to complete.
After the first iteration it will run in a matter of seconds. This is because it
will just be comparing the latest videos against the hash-map until it has come
across 50 videos in a row that are in the hash-map.

For anyone wanting to try the extension it can be accessed [here](https://www.dropbox.com/s/3jqvgvtlv69gmi9/app.tar.gz?dl=0)



Once downloaded unzip the folder, go to the chrome extensions page and select
developer mode. Then select load unpacked extensions and select the unpacked
app folder. Now go to the Youtube history page and run the application.
