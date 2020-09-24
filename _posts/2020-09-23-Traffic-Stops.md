---
layout: post
title: What happens at traffic stops?
subtitle: Quit rubbernecking and look here instead
cover-img: /assets/img/path.jpg
#thumbnail-img: /assets/img/thumb.png
#share-img: /assets/img/path.jpg
tags: [Lambda]
---
## Why I care about traffic stops and so do you
Every time a patrol car gets behind my car my pulse quickens and my palms start to sweat. What did I do?! I begin to quickly go through what I must have done to get pulled over. Then the patrol car smoothly passes me and pulls over someone in front of me. Who is that person? What did that person do? How they are being punished? This post begins to answer these questions.
## About the Data
Here is the [raw data.](http://users.stat.ufl.edu/~winner/data/trafficstop.csv)

Here is the [analysis notebook.](https://colab.research.google.com/drive/1mkk8PlMwRqNhetWWzT5IobfXga0dMDQ_#scrollTo=FAQhY9vHU9Mz)

This dataset was pulled from the University of Florida website. University of Florida retrieved the data from data.gov. This dataset was already cleaned and ready for analysis. 

This dataset shows the records of all reported traffic stops from a large southeastern city in the United States in 2016. Since this data is only from one city for one year the data is just a sample of what happens at traffic stops. A more thorough analysis of traffic stops and yearly trends in the US is beyond the scope of this post.
## Who gets stopped?
 
As you can see below there is a clear decline in traffic stops related to the age of the driver. Teen drivers do not have many stops. This is probably because they are only legally allowed to drive for a few years whereas the other age groups account for ten years of stops. This also explains why rental agencies and insurance companies charge higher rates for people in their 20s.

![Age Group](/assets/img/age_groups.png){: .mx-auto.d-block :}

## What caused a stop and what was the result?
So, why are people in their 20s getting stopped? The graph below shows the answer, and the answer is pretty boring with the number one reason being vehicle registration. The data shows that the older you are the more stops you have for speeding, although teens lead the speeding category with about 35% of their stops being speeding related. Another reason the percentage of speeding stops increases with age could be because the vehicle registration percentage decreases as drivers get more disciplined in keeping track of their registration.

![Age Group and Result](/assets/img/age_group_and_result (1).png){: .mx-auto.d-block :}

As shown in the graph below if you are speeding or driving a vehicle without the proper registration you are much more likely to be pulled over. Those two categories combine for over 68% of all traffic stops. Both of these offenses are easily visible to a patrolling officer which could lead to their high rates. 

It seems like for the officers in this city if they are going to take the time to write something down they are going to make it count. The officers issue a citation 41% of the time versus just giving a written warning 4% of the time. 

The percent of people arrested from a traffic stop is very low at 1.97%. However if you have the misfortune of being stopped on suspicion of DWI the percent of arrests skyrocket to 75%. 

The police seem to have a lot of advertising campaigns in the southeastern city that I live in (which may or may not be the city represented by the data) for preventing DWIs and wearing your seatbelt this is not reflected in the percent of traffic stops. Seatbelts accounted for 0.8%, and DWIs for a measly 0.14% of total traffic stops.

![Reason and Result](/assets/img/reason_and_result (4).png){: .mx-auto.d-block :}

# Conclusion
Keep your vehicle registration up to date, be careful about speed limits, and be extra careful if you are in your 20s!
