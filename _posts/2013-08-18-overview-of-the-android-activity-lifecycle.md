---
ID: 1971
post_title: >
  Overview of the Android Activity
  Lifecycle
author: Shwuzzle
post_date: 2013-08-18 13:33:39
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2013/08/18/overview-of-the-android-activity-lifecycle/
published: true
---
In developing for the Android platform, one of the most important concepts to understand is the Activity Lifecycle. This is important because applications behave much differently on Android when compared to traditional platforms, such as Windows, OS X, or Linux. With Android you have less control over the lifetime of an application.

An activity is a single user interface screen that contains one or many views (visual elements). The views (controls/widgets) on the activity allow a user to interact with it. An application can have one or many activities that can be linked together as defined in the manifest file.

There are four states in which an activity can exist:
<ol>
	<li>Active/Running - activity has focus and is visible</li>
	<li>Paused - activity is partially visible but not active and does not have focus (occurs when an activity is on top of it, but does not cover the whole screen or uses some form of transparency)</li>
	<li>Stopped - activity is not visible any longer, but the state is preserved but is likely to be killed if resources are needed</li>
	<li>Destroyed/Dead - activity no longer exists in memory</li>
</ol>
The flow of the lifecycle can briefly explained as:
<ol>
	<li>An activity is launched and the onCreate() method is executed. Here the interface is created and the data elements are initialized.</li>
	<li>Before the activity becomes visible to the user the onStart() method is executed.</li>
	<li>For the activity to become visible the onResume() method is executed and it is now able to be interacted with.</li>
	<li>If another activity is launched then the onPause() method is executed to save the state of the previous activity. There is now the possibility that the activity may be killed to free up resources if needed.</li>
	<li>The activity will stay in the paused state if: the user presses the home button, another activity is launched but does not completely cover the screen, or if the device goes to sleep.</li>
	<li>A few things can happen to the activity in the paused state, they are: it can be resumed (the onResume() method is then executed) or it can be killed by the system if resources are needed. If the activity is killed then the onCreate() method would need to be executed if the activity is launched again. If these things don't happen then the onStop() method is executed, which is also what happens if the user hits the back button on the activity.</li>
	<li>When the activity is in the stopped state a few things can happen here as well: it can be killed to free up resources, it can be restored (either onRestart(), onStart(), or onResume() are executed), or it can be destroyed (onDestroy() is executed).</li>
</ol>
External Resources:
<ul>
	<li><a href="http://developer.android.com/training/basics/activity-lifecycle/index.html">Managing the Activity Lifecycle (developer.android.com)</a></li>
	<li><a href="http://www.android-app-market.com/android-activity-lifecycle.html">Android Activity Lifecycle (android-app-market.com)</a></li>
</ul>