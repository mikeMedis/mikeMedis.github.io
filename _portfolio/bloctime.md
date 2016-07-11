---
layout: post
title: Bloc Time
thumbnail-path: "img/bloctime.png"
short-description: Pomodoro timer. Design and Development. Javascript and AngularJS with Firebase/AngularFire

---

{:.center}
![]({{ site.baseurl }}/img/bloctime.png)
AngularJS with AngularFire, Javascript, and jQuery.  [See code on Github](https://github.com/mikeMedis/blocipedia){:target="_blank"}



## Explanation

I designed and developed a Pomodoro SPA. The timer will count down from 25 minutes to zero, with 5 minute breaks (on prompts), then after four work sessions, users will have the option for a 30 minute break.


## Problem

I wanted my pomodoro application to be a representation on what it felt like to be working the background was set as a piece of notebook paper with the timer in the middle. Users would also be able to save a task that they are working on during that session, and review the list as they are working, that would be in the upper right hand corner with a list of todos.

## Solution

The application was developed with AngularJS and UI-Router.  I created a custom controller for the timer, which controlled the countdown mechanism and separated most of the functionality so I would have one controller for each purpose in the application.

Firebase/AngularFire provided the database system for users to upload/save a list of tasks completed during their work sessions.



## Conclusion

This application had several different parts which made it challenging and fun to work on. I especially enjoyed developing the timer controller, applying different CSS styles to the body and creating a responsive SPA.
