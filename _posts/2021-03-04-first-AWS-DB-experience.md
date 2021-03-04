---
layout: post
title: First Experience Using AWS
subtitle: Planning the architecture, building a database, and deploying an API
cover-img: /assets/img/database.jpg
#thumbnail-img: /assets/img/thumb.png
#share-img: /assets/img/database.jpg
tags: [Lambda]
---
## Why this project?
Human Right First is a nonprofit with a mission of upholding human rights and fighting for freedom around the globe. One of their apps highlights incidents of police brutality specifically at protests in the United States. For this project, the goal was to get a more comprehensive and robust data collection method for use in the app. Currently, the only source of data to the app was through Police Brutality 2020 where the data is manually crowdsourced through volunteers.

## What is the scope of work?
The project goal of getting more comprehensive data of all the incidents taking place was to be accomplished using Twitter. The plan was to acquire data using the Twitter API. Then, classify that data using a machine learning algorithm and get the incidents classified as police brutality to the app.

My role in the project team was to verify that the current source of data would smoothly combine with the new Twitter source and also build a way to transfer data between the data science team and the app.

## What were the technical challenges?
There were many questions:
How would we store the tweets that had been classified by the model?
Do we need a database? If we use a database what kind should be used?
Do we need an API?
How do I even build an API??

The first problem to solve was how the data was going to flow from our sources to the app. The current way that data was being transferred was through the use of a CSV file that was generated, sent to the app, and then deleted once a day. 

Another issue was that the existing codebase had multiple files with functions that were over two hundred lines of code that were not working.

## How were these challenges resolved?
An API connected to a database seemed to be the best solution to send data to the app. This method would increase the automation and scalability of the data retrieval process for the app. Here is a simple flowchart of the architecture:

![Data Science Architecture](https://raw.githubusercontent.com/n8mcdunna/human-rights-first-ds-labs31/main/DS-Flow%20Chart.png)


A  FastAPI would be deployed using Elastic Beanstalk from AWS and a Postgres database would be set up using Amazon RDS. Our app only needed to store a small amount of data and handle a small number of users. Therefore the app did not need a specialized transactional or analytical database so a Postgres database was chosen.

For the API, A FastAPI was chosen because it has a simple and easy-to-use routing system, uses a standardized OpenAPI schema, and is just fast.  Also, the built-in connection tools the API provided would be much better than the current situation of using a CSV file. 

Now that a plan for the data architecture had formed I began the implementation phase. Except…  the existing codebase still had those huge functions full of bugs. 

So I dug into removing redundant code and breaking the huge functions into small easily readable and usable functions. Fortunately, this process taught me many useful details about how the data currently in use was being processed and the existing codebase. Then it was on to creating the database and deploying the API.

Database tables were created using the psycopg2 python library. API routes were created using FastAPI and tested locally. Then the errors began during the API deployment. First a module import error, then an environment variable error, then a spacy installation error. After carefully studying the AWS error logs, reviewing documentation, and multiple redeployment attempts the API was successfully deployed to AWS servers in Virginia! 

## What are the next steps to improving this project?
Currently, the machine-learning model sends several hundred incidents for an administrator to review before the incidents are displayed on the app. Many of these incidents are false positives and need to be filtered out before being sent to the dashboard of the administrator. Also, there are many tweets that create duplicates of the same police brutality incident. These duplicates need to be found and removed.

For more content like this check out [my github](https://github.com/n8mcdunna) and [my medium account](https://medium.com/@n8.mcdonough)
