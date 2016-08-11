---
ID: 1855
post_title: >
  What every programmer should know about
  security
author: Shwuzzle
post_date: 2012-05-07 14:52:22
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2012/05/07/what-every-programmer-should-know-about-security/
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
There's an excellent thread going on over at stackoverflow.com about suggestions for what every programmer should know about security.

Some of the more interesting highlights:
<blockquote>
<ul>
	<li><em><strong>Never trust user input!</strong></em></li>
	<li><em><a href="http://www.ibm.com/developerworks/library/l-sp2.html">Validate input</a> from all untrusted sources - use whitelists not blacklists</em></li>
	<li><em>Plan for security from the start - it's not something you can bolt on at the end</em></li>
	<li><em>Keep it simple - complexity increases the likelihood of security holes</em></li>
	<li><em>Keep your <a href="http://en.wikipedia.org/wiki/Attack_surface">attack surface</a> to a minimum</em></li>
	<li><em>Make sure you <a href="http://www.owasp.org/index.php/Fail_securely">fail securely</a></em></li>
	<li><em>Use <a href="https://buildsecurityin.us-cert.gov/bsi/articles/knowledge/principles/347-BSI.html">defence in depth</a></em></li>
	<li><em>Adhere to the principle of <a href="https://buildsecurityin.us-cert.gov/bsi/articles/knowledge/principles/351-BSI.html">least privilege</a></em></li>
	<li><em>Use <a href="http://www.owasp.org/index.php/Threat_Risk_Modeling">threat modelling</a></em></li>
	<li><em><a href="http://www.cgisecurity.com/owasp/html/ch04s09.html">Compartmentalize</a> - so your system is not all or nothing</em></li>
	<li><em>Hiding secrets is hard - and secrets hidden in code won't stay secret for long</em></li>
	<li><em>Don't write your own crypto</em></li>
	<li><em>Using crypto doesn't mean you're secure (attackers will look for a weaker link)</em></li>
	<li><em>Be aware of <a href="http://www.linuxjournal.com/article/6701">buffer overflows</a> and how to protect against them</em></li>
</ul>
<em>There are some excellent books and articles online about making your applications secure:</em>
<ul>
	<li><em><a href="http://rads.stackoverflow.com/amzn/click/0735617228"><strong>Writing Secure Code 2nd Edition</strong></a> - I think every programmer should read this</em></li>
	<li><em><a href="http://rads.stackoverflow.com/amzn/click/020172152X">Building Secure Software: How to Avoid Security Problems the Right Way </a></em></li>
	<li><em><a href="http://rads.stackoverflow.com/amzn/click/0596003943">Secure Programming Cookbook</a></em></li>
	<li><em><a href="https://docs.google.com/viewer?url=http://www.usenix.org/events/sec04/tech/slides/mcgraw.pdf">Exploiting Software</a></em></li>
	<li><em><a href="http://www.cl.cam.ac.uk/%7Erja14/book.html">Security Engineering</a> - an excellent read</em></li>
	<li><em><a href="http://www.dwheeler.com/secure-programs/Secure-Programs-HOWTO/index.html">Secure Programming for Linux and Unix HOWTO</a></em></li>
</ul>
</blockquote>
&nbsp;

Check out the full discussion here: <a href="http://stackoverflow.com/questions/2794016/what-should-every-programmer-know-about-security">What should every programmer know about security? (via stackoverflow.com)</a>
<br />&nbsp;