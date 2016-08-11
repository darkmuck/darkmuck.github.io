---
ID: 1842
post_title: Never Throw Away Old Code
author: Shwuzzle
post_date: 2012-03-12 09:15:48
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
source: <a href="http://www.joelonsoftware.com/articles/fog0000000069.html">Things You Should Never Do, Part I (joelonsoftware.com)</a>

For many reasons, it is almost never a good idea to throw away old code. It may seem like a good idea to start from fresh if the existing code base is bloated, slow, hard to maintain, etc. However, by starting from fresh you are losing many many things. Some of the most notable reasons to keep your old code around are:
<ul>
	<li>You may not do better the second time and what you've already done</li>
	<li>The old code has been used and is (most likely) proven</li>
	<li>You may lose out on days, weeks, months, or even years of bug fixes and testing</li>
	<li>If its a commercial product, you lose out on your current market position/leadership</li>
</ul>
You might not even need to throw away the entire code base; you may be able to get away with rewriting/refactoring only certain parts of it. This could most likely be more efficient than starting over from nothing.

However, if your code is experimental or very small you may be able to more easily justify throwing it away. In these cases you would more easily be able to improve an algorithm(s) or implement new ideas (if starting from scratch).
