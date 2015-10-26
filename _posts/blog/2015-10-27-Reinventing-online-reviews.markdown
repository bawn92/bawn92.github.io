---
layout: post
title:  "Reinventing online reviews"
date:   2015-10-27 18:11:16
categories: blog
---

Online reviews for products are majorly influencing purchasers buying decisions and 70% of people consult online reviews prior to purchasing products [Business Week, Oct 2008]. With this being said information overload for reviews is becoming a significant problem for online retailers. How dose a retailer tailer make their review recommendation system show the review the user will find must useful and ultimately having a higher chance of leading that customer to a purchase.

A major problem I have with online reviews is that if you read only the most helpful and unhelpful reviews, how do you how accurate a representation this review is of the entire users bases feelings on a specific features. In order too get this broad understanding of the general feel for specific features you need to read a vast number of both positive and negative reviews. It becomes extremely time consuming and taxing for and average purchaser to sive though huge amounts of reviews.

Amazon always provides a section with technical details/features and another for product reviews. I believe these can be combined to provided the purchaser with information that would be critical in the purchasing decision process. The method I have devised is to combine these two sections through sentiment analysis, opinion mining and natural language processing.

The technique I have applied involves analyzing every user review for a product and selecting the features mentioned in each review and then obtaining the positive, negative or neutral sentiment relating to that feature.

picture

This was accomplished by first splitting the text into sentences. I then performed text chunking and then part-of-speech (POC) tagging using maximum entropy. Once this was complied extracting features and positive or negative sentiment closet to the feature becomes easier. Lots of other pre and post processing techniques are applied to ensure the correct sentiment is taken for each feature. The method I have described is an extremely brief overview.

This image is an example of what the application code produces. This table was generate from real user reviews from amazon. Neutral sentiment indicates no positive or negative sentiment words appeared in the same sentence as the feature.

picture

Once this table of information has been generate it can be displayed to the user in a mirade of different ways. What I decided to do was to select the top 10 most talked about features. I represented each of these features as a hexagon and varyied the size of the hexagon depending on the amount of time it was mentioned and vary the color depending on the ration of positive and negative sentimnt.

Picture picture
