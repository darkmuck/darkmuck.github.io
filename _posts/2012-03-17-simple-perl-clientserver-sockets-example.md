---
ID: 1849
post_title: >
  Simple Perl Client/Server Sockets
  Example
author: Shwuzzle
post_date: 2012-03-17 17:38:41
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2012/03/17/simple-perl-clientserver-sockets-example/
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
Here is a very simple client/server example coded in Perl. This is an extremely basic application - the goal was merely for me to learn how to use sockets in Perl. You can check out the code on github here: <a href="https://github.com/darkmuck/SimplePerlSockets">github.com/darkmuck/SimplePerlSockets</a>.

After you've downloaded the client and server files follow these instructions to test it out:
<ol>
	<li>Open two terminal windows</li>
	<li>From the first terminal, run these commands:</li>
<ol>
	<li>$ chmod a+x server.pl;perl server.pl 1234;</li>
</ol>
	<li>From the second terminal, run these commands:</li>
<ol>
	<li>$ chmod a+x client.pl;perl client.pl localhost 1234</li>
</ol>
	<li>From the second terminal window (client) try to type any word(s) and press enter. You should see the result transmitted to terminal window #1 (server).</li>
</ol>