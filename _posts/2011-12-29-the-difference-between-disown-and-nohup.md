---
ID: 1806
post_title: 'The difference between disown, &#038;, and nohup'
author: Shwuzzle
post_date: 2011-12-29 13:55:33
post_excerpt: ""
layout: post
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
<em>&amp;</em> - This causes the application to run in the background. You will get a new shell prompt after issuing this command.

<em>nohup</em> and <em>disown</em> - Both of these prevent <em>SIGHUP</em> (hangup) signals so the application isn't killed when the terminal session is closed. <em>nohup</em> does this when the job starts. <em>disown</em> can be used to make changes to an actively running job.
