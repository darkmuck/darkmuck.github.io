---
ID: 1811
post_title: >
  What every programmer should know about
  memory
author: Shwuzzle
post_date: 2012-01-04 09:25:42
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
<em>"In the early days computers were much simpler. The various components of a system, such as the CPU, memory, mass storage, and network interfaces, were developed together and, as a result, were quite balanced in their performance. For example, the memory and network interfaces were not (much) faster than the CPU at providing data.</em>

<em>This situation changed once the basic structure of computers stabilized and hardware developers concentrated on optimizing individual subsystems. Suddenly the performance of some components of the computer fell significantly behind and bottlenecks developed. This was especially true for mass storage and memory subsystems which, for cost reasons, improved more slowly relative to other components.</em>

<em>The slowness of mass storage has mostly been dealt with using software techniques: operating systems keep most often used (and most likely to be used) data in main memory, which can be accessed at a rate orders of magnitude faster than the hard disk. Cache storage was added to the storage devices themselves, which requires no changes in the operating system to increase performance. {Changes are needed, however, to guarantee data integrity when using storage device caches.} For the purposes of this paper, we will not go into more details of software optimizations for the mass storage access.....</em>

<em>For the most part, this document will deal with CPU caches and some effects of memory controller design. In the process of exploring these topics, we will explore DMA and bring it into the larger picture. However, we will start with an overview of the design for today's commodity hardware. This is a prerequisite to understanding the problems and the limitations of efficiently using memory subsystems. We will also learn about, in some detail, the different types of RAM and illustrate why these differences still exist....."</em>

<a href="http://lwn.net/Articles/250967/">Part 1 (http://lwn.net/Articles/250967/)</a>
<a href="http://lwn.net/Articles/252125/">Part 2 (http://lwn.net/Articles/252125/)</a>
<a href="http://lwn.net/Articles/253361/">Part 3 (http://lwn.net/Articles/253361/)</a>
<a href="http://lwn.net/Articles/254445/">Part 4 (http://lwn.net/Articles/254445/)</a>
<a href="http://lwn.net/Articles/255364/">Part 5 (http://lwn.net/Articles/255364/)</a>
<a href="http://lwn.net/Articles/256433/">Part 6 (http://lwn.net/Articles/256433/)</a>
<a href="http://lwn.net/Articles/257209/">Part 7 (http://lwn.net/Articles/257209/)</a>
