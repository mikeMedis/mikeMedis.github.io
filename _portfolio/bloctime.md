---
layout: post
title: Bloc Time
thumbnail-path: "img/bloctime.png"
short-description: Pomodoro timer and TODO list

---

{:.center}
![]({{ site.baseurl }}/img/bloctime.png)
Pomodoro timer and a tasks list.

{:.center}
* [See code on Github](https://github.com/mikeMedis/bloctime){:target="_blank"}



## Explanation

The pomodoro timer was the influence of the designed and developed Bloc Time SPA. The timer will count down from 25 minutes to zero, with 5 minute breaks (on prompts), then after four work sessions, users will have the option for a 30 minute break. Also included is a working task list to stay on top of TODO items while using the pomodoro technique.


## Problem

I wanted my pomodoro application to be a representation on what it felt like to be working at the users desk and writing tasks down on a piece of notebook paper. The background was set then set to a piece of notebook paper with the timer in the middle. Users would also be able to save a task that they are working on during that session, and review the list as they work durning the session sand also during the break (not advised) this is in the upper left hand corner with a list of tasks.

## Solution

The application was developed with AngularJS and UI-Router. I created a custom controller for the timer, which controls the countdown mechanism. Using John Papas [angular-styleguide](https://github.com/johnpapa/angular-styleguide) from Github I separated all functionally to individual controllers to organize my code. Firebase/AngularFire provided the database system for users to upload/save a list of tasks completed during their work sessions.

## Conclusion

This application had several different parts which made it challenging and fun to work on. I especially enjoyed developing the timer controller, applying different CSS styles to the body and creating a responsive SPA. The SPA is now a functional pomodoro timer that I now use in my own personal development.
