---
layout: post
title: What happens at traffic stops?
subtitle: Quit rubbernecking and look here instead
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/path.jpg
tags: [Lambda]
---
## Why I care about traffic stops and so do you
Every time a patrol car gets behind my car my pulse quickens and my palms start to sweat. What did I do?! I begin to quickly go through what I must have done to get pulled over. Then the patrol car smoothly passes me and pulls over someone in front of me. Who is that person? What did that person do? How they are being punished? This post begins to answer these questions.
## About the Data
Data source: http://users.stat.ufl.edu/~winner/data/trafficstop.csv

This dataset is from a large and anonymous city in the southeastern part of the United States, and was pulled from the University of Florida website. University of Florida retrieved the data from data.gov. This dataset was already cleaned, categorized, and ready for analysis. 

This dataset shows the records of all reported traffic stops from a large southeastern city in the United States in 2016. Since this data is only from one city for one year the data is just a sample of what happens at traffic stops. A more thorough analysis of traffic stops and yearly trends in the US is beyond the scope of this post.

[Analysis notebook](https://colab.research.google.com/drive/1mkk8PlMwRqNhetWWzT5IobfXga0dMDQ_#scrollTo=FAQhY9vHU9Mz)

## Who gets stopped?
At the beginning of this project I wanted to look at 
As you can see below the data is clear: the younger you are the more likely you are to be pulled over.

## What caused a traffic stop and what was the result?
As shown in the above below if you are speeding or driving a vehicle without the proper registration you are much more likely to be pulled over. Those two categories combine for over 68% of all traffic stops. 

It seems like for the officers in this city if they are going to take the time to write something down they are going to make it count with 41% of the time the officers issue a citation versus just 4% of the time giving a written warning. Furthermore, the percent of people arrested from a traffic stop is very low at 1.97%. However if you are stopped for a DWI the percent of arrests skyrocket to 75%. 

Although the police seem to have a lot of advertising campaigns on preventing DWIs and wearing your seatbelt this is not reflected in the percent of traffic stops with seatbelts accounting for 0.8% and DWIs for 0.14% of total traffic stops.

![Reason and Result](/assets/img/reason_and_result (3).png)
