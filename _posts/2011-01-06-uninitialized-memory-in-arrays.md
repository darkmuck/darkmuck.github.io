---
ID: 1506
post_title: Uninitialized Memory in Arrays
author: Shwuzzle
post_date: 2011-01-06 13:55:13
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2011/01/06/uninitialized-memory-in-arrays/
published: true
aktt_notify_twitter:
  - 'yes'
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
aktt_tweeted:
  - "1"
---
This is a really neat trick that has been around for over 30 years. With an array, you can leave values uninitialized and then read during normal operation and your code will work properly no matter what junk data is in the array. I may try to implement this using C or Perl just for fun. If you want to read more about how it works and what the arrays look like check out the full article below.

<a href="http://research.swtch.com/2008/03/using-uninitialized-memory-for-fun-and.html">Using Uninitialized Memory for Fun and Profit (research.swtch.com)</a>