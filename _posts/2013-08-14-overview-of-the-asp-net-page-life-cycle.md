---
ID: 1953
post_title: Overview of the ASP.NET Page Life Cycle
author: Shwuzzle
post_date: 2013-08-14 11:06:36
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2013/08/14/overview-of-the-asp-net-page-life-cycle/
published: true
---
When running an ASP.NET webpage the page goes through a series of steps as it is being processed. This page life cycle includes: instantiating controls, restoring and maintaining state, running event handler code, and rendering. Having a good understanding of the page life cycle is important so that you know when in the process you should populate properties, initialize controls, run control behavior code, etc.

The stages of the page life cycle are:
<ol>
	<li>Page Request</li>
	<li>Start</li>
	<li>Initialization</li>
	<li>Load</li>
	<li>Postback event handling</li>
	<li>Rendering</li>
	<li>Unload</li>
</ol>
Within each of these stages there are many events that are raised, which allow you to run your code. A few fairly frequently used events that you would probably use are:
<ul>
	<li>PreInit</li>
	<li>Init</li>
	<li>InitComplete</li>
	<li>PreLoad</li>
	<li>Load</li>
	<li>Control Events</li>
	<li>LoadComplete</li>
	<li>PreRender</li>
	<li>PreRenderComplete</li>
	<li>SaveStateComplete</li>
	<li>Render</li>
	<li>Unload</li>
</ul>
In addition, you should also think about the life cycle of individual server controls themselves. These life cycles are similar to the page life cycle but operate independently of it. This is important to think about in many scenarios, such as data-bound controls that require use of data binding events, or login control events, or etc.

For more in-depth information on the ASP.NET Page Life Cycle check some of the following external resources:
<ul>
	<li><a href="http://msdn.microsoft.com/en-us/library/ms178472.aspx">ASP.NET Page Life Cycle Overview (msdn.microsoft.com)</a></li>
	<li><a href="http://www.codeproject.com/Articles/73728/ASP-NET-Application-and-Page-Life-Cycle">ASP.NET Application and Page Life Cycle (codeproject.com)</a></li>
	<li><a href="http://wiki.asp.net/page.aspx/1512/aspnet-page-life-cycle-events/">ASP.NET Page Life Cycle Events (wiki.asp.net)</a></li>
</ul>