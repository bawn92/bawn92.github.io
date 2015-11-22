---
layout: post
title:  "Reinventing online reviews"
date:   2015-10-27 18:11:16
categories: blog
---

Online reviews for products are majorly influencing purchasers buying decisions and 70% of people now consult online reviews prior to purchasing products [Business Week, Oct 2008]. With this being said information overload for reviews is becoming a significant problem for online retailers. The user is presented with a bewildering number of reviews for each product. In order to compare two items throughly and make an informed purchase the user must read multiple reviews to get a fair and overall view of product.

Amazon has tried to solve this by presenting the most helpful and unhelpful reviews. The problem with this scenario is that if the user only reads these two reviews they have no guarantee that these reviews give a fair representation of the overall product. Amazon also provides a section with technical details/features. I believe reviews and features can be combined in a graphical way to provided the purchaser with information that may greatly influence there buying decisions. The method I have devised is to combine both technical details/features with user generated reviews through sentiment analysis, opinion mining and natural language processing with the goal of presenting the results in a honeycomb structure.

The technique I have applied involves analyzing every user review for a product. The features mentioned in each review are then extracted along with the positive, negative or neutral sentiment relating to that feature. The image below shows an example of the extraction.

<img src="https://raw.githubusercontent.com/bawn92/bawn92.github.io/master/assets/img/feature-extraction.png" width="800" height="440"/>

The extraction of sentiment is done by first splitting the text into sentences. Text chunking and part-of-speech (POC) tagging using maximum entropy is also preformed. After the extracting of the features and positive/negative/neutral sentiment a variety of processing techniques are applied to ensure the correct sentiment count for each feature is obtained. The following image is a sample table of the sentiment for the top 10 most talked about features for a given camera. This table was generate from a sub-set of real user reviews from amazon. Neutral sentiment indicates no positive or negative sentiment words appeared in the same sentence as the feature.

<img src="https://raw.githubusercontent.com/bawn92/bawn92.github.io/master/assets/img/totalcount.png" width="800" height="440"/>

Once this table of information has been generated I represent each feature as a hexagon. I vary the size of the hexagon depending on the word count of that feature. I also vary the color depending on the ration of positive and negative sentiment. The equations I generated can be seen in the following picture.

<img src="https://raw.githubusercontent.com/bawn92/bawn92.github.io/master/assets/img/design.png" width="800" height="440"/>

You then output the data in the sentiment table through the above equations. Then you order the hexagons from negative to positive. This achieves the following honeycomb like structure:

<img src="https://raw.githubusercontent.com/bawn92/bawn92.github.io/master/assets/img/honeycomb.jpg" width="800" height="440"/>
