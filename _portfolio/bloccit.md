---
layout: post
title: Bloccit
thumbnail-path: "img/Bloccit.PNG"
short-description: Bloccit is a Reddit like web app where users can post and vote on links and comments.

---

## Summary
A website like Reddit can be implemented using many of the core Rails features. [Bloccit](https://rocky-gorge-8621.herokuapp.com/) is an app modeled after Reddit with the various features relying on the Rails framework in order to gain familiarity with using it.

## Explaination
This project was my introduction to the MVC model and to creating a Rails application from start to finish. It's purpose was to provide a learning experience in which I could begin to gain some fluency working with the Rails framework.

## Problem
Bloccit was build in small sections primarily relying on Test Driven Design to drive the creation of features. The first challenge was getting basic views established. The next issue was to create the underlying models for the application. Finally I needed to tie them together with some basic controllers. Each feature more or less would follow this model and the bulk of issues arose when creating complex relationships, like implementing the ability to label both a topic and a post, each of which is based on separate models.

## Solution
I would start each feature by writing RSpec tests for them. This allowed me to incrementally build out more complex features by giving me quick feedback as to when I was inadvertently breaking something. Because this was a "learning" project users were implemented manually. This meant all authorization was based on enum datatypes and had to be worked into the controllers and models manually. Writing tests for this proved very useful because it allowed me to quickly build more complex roles and refine their access types with little effort. Labeling posts also proved to be difficult but that was due to me struggling conceptually with the idea of polymorphic relationships. Once I gained a better understanding of model interfaces I was able to get that section working.

## Conclusion
I was able to complete the project in less than the allotted amount of time, however I allowed myself to struggle on the labeling section for too long. All RSpec tests pass and from my personal testing the site appears to work well. Other than that though it is lacking in originality and uses almost no styling. While working on this project I started to get the sense that I cannot extrapolate on the time and effort requirements of future work based on conceptually different past work. For example even though I was able to quickly set up the relationship between users and posts, setting up the relationship between labels, posts, and topics took considerably longer. Not planning for this definitely made my initial time estimates wrong.
