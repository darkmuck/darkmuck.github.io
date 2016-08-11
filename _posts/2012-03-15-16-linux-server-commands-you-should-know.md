---
ID: 1846
post_title: 16 Linux Server Commands You Should Know
author: Shwuzzle
post_date: 2012-03-15 08:33:19
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2012/03/15/16-linux-server-commands-you-should-know/
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
original source: <a href="http://h30565.www3.hp.com/t5/Feature-Articles/16-Linux-Server-Monitoring-Commands-You-Really-Need-To-Know/ba-p/1936">16 Linux Server Monitoring Commands You Really Need To Know</a>
<h3>iostat</h3>
The <a href="http://www.cyberciti.biz/tips/linux-disk-performance-monitoring-howto.html" rel="nofollow" target="_blank">iostat</a> command shows in detail what your storage subsystem is up to. You usually use <tt>iostat</tt> to monitor how well your storage sub-systems are working in general and to spot slow input/output problems before your clients notice that the server is running slowly. Trust me, you want to spot these problems before your users do!
<h3>meminfo and free</h3>
<a href="http://www.redhat.com/advice/tips/meminfo.html" rel="nofollow" target="_blank">Meminfo</a> gives you a detailed list of what's going on in memory. Typically you access meminfo's data by using another program such as <tt>cat</tt> or <tt>grep</tt>. For example,

<tt>cat /proc/meminfo</tt>

gives you the details of what's going on in your server’s memory at any given moment.

For a quick “just the facts” look at memory, you can use the <tt>free</tt> command. In short, <tt>free</tt> gives you the overview; <tt>meminfo</tt> gives you the details.
<h3>mpstat</h3>
The <a href="http://linuxcommand.org/man_pages/mpstat1.html" rel="nofollow" target="_blank">mpstat</a> command reports on the activities of each of the available CPUs on a multi-processor server. These days, thanks to <a href="http://h30565.www3.hp.com/t5/Feature-Articles/What-Does-x86-Need-to-Compete-With-RISC/ba-p/1222" target="_blank">multi-core processors</a>, that’s almost all servers. <tt>mpstat</tt> also reports on the average activities of all your server's CPUs. It enables you to display overall CPU statistics per system or per processor. This overview can alert you to possible application problems before they get to the point of annoying users.
<h3>netstat</h3>
<a href="http://www.thegeekstuff.com/2010/03/netstat-command-examples/" rel="nofollow" target="_blank">Netstat</a>, like <tt>ps</tt>, is a Linux tool that administrators use every day. It displays a lot of network related information, such as socket usage, routing, interface, protocol, network statistics, and more. Some of the most commonly used options are:
<blockquote><tt>-a</tt> Show all socket information

<tt>-r</tt> Show routing information

<tt>-i</tt> Show network interface statistics

<tt>-s</tt> Show network protocol statistics</blockquote>
<h3>nmon</h3>
<a href="http://nmon.sourceforge.net/pmwiki.php" rel="nofollow" target="_blank">Nmon</a>, short for Nigel's Monitor, is a popular <a href="http://h30565.www3.hp.com/t5/Feature-Articles/Crafting-Small-Business-Open-Source-Policies/ba-p/1368" target="_blank">open-source</a> tool to monitor Linux systems performance. Nmon watches the performance information for several subsystems, such as processor utilization, memory utilization, run queue information, disk I/O statistics, network I/O statistics, paging activity, and process metrics. You can then view nmon's real-time system measurements via its <tt>curses</tt> “graphical” interface.

To run <tt>nmon</tt>, you start the tool from the shell. Once up, you select the subsystems to monitor by typing in its one-key commands. For example, to get CPU, memory, and disk statistics, you type <tt>c</tt>, <tt>m</tt>, and <tt>d</tt>. You can also use <tt>nmon</tt> with the <tt>-f</tt> flag to save performance statistics to a CSV file for later analysis.

