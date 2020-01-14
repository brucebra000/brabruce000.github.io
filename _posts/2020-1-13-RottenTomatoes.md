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

[Here is the machine that will make the predictions](https://colab.research.google.com/drive/1Uy1lae7lP1lcsk9Z3LNDJpG6kjRngbRR)(Made in google colab).

# What do these classifications mean?

Rotten Tomatoe's critic ratings are classified as _Certified Fresh_, _Fresh_, or _Rotten_
based on their critic review scores.

**Certified Fresh** = Critic review score above 70%.  
**Fresh** = Critic review score between 70% and 60%.  
**Rotten** = Critic review score lower than 60%.

# About the data

This dataset contains **16638** movies! Each movie in this dataset contains information about it's critic rating, audience rating,
cast, genre, directors, etc. There is a lot for our machine to look through, but not everything on here will be useful. Categories such as movie poster links and Rotten Tomatoes webpage links won't be necessary, so those will be removed from the data. I also wanted to make the machine predict a movie's critic rating before the movie is released. In a real world senario, this means that we wouldn't have any information regarding the audience, as the movie would have had to been released for them to even see it. Categories such as audience rating and audience count will have to be removed. Those categories also cause data leakage. If the audience gives a movie a high rating, then there is a very good chance that the critics did as well. In fact, the machine would be able to predict a movie's critic rating with 98% accuracy if those categories stayed in!

