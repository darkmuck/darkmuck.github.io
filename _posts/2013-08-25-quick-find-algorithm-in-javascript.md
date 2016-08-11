---
ID: 2018
post_title: Quick-Find Algorithm in JavaScript
author: Shwuzzle
post_date: 2013-08-25 13:21:32
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2013/08/25/quick-find-algorithm-in-javascript/
published: true
---
Here is my (quickly thrown together) simple implementation of the quick-find algorithm. For more information on the algorithm and the Disjoint-set data structure (quick-find performs some useful operations on this type of data structure) check out the Wikipedia page on <a href="http://en.wikipedia.org/wiki/Disjoint-set_data_structure">Disjoint-set data structure here</a>.
<pre style="padding-left: 30px;">var numArray;

function QuickFindUF(numToFind) {
    numArray = new Array(numToFind);
    
    for (var i = 0; i &lt; numToFind; i++) {
        numArray[i] = i;
        document.write(numArray[i] + "&lt;br/&gt;");
    }
}

function connected(p,q) {
    return numArray[p] == numArray[q];   
}

function union(p,q) {
    var pid = numArray[p];
    var qid = numArray[q];
    for (var i=0; i &lt; numArray.length();i++){
        if (numArray[i] == pid) numArray[i] = qid;
    }
}</pre>