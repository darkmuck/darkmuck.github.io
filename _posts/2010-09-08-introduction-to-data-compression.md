---
ID: 1310
post_title: Introduction to Data Compression
author: Shwuzzle
post_date: 2010-09-08 09:29:07
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
If you are interested in learning more about data compression check out this ebook, <a href="http://www.cs.cmu.edu/afs/cs/project/pscico-guyb/realworld/www/compression.pdf">[PDF] Introduction to Data Compression)</a>,<a href="http://www.cs.cmu.edu/afs/cs/project/pscico-guyb/realworld/www/compression.pdf"> </a>that I just came across. It provides a good introduction to information theory, probability coding, applications of probability coding, data compression algorithms, and more related information. I haven't had a chance to read over the entire ebook, but it seems to be a sufficient introduction to data compression topics. However, if you are still curious and want to learn more, check out some of these books:
<ul>
	<li><a href="http://www.amazon.com/Data-Compression-Reference-David-Salomon/dp/1846286026/">Data Compression: The Complete Reference (Amazon.com)</a></li>
	<li><a href="http://www.amazon.com/Managing-Gigabytes-Compressing-Multimedia-Information/dp/1558605703">Managing Gigabytes: Compressing and Indexing Documents and Images (Amazon.com)</a></li>
</ul>
So what is data compression? According to theoretical computer science and information theory, it is the process of encoding data by using less bits than the unencoded version would use via the use of certain encoding mechanisms. It is really useful because it helps to reduce the use of resources on a system, specifically network bandwidth and hard disk space. However, there is a down side to compression. The data must be compressed and decompressed, which requires additional processing. In some cases, this can take quite a bit of time and use a lot of system resources, negatively affecting other applications on the system.

There are many different algorithms used for compression. They fall into two main categories: <a href="http://en.wikipedia.org/wiki/Lossless_compression">Lossless </a>and <a href="http://en.wikipedia.org/wiki/Lossy_data_compression">Lossy</a>. <a href="http://en.wikipedia.org/wiki/Lossless_compression">Lossless </a>algorithms represent the original data more concisely without any errors using statistical redundancy (compression is done by removing commonly occurring sets of bits and then fully replacing them during decompression). <a href="http://en.wikipedia.org/wiki/Lossy_data_compression">Lossy </a>compression is a bit more extreme. It involves human perception of the data. With <a href="http://en.wikipedia.org/wiki/Lossy_data_compression">lossy</a> algorithms, all data is not replaced upon decompression, which results in a slightly altered outcome. Although some data is removed, <a href="http://en.wikipedia.org/wiki/Lossy_data_compression">lossy </a>compression provides a method of preserving greater amounts of system resources when compared to <a href="http://en.wikipedia.org/wiki/Lossless_compression">lossless </a>compression.

<strong>Additional Resources
</strong>
<ul>
	<li><a href="http://en.wikipedia.org/wiki/Information_theory">Information Theory (Wikipedia)</a></li>
	<li><a href="http://en.wikipedia.org/wiki/Data_compression">Data Compression (Wikipedia)</a></li>
	<li><a href="http://thepcreport.net/tutorials/guide-to-compression-formats/">Guide to Compression Formats (thepcreport.net)</a></li>
	<li><a href="http://www.maximumcompression.com/lossless_vs_lossy.php">Lossless and Lossy Data Compression (maximumcompression.com)</a></li>
</ul>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 16px; width: 1px; height: 1px; overflow: hidden;">
<h1 class="parseasinTitle"><span id="btAsinTitle">Managing Gigabytes: Compressing and Indexing Documents and Images</span></h1>
</div>
