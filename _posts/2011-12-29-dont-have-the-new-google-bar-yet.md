---
ID: 1792
post_title: 'Don&#8217;t have the new Google bar yet?'
author: Shwuzzle
post_date: 2011-12-29 11:26:53
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2011/12/29/dont-have-the-new-google-bar-yet/
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
By now most users should have the new Google bar, however if you don't follow these instructions.

If you are using Google Chrome right click on any whitespace on a Google page and select "Inspect Element". Click on the Console tab and paste the following text and press enter.
<table style="width: 300px; background-color: #cccacd; border-width: 0px; border-color: #000000; border-style: solid;" border="0" align="left">
<tbody>
<tr>
<td><span style="font-size: x-small;">document.cookie="PREF=ID=03fd476a699d6487:U=88e8716486ff1e5d:FF=0:LD=en:</span>
<span style="font-size: x-small;">CR=2:TM=1322688084:LM=1322688085:S=McEsyvcXKMiVfGds; path=/; domain=.google.com";</span>
<span style="font-size: x-small;">window.location.reload();</span></td>
</tr>
</tbody>
</table>
&nbsp;

&nbsp;

Congratulations, you should now see the new Google bar at the top of the page!