---
layout: post
title: "Naive Bayes"
date: 2017-08-19
---
Naive Bayes is an ML algorithm that allows you to label the result into classification.

I used Naive Bayes in sentiment analysis. The sentiment analysis example aims toto classify if the comment is  positive or negative. 

My dataset came from three sources, namely: IMDB, Amazon, and Yelp. I downloaded  sources from an online repository and combined them into one. I separated the data into two groups, namely:  features and label. Features refer to the comment in term frequency representation; label refers to positive or negative. Furthermore, features and label are divided into two sections: training and testing. Training refers to data used in "teaching" the model; testing refers to data used in "learning" if the model works after teaching it. Hence, I had training features, training label, testing features, and testing label.

I used scikit-learn to create a model. I imported Naive Bayes from the package and fit the training features and training label using the algorithm. This led to a model named classifier. The classifier is then fed with testing features and testing label. The final step led to my realization that the model's prediction is not perfect but fascinating to discover.