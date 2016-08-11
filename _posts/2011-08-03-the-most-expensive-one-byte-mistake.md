---
ID: 1706
post_title: The Most Expensive One Byte Mistake
author: Shwuzzle
post_date: 2011-08-03 07:44:25
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2011/08/03/the-most-expensive-one-byte-mistake/
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
"<em>The best candidate I have been able to come up with is the C/Unix/Posix use of NUL-terminated text strings. The choice was really simple: Should the C language represent strings as an address + length tuple or just as the address with a magic character (NUL) marking the end? This is a decision that the dynamic trio of Ken Thompson, Dennis Ritchie, and Brian Kernighan must have made one day in the early 1970s, and they had full freedom to choose either way. I have not found any record of the decision, which I admit is a weak point in its candidacy: I do not have proof that it was a conscious decision.</em>

<em>As far as I can determine from my research, however, the address + length format was preferred by the majority of programming languages at the time, whereas the address + magic_marker format was used mostly in assembly programs. As the C language was a development from assembly to a portable high-level language, I have a hard time believing that Ken, Dennis, and Brian gave it no thought at all.</em>

<em>Using an address + length format would cost one more byte of overhead than an address + magic_marker format, and their PDP computer had limited core memory. In other words, this could have been a perfectly typical and rational IT or CS decision, like the many similar decisions we all make every day; but this one had quite atypical economic consequences.</em>"

<a href="http://queue.acm.org/detail.cfm?id=2010365">The Most Expensive One-Byte Mistake (queue.acm.org)</a>