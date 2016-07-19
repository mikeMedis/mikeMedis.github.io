---
layout: post
title: Bloc Marks
thumbnail-path: "img/blocmarks.png"
short-description: BlocMarks is a social bookmarking application for finding and sharing your favorite URLs with your friends online.

---

{:.center}
![]({{ site.baseurl }}/img/blocmarks.png)
Bloc Marks is a social bookmarking application for finding and sharing your favorite URLs with your friends online.

{:.center}
* [See code on Github](https://github.com/mikeMedis/blocmarks){:target="_blank"}

## Explanation

Bloc Marks is also a Ruby on Rails application that uses a native browser to share the users favorite bookmarks with other users. Bloc Marks makes sharing the users favorite bookmarked sites with their friends, coworkers, and even their family a very simple job. Establishing an organizational method with each bookmarked URL by topic makes the user experience as effort-free as possible. Making bookmarking a social experience by offering public access to the user's favorite websites.

## Problem

It is easy enough to bookmark a URL in your browser, but eventually your bookmark library may get cluttered and it may require effort to manage bookmarks. It would be nice to have the ability to share bookmarks with friends. That is not something you can do easily from your native browser.

## Solution

The BlocMarks application will solve this problem so that users can have their own bookmarks organized by topic as well as have them shared to other users adding the ability to like and dislike as well.

## Results

Achieving the desired results, I first used Devise a ruby gem to have a user sign up and authentic who they were in order to gain access in to the web application.

## Conclusion

Authenticating users to gain access into the web application. Users were associated with topics through the use of ```ActiveRecord``` in the Rails framework. Also using the ```ActiveRecord``` to associate bookmarks with topics.

{:.center}
``` ruby
class Topic < ActiveRecord::Base
	belongs_to: :user
	has_many :bookmarks
end
```
