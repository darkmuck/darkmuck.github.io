---
ID: 1335
post_title: Automatic Rsync Script
author: Shwuzzle
post_date: 2010-09-19 14:44:09
post_excerpt: ""
layout: page
permalink: >
  http://localhost:8080/projects/linux-shell-scripts/auto_rsync/
published: true
aktt_notify_twitter:
  - 'no'
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
---
Version: 2010.09
Download: <a href="http://shwuzzle.com/wp-content/uploads/2010/09/auto-rsync-2010.09.sh.tar">auto-rsync-2010.09.sh.tar</a>

This script will produce incremental backups between two local directories or between directories on remote servers. In essence I guess you could say that this script will mimic the 'core' behavior of Apple's Time Machine software for Mac OS X. Rsync is available on nearly all Unix-compatible operating systems (BSD, linux, solaris, etc.), it is easy to use, and can be automated via a combination of this script and cron.

Use the following code to produce a backup by filling in the appropriate values for each parameter. Alternatively, you can download the complete script here: <a href="http://shwuzzle.com/wp-content/uploads/2010/09/auto-rsync-2010.09.sh.tar">auto-rsync-2010.09.sh.tar</a>
<table style="border: 0pt solid #80807f; background-color: #d6d6d6; width: 505px; height: 157px;" border="0" cellspacing="0" cellpadding="0">
<tbody>
<tr valign="top">
<td>
<pre>#!/bin/bash
now=`date "+%Y-%m-%dT%H_%M_%S"`
dir=/home/username/
username=theusername
server=servername

rsync -azP --delete --delete-excluded --exclude-from=$dir/.rsync/exclude \
--link-dest=../current \
$dir $username@$server:Backups/incomplete_backup-$now &amp;&amp; \
ssh $username@$server "mv Backups/incomplete_backup-$now \
Backups/backup-$now &amp;&amp; rm -f Backups/current &amp;&amp; \
ln -s backup-$now Backups/current"</pre>
</td>
</tr>
</tbody>
</table>