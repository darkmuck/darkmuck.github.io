---
ID: 1879
post_title: How Computers Boot Up
author: Shwuzzle
post_date: 2013-01-12 23:08:03
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2013/01/12/how-computers-boot-up/
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
Here is a somewhat lengthy but very good in-depth description of how an x86 machine boots up from the point you hit the power button until the operating system kernel initializes.

<a href="http://shwuzzle.com/wp-content/uploads/2013/01/bootProcess.png"><img class="alignnone  wp-image-1880" title="bootProcess" src="http://shwuzzle.com/wp-content/uploads/2013/01/bootProcess.png" alt="" width="472" height="169" /></a>

"<em>Things start rolling when you press the power button on the computer (no! do tell!). Once the motherboard is powered up it initializes its own firmware – the chipset and other tidbits – and tries to get the CPU running. If things fail at this point (e.g., the CPU is busted or missing) then you will likely have a system that looks completely dead except for rotating fans. A few motherboards manage to emit beeps for an absent or faulty CPU, but the zombie-with-fans state is the most common scenario based on my experience. Sometimes USB or other devices can cause this to happen: unplugging all non-essential devices is a possible cure for a system that was working and suddenly appears dead like this. You can then single out the culprit device by elimination.</em> If all is well the CPU starts running..... (continued in the article linked below)"

<a href="http://duartes.org/gustavo/blog/post/how-computers-boot-up">How Computers Boot Up (duartes.org)</a>