---
ID: 2048
post_title: Bucket Sort algorithm in JavaScript
author: Shwuzzle
post_date: 2013-09-10 12:08:34
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2013/09/10/bucket-sort-algorithm-in-javascript/
published: true
snapEdIT:
  - "1"
snapFB:
  - 's:188:"a:1:{i:0;a:5:{s:4:"doFB";s:1:"1";s:8:"PostType";s:1:"A";s:10:"AttachPost";s:1:"1";s:10:"SNAPformat";s:51:"New post (%TITLE%) has been published on %SITENAME%";s:11:"isPrePosted";s:1:"1";}}";'
snap_isAutoPosted:
  - "1"
snapTW:
  - 's:126:"a:1:{i:0;a:4:{s:4:"doTW";s:1:"1";s:10:"SNAPformat";s:15:"%TITLE% - %URL%";s:8:"attchImg";s:1:"0";s:11:"isPrePosted";s:1:"1";}}";'
---
<a href="http://en.wikipedia.org/wiki/Bucket_sort">Bucket (bin) sort</a> is a sorting algorithm that parts an array into buckets. Each of these are sorted recursively with the bucket sorting algorithm. The basic procedure of Bucket Sort is:
1. Create an empty array
2. Loop through the original array and put each object in a "bucket"
3. Sort each of the non-empty buckets
4. Check the buckets in order and then put all objects back into the original array
<pre>var array = [2, 4, 1, 5, 3];
bucketSort(array);

function bucketSort(a) {
  var r = [], b = [], v, c;
  for (v of a) (b[v] || (b[v] = [])).push(v);
  for (c of b) if (c != null) for each (v in c) r.push(v);
  return r;
}</pre>
For more information on the Bucket Sort check the Wikipedia page here: <a href="http://en.wikipedia.org/wiki/Bucket_sort">Bucket Sort - Wikipedia.org</a>.