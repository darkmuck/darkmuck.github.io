---
ID: 1961
post_title: >
  Explanation of the .NET Application,
  Session, and View States
author: Shwuzzle
post_date: 2013-08-16 08:00:47
post_excerpt: ""
layout: post
published: true
---
Application State
The application state's purpose is primarily to store data for all variables in an ASP.NET application.The class used to store this data is the HttpApplication class, which can be accessed via the 'Code Behind' file. The data held within this class is available to all pages in the app and for all entities accessing the app. However, there is a method to lock certain peices of data to only allow certain users access to it.

Session State
The session state stories specific information about each distinct session. The session state can be configured in the &lt;sessionState&gt; section of the application's web.config file. The session state also stored information pertaining to users in individual session variables. Each user access their session data using a session ID, which retrieves cookies via HTTP/HTTPS from the web server. The session state can be accessed via the Session object in the 'Code Behind' file.

View State
The view state stores information about a specific page, which is hashed and stored as a hidden field on each page. The view state can be accessed via the ViewState object in the 'Code Behind' file.
