---
layout: post
title: Get It Done
thumbnail-path: "img/pomodoro.png"
short-description: Pomodoro timer. Design and Development. Javascript and AngularJS with Firebase/AngularFire

---

{:.center}
![]({{ site.baseurl }}/img/pomodoro.png)

AngularJS with AngularFire, Javascript, and jQuery.

{:.center}
[See code on Github](https://github.com/saraguittarclark/pomodoro-app){:target="_blank"}

[See SPA on Heroku](https://evening-oasis-30686.herokuapp.com/){:target="_blank"}

## Explanation

I designed and developed a Pomodoro SPA. The timer will count down from 25 minutes to zero, with 5 minute breaks (on prompts), then after four work sessions, users will have the option for a 30 minute break.

{:.center}
![]({{ site.baseurl }}/img/pomodoro-ss/party-finished.png)

## Problem

I wanted my pomodoro application to be a little different visually, but maintain the same functionality as others available to users. I wanted the application to change background colors (depending on the timer and timer state), and show images at different times to help motivate users. Users would also be able to save a task that they are working on during that session, and review the list as they are working.

{:.center}
![]({{ site.baseurl }}/img/pomodoro-ss/vangogh-break.png)

## Solution

The application was developed with AngularJS and UI-Router. I created two states - the timer/working state, and the "FAQ" state, which has links to information regarding the Pomodoro method, as well as citations for the images used. I created a custom controller for the timer, which controlled the countdown mechanism and images, quotes, and background styles.

Firebase/AngularFire provided the database system for users to upload/save a list of tasks completed during their work sessions.

{:.center}
![]({{ site.baseurl }}/img/pomodoro-ss/bird-finished.png)

## Conclusion

This application had several different parts which made it challenging and fun to work on. I especially enjoyed developing the timer controller, applying different CSS styles to the body, creating a responsive SPA, and working on displaying different images for different timer states.

{:.center}
![]({{ site.baseurl }}/img/pomodoro-ss/leyster-break.png)
