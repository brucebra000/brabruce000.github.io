---
layout: post
title: Rotten Tomatoes
subtitle: Predicting Movie Ratings
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [Machine Learning]
comments: true
---

I've created a machine that will try to predict a movie's critic rating will be classified as _Certified Fresh_, _Fresh_, or _Rotten_
on the website [Rotten Tomatoes](https://www.rottentomatoes.com/)!

![Certified Fresh](https://hips.hearstapps.com/digitalspyuk.cdnds.net/17/31/1501854760-certified-fresh.png?resize=480:*){: .center-block :}

The dataset that was used for this project was posted by [Stefano Leone](https://www.kaggle.com/stefanoleone992)
and can be found [here](https://www.kaggle.com/stefanoleone992/rotten-tomatoes-movies-and-critics-datasets).

[Here is the machine that will make the predictions](https://colab.research.google.com/drive/1Uy1lae7lP1lcsk9Z3LNDJpG6kjRngbRR).

# What do these classifications mean?

Rotten Tomatoe's critic ratings are classified as _Certified Fresh_, _Fresh_, or _Rotten_
based on their critic review scores.

**Certified Fresh** = Critic review score above 70%.  
**Fresh** = Critic review score between 70% and 60%.  
**Rotten** = Critic review score lower than 60%.
