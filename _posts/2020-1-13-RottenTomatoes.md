---
layout: post
title: Rotten Tomatoes
subtitle: Predicting Movie Ratings
tags: [Machine Learning]
comments: true
---

I've created a machine that will try to predict a movie's critic rating will be classified as _Certified Fresh_, _Fresh_, or _Rotten_
on the website [Rotten Tomatoes](https://www.rottentomatoes.com/)!

![Certified Fresh](https://hips.hearstapps.com/digitalspyuk.cdnds.net/17/31/1501854760-certified-fresh.png?resize=480:*){: .center-block :}

The dataset that was used for this project was posted by [Stefano Leone](https://www.kaggle.com/stefanoleone992)
and can be found [here](https://www.kaggle.com/stefanoleone992/rotten-tomatoes-movies-and-critics-datasets).

[Here is the machine that will make the predictions](https://colab.research.google.com/drive/1Uy1lae7lP1lcsk9Z3LNDJpG6kjRngbRR). 

Most of what I will be talking about will appear in this google colab link.

# What do these classifications mean?

Rotten Tomatoe's critic ratings are classified as _Certified Fresh_, _Fresh_, or _Rotten_
based on their critic review scores.

**Certified Fresh** = Critic review score above 70%.  
**Fresh** = Critic review score between 70% and 60%.  
**Rotten** = Critic review score lower than 60%.

# About the data

This dataset contains **16638** movies! Each movie in this dataset contains information about it's critic rating, audience rating,
cast, genre, directors, etc. There is a lot for our machine to look through, but not everything on here will be useful. Categories such as movie poster links and Rotten Tomatoes webpage links won't be necessary, so those will be removed from the data. I also wanted to make the machine predict a movie's critic rating before the movie is released. In a real world senario, this means that we wouldn't have any information regarding the audience, as the movie would have had to been released for them to even see it. Categories such as audience rating and audience count will have to be removed. Those categories also cause data leakage. If the audience gives a movie a high rating, then there is a very good chance that the critics did as well. In fact, the machine would be able to predict a movie's critic rating with 98% accuracy if those categories stayed in!

# Popular cast members

Lets dig through the cast column and count up every actor! I want to manufacture a column that will display how many popular actors appear in each movie. If a movie has a high number of popular actors, it may help make the machine make more accurate predictions. If an actor appears in, lets say, 30 or more movies, then we will consider them a popular actor. First I created a library that will store every actor's name in the entire dataset. Every time a name shows up twice, that actors movie count will tally up by 1. Once I've finished reading through the whole cast column to collect every actor's name, I singled out every actor that appeared in 30 or more movies and put them in their own library. I read through the cast column again and compared it to the new library. Every time an actor's name appeared who was also in our popular actor's library, the number in our new _popularactor_ column would go up. Now that we have finished, we can see that a movie such as _12 Angry Men_ has 2 actors that appear in 30 or more movies!

# The Results

With everything sorted out, I traied the model and made the predictions. The machine can guess a movie's critic review score about **54.5%** of the time! Lets see what features our model found important.

![Feature Importance](https://prnt.sc/qncukz){: .center-block :}
