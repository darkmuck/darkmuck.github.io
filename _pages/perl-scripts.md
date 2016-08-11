---
ID: 1465
post_title: Perl Scripts
author: Shwuzzle
post_date: 2010-12-31 13:05:52
post_excerpt: ""
layout: page
permalink: >
  http://localhost:8080/projects/perl/perl-scripts/
published: true
aktt_notify_twitter:
  - 'yes'
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
---
<strong>Read and Parse a Tab Delimited Text File</strong>

The following Perl script will read all text files in the current working directory and then print columns 1 and 2 in a separate output file named "result.out".
<table style="border: 0pt solid #80807f; background-color: #d6d6d6; width: 505px; height: 157px;" border="0" cellspacing="0" cellpadding="0">
<tbody>
<tr valign="top">
<td>
<pre>#!/usr/bin/perl -w

#William DiStefano
#Version: 1

use Cwd;
my(@handles);

print "Process starting...\n";

unlink "result.out"; #remove result file if it exists

for(&lt;./*.txt&gt;){
  open($handles[@handles], $_);
}

my$continue = 1;

while ($continue) {
  $continue = 0;
  for my$op(@handles) {
    my@col = split;
    print OUTFILE $col[0] . "\t" . $col[1];
    $continue = 1;
  }
  print OUTFILE "\n";
}

undef@handles; #close tab-delimited files
close(OUTFILE); #close result.out

print "Process Complete!";</pre>
</td>
</tr>
</tbody>
</table>
&nbsp;

<strong>A Very Simple Way to Parse XML Files</strong>
<table style="border-width: 0pt; border-style: solid; -moz-border-top-colors: none; -moz-border-right-colors: none; -moz-border-bottom-colors: none; -moz-border-left-colors: none; -moz-border-image: none; background-color: #d6d6d6; width: 505px; height: 157px;" border="0">
<tbody>
<tr>
<td>
<pre>#!/usr/bin/perl -w</pre>
<pre> use strict;</pre>
<pre> use XML::Simple;</pre>
<pre>use Data::Dumper;</pre>
<pre>my $smpl = XML::Simple-&gt;new();
 my $d = $smpl-&gt;XMLin('file.xml');</pre>
<pre>print Dumper($d) . "\n";</pre>
</td>
</tr>
</tbody>
</table>