For day to day server monitoring I find <tt>nmon</tt> to be the single most useful program in my Linux system management tool-kit.
<h3>pmap</h3>
The <a href="http://linuxcommand.org/man_pages/mpstat1.html" rel="nofollow" target="_blank">pmap</a> command reports the amount of memory that your server's processes are using. You can use this tool to determine which processes on the server are being allocated memory and whether any of these processes are being piggy with RAM.
<h3>ps and pstree</h3>
The <a href="http://www.linux.ie/newusers/beginners-linux-guide/ps.php" rel="nofollow" target="_blank">ps</a> and <a href="http://www.linfo.org/pstree.html" rel="nofollow" target="_blank">pstree</a> commands are two of the Linux administrator’s best friends. They both provide a list of all currently running processes. <tt>Ps</tt> tells you how much memory and processor time the server’s programs are using. <tt>Pstree</tt> shows less information, but highlights which processes are the children of other processes. Armed with this information, you can spot out–of-control processes and kill them off with Linux's “take no prisoners” <a href="http://linux.about.com/library/cmd/blcmdl_kill.htm" rel="nofollow" target="_blank">kill</a> command.
<h3>sar</h3>
The <a href="http://www.thegeekstuff.com/2011/03/sar-exampl" rel="nofollow" target="_blank">sar</a> program is a Swiss-army knife of a system monitoring tool. The <tt>sar</tt> command is actually made up of three programs: <tt>sar</tt>, which displays the data, and <tt>sa1</tt> and <tt>sa2</tt>, which collect and store it. Once installed, <tt>sar</tt> creates a detailed overview of CPU utilization, memory paging, network I/O and transfer statistics, process creation activity, and <a href="http://h30565.www3.hp.com/t5/Feature-Articles/Securing-Data-at-Rest-with-Encrypted-Portable-Drives/ba-p/243" target="_blank">storage device</a> activity. The big difference between <tt>sar</tt> and <tt>nmon</tt> is that the former is better at long-term system monitoring, while I find <tt>nmon</tt> to be better at giving me a quick read on my server's status.
<h3>strace</h3>
<a href="http://www.hokstad.com/5-simple-ways-to-troubleshoot-using-strace.html" rel="nofollow" target="_blank">strace</a> is often thought of a programmer's debugging tool, but it's more than that. It intercepts and records the system calls that are called by a process. This makes it a useful diagnostic, instructional, and debugging tool. For example, you can use <tt>strace</tt> to find out which configuration file a program is actually using when it starts up.

<tt>Strace</tt> does have one flaw though. When it's checking out a specific process, that process' performance will fall through the floor. Thus, I only use <tt>strace</tt> when I already have a darned good reason to think that <em>that</em> program is causing trouble.
<h3>tcpdump</h3>
<a href="http://danielmiessler.com/study/tcpdump/" rel="nofollow" target="_blank">Tcpdump</a> is a simple, robust network monitoring utility. Its basic protocol analyzing capability enables you to get a rough view of <a href="http://h30565.www3.hp.com/t5/Feature-Articles/Understanding-Syslog-Managers-and-How-to-Use-Them/ba-p/1488" target="_blank">what is happening on your network</a>. To really dig into what's going on with your network however, you'll want to use <a href="http://ww/" rel="nofollow" target="_blank">Wireshark</a> (see below).
<h3>top</h3>
The <a href="http://adminlinux.blogspot.com/2009/06/how-do-i-use-linux-top-command.html" rel="nofollow" target="_blank">top</a> command shows what's going on with your active processes. By default, it displays the most CPU-intensive tasks running on the server and updates the list every five seconds. You can sort the processes by PID (Process ID); age, newest first; time, by cumulative time; and resident memory usage and total time it's been using the CPU since startup. I find this a fast and easy way to see if any process is starting to go out of control and about to get into trouble.
<h3>uptime</h3>
Use <a href="http://www.computerhope.com/unix/uptime.htm" rel="nofollow" target="_blank">uptime</a> to see how long the server has been running and how many users are logged on. It also gives you an overview of the average server load. The optimal value of the load is 1 or less, which means that each process has immediate access to the CPU and there are no CPU cycles lost.
<h3>vmstat</h3>
For the most part, you use <a href="http://www.linuxjournal.com/article/8178" rel="nofollow" target="_blank">vmstat</a> to monitor what's going on with virtual memory. Linux constantly uses virtual memory to get the best possible storage performance.

If your applications are taking up too much memory you get excessive page-outs — programs moving from RAM to your system's swap space, which is on the hard drive. Your server can reach a point where it's spending more time managing memory paging than running your applications, a condition called thrashing. When your computer is thrashing, its performance falls through the floor. <tt>Vmstat</tt>, which can display either average data or actual samples, can help you spot memory pig programs and processes before they bring your server to a crawl.
<h3>Wireshark</h3>
<a href="http://www.wireshark.org/" rel="nofollow" target="_blank">Wireshark</a>, formerly known as Ethereal (and still often referred to that way), is <tt>tcpdump</tt>'s big brother, though it is more sophisticated and with far more advanced protocol analyzing and reporting. Wireshark has both a GUI interface and a shell interface. If you do any serious network administration, you <em>must</em> use ethereal. And, if you're using Wireshark/ethereal, I highly recommend Chris Sander's <a href="http://www.amazon.com/gp/product/B002N3M6RC/ref=as_li_ss_tl?ie=UTF8&amp;tag=thegroovycorpora&amp;linkCode=as2&amp;camp=1789&amp;creative" rel="nofollow" target="_blank">Practical Packet Analysis</a>, a great book on how to get the most out of this useful program.

This has only been a 10,000 foot overview of some of Linux's most valuable system monitoring programs. Still, if you can master these programs you'll be well on your way to being a top Linux system administrator.