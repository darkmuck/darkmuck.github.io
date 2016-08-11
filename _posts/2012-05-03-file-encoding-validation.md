---
ID: 1852
post_title: File Encoding Validation
author: Shwuzzle
post_date: 2012-05-03 08:19:57
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2012/05/03/file-encoding-validation/
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
If you're using a Unix or Unix-like operating system you can leverage the GNU iconv library to validate the encoding of a file or files. Although, the GNU iconv library is actually meant to do file conversions, it can still be used in a way that will give you some understanding if the file(s) contain invalid byte sequences.

$ iconv -f UTF-8 the_file -o /dev/null

In the above example you actually don't need to necessarily specify the UTF-8 as this is the assumed default encoding for iconv. This example will output a 0 if the file is able to be converted (no encoding errors) or a 1 if it cannot (encoding errors). It will also display the byte offset where the invalid byte sequence occurs. Also, an alternative syntax for this command might be something like:

$ iconv -f UTF-8 &lt; the_file &gt; /dev/null

For more information refer to:
<ul>
	<li><a href="http://www.gnu.org/savannah-checkouts/gnu/libiconv/documentation/libiconv-1.13/iconv.1.html">ICONV man page</a></li>
	<li><a href="http://www.gnu.org/software/libiconv/">GNU libiconv</a></li>
</ul>