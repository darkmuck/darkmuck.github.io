---
ID: 1273
post_title: Fast Sorting Algorithm Uses GPUs
author: Shwuzzle
post_date: 2010-08-30 07:28:55
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2010/08/30/fast-sorting-algorithm-uses-gpus/
published: true
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
---
A new, extremely fast sorting algorithm has been created for GPUs (CUDA-capable only) by researchers at the University of Virginia. This new algorithm is capable of sorting at a rate of one billion (integer) keys per second using a GPU. Normally CPUs aren't as efficient as CPUs for these types of algorithms (for sorting), but these researchers claim to have created one much faster than any other known CPU-based sorting method.

This algorithm is for sorting large sequences of fixed-length keys/values. The current implementation can sort any of the C/C++ built-in numeric types or any structured payload types. Head over to the project's website using the link below or <a href="http://code.google.com/p/back40computing/wiki/RadixSorting#Building_and_Adapting">download the code</a> directly and try it for yourself.

<a href="http://code.google.com/p/back40computing/wiki/RadixSorting">RadixSorting - back40computing (Google Code)</a>