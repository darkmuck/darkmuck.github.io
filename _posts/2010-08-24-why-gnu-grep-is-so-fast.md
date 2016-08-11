---
ID: 1242
post_title: Why GNU Grep is so fast
author: Shwuzzle
post_date: 2010-08-24 07:50:22
post_excerpt: ""
layout: post
published: true
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
---
GNU Grep has been around for decades. This is a common *nix tool for searching named input files for lines containing a match to a given pattern. The original author, Mike Haertel, has a post on the FreeBSD mailing list describing why its so far compared to the BSD implementation of Grep. There are a couple of tricks that GNU Grep performs, namely the use of the well known Boyer-Moore algorithm. This algorithm looks for the last letter of a target string and then uses a lookup table to see how far ahead it can skip in the input when it finds a non-matching character. In addition, GNU Grep avoids breaking the input into lines, which would slow grep down because it has to look for every byte. There are more details on why GNU Grep is so fast; check out the links and other resources below.

Check out the <a href="http://lists.freebsd.org/pipermail/freebsd-current/2010-August/019310.html">full message here</a> via the <a href="http://docs.freebsd.org/mail/">FreeBSD mailing list archives</a>.

Additional Information:
<ul>
	<li><a href="http://en.wikipedia.org/wiki/Boyer-Moore">Boyer-Moore String Search Algorithm</a></li>
	<li><a href="http://unixhelp.ed.ac.uk/CGI/man-cgi?grep">GNU grep man page</a></li>
	<li><a href="http://portal.acm.org/citation.cfm?id=137560">"Fast String Searching", by Andrew Hume and Daniel Sunday</a></li>
</ul>
