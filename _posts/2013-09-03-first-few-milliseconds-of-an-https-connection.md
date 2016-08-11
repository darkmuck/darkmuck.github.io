---
ID: 2039
post_title: >
  First Few Milliseconds of an HTTPS
  Connection
author: Shwuzzle
post_date: 2013-09-03 15:38:35
post_excerpt: ""
layout: post
published: true
snap_isAutoPosted:
  - "1"
snapEdIT:
  - "1"
snapFB:
  - 's:188:"a:1:{i:0;a:5:{s:4:"doFB";s:1:"1";s:8:"PostType";s:1:"A";s:10:"AttachPost";s:1:"1";s:10:"SNAPformat";s:51:"New post (%TITLE%) has been published on %SITENAME%";s:11:"isPrePosted";s:1:"1";}}";'
snapTW:
  - 's:126:"a:1:{i:0;a:4:{s:4:"doTW";s:1:"1";s:10:"SNAPformat";s:15:"%TITLE% - %URL%";s:8:"attchImg";s:1:"0";s:11:"isPrePosted";s:1:"1";}}";'
---
What actually happens behind the scenes of a HTTPS connection?

"<em>Client Hello. TLS wraps all traffic in "records" of different types. We see that the first byte out of our browser is the hex byte 0x16 = 22 which means that this is a "handshake" record. </em>

<em>The next two bytes are 0x0301 which indicate that this is a version 3.1 record which shows that TLS 1.0 is essentially SSL 3.1.</em>

<em>The handshake record is broken out into several messages. The first is our "Client Hello" message (0x01). There are a few important things here....." (continued in full article link below)"</em>

full article: <a href="http://www.moserware.com/2009/06/first-few-milliseconds-of-https.html?repost!&amp;utm_source=Coder+Weekly">The First Few Milliseconds of an HTTPS Connection</a>
