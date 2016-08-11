---
ID: 1815
post_title: 'Tip: How to connect to a database with different credentials in SQL Server Management Studio'
author: Shwuzzle
post_date: 2012-01-06 10:42:59
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2012/01/06/tip-how-to-connect-to-a-database-with-different-credentials-in-sql-server-management-studio/
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
If you are logged into your machine with a username that doesn't have access to a certain SQL Server database you can launch SQL Server Management Studio with different credentials. This allows you to use Windows Authentication with a different username when connecting to the database server.
<table style="width: 475px; background-color: #ddd9db;" border="0">
<tbody>
<tr>
<td><span style="font-size: x-small; margin-left: 8px;">runas /user:DOMAIN\USERNAME "C:\Program Files (x86)\Microsoft SQL Server\100\Tools\Binn\VSShell\Common7\IDE\Ssms.exe"</span></td>
</tr>
</tbody>
</table>
&nbsp;