---
ID: 1445
post_title: 'America&#8217;s Most Important Algorithm'
author: Shwuzzle
post_date: 2010-12-22 08:39:59
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
<em>"Yesterday the Census Bureau announced the new <a href="http://2010.census.gov/2010census/data/apportionment-data-text.php">apportionment</a> of the 435 representatives to states based on the 2010 census. Illinois  lost one representative. Texas gains four. Not only do these affect the  makeup of the House of Representatives but also the <a href="http://en.wikipedia.org/wiki/Electoral_College_%28United_States%29">Electoral College</a> that chooses the president.

Since 1940 the apportionment is not done by a specific formula but by an algorithm.
</em>
<ul>
	<li><em>Input: Pop, a population array for the 50 states.</em></li>
	<li><em>Output: Rep, a representatives array for the 50 states.</em></li>
	<li><em>Let Rep[i] = 1 for each state i.</em></li>
	<li><em>For j = 51 to 435</em>
<ul>
	<li><em>Let i = arg max Pop[i]/sqrt(Rep[i]*(Rep[i]+1))</em></li>
	<li><em>Rep[i] = Rep[i]+1</em></li>
</ul>
</li>
</ul>
<em> This algorithm called the <a href="http://en.wikipedia.org/wiki/Huntington-Hill_method">Huntington-Hill method</a> or the Method of Equal Proportions, minimizes the relative difference between sizes of congressional districts.
</em>
<em>Check out the Census Bureau video <a href="http://www.youtube.com/watch?v=RUCnb5_HZc0">The Amazing Apportionment Machine</a>."</em>
<div><em>
</em></div>
<div>[youtube]http://www.youtube.com/watch?v=RUCnb5_HZc0[/youtube]</div>
<div></div>
<em>"Implemented naively the running time is O(rn) for n the number of states  and r the number of representatives. I'll leave it to you readers to  find better implementations. Can I compute how many representatives New  Jersey gets from Pop in o(n) space?

Of course with n=50 and r=435 the numbers don't get big enough to cause  any problem at all for today's computers. I wonder how long it took in  1940?</em> " via <a href="http://blog.computationalcomplexity.org/2010/12/americas-most-important-algorithm.html">Computational Complexity: America's Most Important Algorithm (computationalcomplexity.org)</a>
