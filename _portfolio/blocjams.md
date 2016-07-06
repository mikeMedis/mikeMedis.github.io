---
layout: post
title: Training Project Javascript/JQuery/Angular - BlocJams
thumbnail-path: "img/blocjams.png"
short-description: Music player. Javascript and AngularJS Development.

---

{:.center}
![]({{ site.baseurl }}/img/blocjams.png)

Javascript, jQuery, and AngularJS, with Buzz HTML5 Sound Library.

{:.center}
[See code on Github](https://github.com/saraguittarclark/bloc-jams-angular){:target="_blank"}

## Explanation

BlocJams is a fully functional music player, built first with vanilla Javascript, then refactored with jQuery and AngularJS. Songs can be skipped, replayed, muted and unmuted. HTML5 Buzz library was used to support music playback (along with a variety of other functions).

## Problem

BlocJams is a browser-only clone of Spotify/Amazon Music. The SPA has three states - a landing state for new visitors, a collection state that shows available album(s) to select, and an album state in which users could play an album. A player bar, available at the bottom of the album state, would let users change the volume, skip or replay songs, adjust volume, and see information about the song that is playing.

## Solution

BlocJams' SongPlayer service does the majority of the heavy lifting in this Angular SPA. Through this (custom) Angular service, songs from the available album are stopped/started, muted/unmuted, and skipped or replayed. I added an autoplay feature for the application, which directs the songs to play one after another. The custom Seek-Bar directive allows the user to adjust volume and song playback position from the player bar.

## Conclusion

BlocJams provides a quality user experience with a sample album, and it would be nice to expand this application (someday) into a cloud/web based music storage solution.
