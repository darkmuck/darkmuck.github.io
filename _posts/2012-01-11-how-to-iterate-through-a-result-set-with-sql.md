---
ID: 1828
post_title: >
  How to iterate through a result set with
  SQL
author: Shwuzzle
post_date: 2012-01-11 16:48:01
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
<strong>Method 1: Using a cursor</strong>
<pre style="padding-left: 30px;">declare cursor1 cursor local for select * from tablename
open cursor1
fetch next from cursor1 into #temptable
while @@fetch_status = 0
begin
if exists (select column from tablename where 
        id = (select id from #temptable))
    begin 
        /* do stuff here */ 
    end
else
    begin
        /* do other stuff here */
    end 
if object_id('tempdb..#temptable') is not null
        drop table #temptable
fetch next from cursor1 into #temptable
end
close cursor1
deallocate cursor1</pre>
<strong>Method 2: Using a temporary table with primary key
</strong>        (via: <a href="http://support.microsoft.com/kb/111401">http://support.microsoft.com/kb/111401</a>)
<pre style="padding-left: 30px;">declare @au_id char( 11 )
set rowcount 0
select * into #mytemp from authors
set rowcount 1
select @au_id = au_id from #mytemp
while @@rowcount &lt;&gt; 0
begin
    set rowcount 0
    select * from #mytemp where au_id = @au_id
    delete #mytemp where au_id = @au_id
    set rowcount 1
    select @au_id = au_id from #mytemp&lt;BR/&gt;
end
set rowcount 0</pre>
<strong>Method 3: Using a temporary table without primary key
</strong>        (via: <a href="http://support.microsoft.com/kb/111401">http://support.microsoft.com/kb/111401</a>)
<pre style="padding-left: 30px;">set rowcount 0
select NULL mykey, * into #mytemp from authors
set rowcount 1
update #mytemp set mykey = 1
while @@rowcount &gt; 0
begin
    set rowcount 0
    select * from #mytemp where mykey = 1
    delete #mytemp where mykey = 1
    set rowcount 1
    update #mytemp set mykey = 1
end
set rowcount 0</pre>
