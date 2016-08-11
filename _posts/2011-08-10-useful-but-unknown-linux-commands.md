---
ID: 1710
post_title: Useful Lesser-Known Linux Commands
author: Shwuzzle
post_date: 2011-08-10 09:56:55
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
The following quoted text is an excerpt from the article "<em><a href="http://www.anchor.com.au/blog/2011/08/awesome-but-often-unknown-linux-commands-and-tools/">Awesome but often unknown Linux commands and tools (anchor.com.au)</a></em>" which I found really useful! There are quite a few lesser-known Linux/Unix commands that can prove to be extremely useful. This quoted text outlines just a few of these, but there are many more out there...

"<em>1. pgrep and pkill – The first command ‘pgrep’ will return the process id based on a name or other attributes. pkill will signal a process with a matching name or attribute. Want to kill all processes being run by a given user? Issue a pkill -U USERNAME; sure beats the hell out of:

ps -U USERNAME|awk {'print $1'}|xargs kill

2. htop – Much like your regular ‘top’ command, on steriods. Gives an interactive view on your machine right now, but with an ascii visual representation of your CPU, memory and swap utilisation. Often not installed by default, but is packaged under both Red Hat Enterprise Linux and Debian and can be trivially installed on most dedicated and virtual private servers.

3. mytop – Similar to top, but designed specifically for MySQL. Gives you an interactive display of what is happening with your MySQL database, in real time. Information such as what queries are being run, amount of data which is being flowing in and out of the database, number of queries being run per second and number of slow queries. This application is once again packaged with most large common Linux distributions.

4. lsof – This cool little command comes with most Linux Distros as default and allows you to display any files which are currently opened on the system. Especially handy for finding files which have been deleted (and not appearing in the file system) but still resident due to being held open by a current running process.

5. iptraf – Want to know where all your network traffic is going to and coming from? iptraf is a really cool tool which can be used to track this information and let you know what is happening on your server. </em>"
