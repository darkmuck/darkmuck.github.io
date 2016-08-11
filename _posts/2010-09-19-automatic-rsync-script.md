---
ID: 1354
post_title: Automatic Rsync Script
author: Shwuzzle
post_date: 2010-09-19 14:54:43
post_excerpt: ""
layout: post
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
I've been messing around with rsync lately on one of my linux machines. I've been looking for a simple solution that would provide something similar to Apple's Time Machine software. There are obviously some open source packages that could provide this functionality for me, but I just wanted something really simple that could be automated. I came up with a script which utilizes rsync and is automated with cron. This script will produce incremental backups between two local directories or between directories on remote servers. In essence I guess you could say that this script succeeds in mimicing the 'core' behavior of Apple's Time Machine software for Mac OS X. Rsync is available on nearly all Unix-compatible operating systems (BSD, linux, solaris, etc.), it is easy to use, and can be automated via a combination of this script and cron.

<a href="http://shwuzzle.com/projects/linux-shell-scripts/auto_rsync/">Check out the full script and more information: Automatic Rsync Script</a>
