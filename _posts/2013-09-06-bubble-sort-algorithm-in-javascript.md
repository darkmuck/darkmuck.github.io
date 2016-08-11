---
ID: 2042
post_title: Bubble Sort Algorithm in JavaScript
author: Shwuzzle
post_date: 2013-09-06 14:15:21
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2013/09/06/bubble-sort-algorithm-in-javascript/
published: true
snap_isAutoPosted:
  - "1"
snapEdIT:
  - "1"
snapFB:
  - 's:188:"a:1:{i:0;a:5:{s:4:"doFB";s:1:"1";s:8:"PostType";s:1:"A";s:10:"AttachPost";s:1:"1";s:10:"SNAPformat";s:51:"New post (%TITLE%) has been published on %SITENAME%";s:11:"isPrePosted";s:1:"1";}}";'
snapTW:
  - 's:126:"a:1:{i:0;a:4:{s:4:"doTW";s:1:"1";s:10:"SNAPformat";s:15:"%TITLE% - %URL%";s:8:"attchImg";s:1:"0";s:11:"isPrePosted";s:1:"1";}}";'
---
<a href="http://en.wikipedia.org/wiki/Bubble_sort">Bubble Sort</a> is a very simple sorting algorithm. It works by stepping through a list to be sorted repeatedly while comparing each pair of coinsiding items and switching them if they are ordered incorrectly. This is a useful algorithm for doing simple comparisons in lists, but there are much more efficient algorithms for larger lists.

Bubble Sort example in JavaScript:
<pre>    var numbers = [3,5,2,4,7,9,6,4,5];
    var tmp;
    for (var i = 0; i &lt; numbers.length; i += 1) {
        for (var j = i; j &gt; 0; j -= 1) {
            if (numbers[j] &lt; numbers[j - 1]) {
                tmp = numbers[j];
                numbers[j] = numbers[j - 1];
                numbers[j - 1] = tmp;
            }
        }
    }
    console.log(numbers);</pre>
For more information on the Bubble Sort check the Wikipedia page here: <a href="http://en.wikipedia.org/wiki/Bubble_sort">Bubble Sort - Wikipedia.org</a>.