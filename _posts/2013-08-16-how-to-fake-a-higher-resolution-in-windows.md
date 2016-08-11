---
ID: 1964
post_title: 'How to &#8216;Fake&#8217; a Higher Resolution in Windows'
author: Shwuzzle
post_date: 2013-08-16 15:34:34
post_excerpt: ""
layout: post
published: true
---
If your windows machine is stuck with a low resolution and you wish you had a higher resolution screen you might want to try out this registry hack. This is a way to "fake" a higher resolution in Windows by lowering the DPI. This method is done by modifying values in the registry because by default Windows won't let you set it this low.
<ol>
	<li>Open the Start Menu and click Run</li>
	<li>Type in regedit and press enter</li>
	<li>Navigate to: HKEY_CURRENT_CONFIG --&gt; Software --&gt; Fonts</li>
	<li>On the right-side from the tree, choose LogPixels and then in the main screen modify it's decimal value to whatever DPI value you'd like, however don't go lower than 85 in most cases (In the Windows Custom DPI settings screen, the default lowest is 96)</li>
	<li>Log off and log back on or just restart your machine</li>
</ol>
