---
ID: 1995
post_title: >
  What Is Cross-Site Scripting (XSS) And
  How to Prevent It
author: Shwuzzle
post_date: 2013-08-22 11:54:30
post_excerpt: ""
layout: post
published: true
---
Cross-Site Scripting (XSS) isn't necessarily an actual "cross-site" attack, instead its essentially an insertion of client-side script code placed strategically such that users will execute them. This is possible when output from the website isn't properly escaped, thereby allowing extra code to be added.

Ideally, at the appropriate times, you will want to escape both input and output from places like your database, however with XSS we're primarily concerned with user input. One method of partially protecting against XSS (and also to prevent SQL injection) you can make use of magic quotes (at least in PHP), which will basically break (causing syntax error) any JavaScript code that may have been added.

There are also other ways to protect against XSS attacks. With PHP, when inserting HTML you can make use of the htmlspecialchars() function, which will convert special characters to HTML. This means that you won't be able to insert additional JavaScript code because it would be encoded. For example, &lt;script&gt; would be encoded to &amp;lt;script&amp;gt;. There are still ways to get around this protection but it's may be helpful to prevent some attacks. Another thing you can do would be to combine your input escaping with output escaping when storing and retrieving data from the database. With this you would escape characters going into the database and then both escape and encode (htmlspecialchars) on the retrieval. For example you would do something like this:
<p style="padding-left: 30px;">Input to Database
query_db(INSERT INTO the_table (column_name) VALUES ('" . escape($_GET["column_name"]) . "'));</p>
<p style="padding-left: 30px;">Output From Database
echo HTMLSPECIALCHARS(query_db("SELECT column_name FROM table_name WHERE id = value"));</p>
<p style="padding-left: 30px;">Combine Input &amp; Output Escaping
$item = HTMLSPECIALCHARS(ESCAPE($_GET["column_name"]));
query_db("INSERT INTO table_name (column_name) VALUES('$item')");
echo query_db("SELECT column_name FROM table_name WHERE id = " . just_inserted_id());</p>
