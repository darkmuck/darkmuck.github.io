---
ID: 1430
post_title: Automatic Staged Compilation
author: Shwuzzle
post_date: 2010-11-29 16:14:41
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2010/11/29/automatic-staged-compilation/
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
Here is a paper I recently came across which was posted on <a href="http://lambda-the-ultimate.org/">lambda-the-ultimate.org</a>. The paper is titled: <a href="http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.95.6636">Automatic Staged Compilation (2005)</a>. It's a dissertation written by Matthai Philipose of the University of Washington. It seems like an interesting concept. I wonder if we'll see any real implementations in the near future? Here is an except from the paper:

...<em>The past few years have seen the emergence of staged optimization,  which produces run-time optimizations that often have much lower  run-time overhead than traditional optimizers, yet do not sacrifice any  of their functionality. The key to the technique is a method, called  staging, to transfer optimization overhead to static compile time from  run time. Unfortunately, developing staged variants of individual  optimizations has been highly specialized, labor-intensive work; staging  pipelines of optimizations even more so. </em>

<em>This dissertation presents a system called the Staged Compilation  Framework (SCF), which automatically stages entire pipelines of compiler  optimizations at arguably little additional engineering cost beyond  building the slower traditional version of the pipeline. SCF harnesses  two powerful but traditionally difficult-to-use techniques, partial  evaluation and dead-store elimination, to achieve staging. An  implementation of SCF shows that staged compilation can speed up  pipelines of classical compiler optimizations by up to an order of  magnitude, and more commonly by a factor of 4.5 to 5 ....</em>"

<a href="http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.95.6636">Automatic Staged Compilation (2005 - Matthai Philipose)</a>