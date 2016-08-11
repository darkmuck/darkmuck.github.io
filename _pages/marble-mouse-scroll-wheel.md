---
ID: 1350
post_title: Marble Mouse Scroll Wheel
author: Shwuzzle
post_date: 2010-09-19 14:49:38
post_excerpt: ""
layout: page
permalink: >
  http://localhost:8080/projects/linux-shell-scripts/marble-mouse-scroll-wheel/
published: true
aktt_notify_twitter:
  - 'no'
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
---
The  Logitech Marble Mouse doesn't come with a physical scroll wheel. For  Microsoft Windows there is a peice of software called: "Marble Mouse  Scroll Wheel" which emulates a scroll wheel by holding down the  left-middle button and using the ball. However no such application  exists for Linux. I did some research and discovered a number of methods  for enabling the scroll wheel. The method I decided upon involves  executing a shell script. This method is sort of clumsy, but you can at  least partially automate it if you want by having the script execute  upon user login. The best method would involving something like  modifying xorg.conf, which I was too impatient to attempt! Follow these  instructions for the shell script method.
<ol>
	<li>Copy and paste the following code into a new file "marbleScroll.sh"</li>
<code> xinput set-button-map "Logitech USB Trackball" 1 2 3 4 5 6 7 8 9
xinput set-int-prop "Logitech USB Trackball" "Evdev Wheel Emulation Button" 8 8
xinput set-int-prop "Logitech USB Trackball" "Evdev Wheel Emulation" 8 1
xinput set-int-prop "Logitech USB Trackball" "Evdev Wheel Emulation Axes" 8 6 7 4 5
xinput set-int-prop "Logitech USB Trackball" "Evdev Wheel Emulation X Axis" 8 6
xinput set-int-prop "Logitech USB Trackball" "Evdev Drag Lock Buttons" 8 9</code>
	<li>Make the file executable with: chmod 755 marbleScroll.sh</li>
	<li>Execute the file with: ./marbleScroll.sh</li>
	<li>You should now be able to scroll vertically by holding down the left-middle mouse button and moving the ball!</li>
</ol>
For more information visit: <a href="https://help.ubuntu.com/community/Logitech_Marblemouse_USB">Logitech Marble Mouse USB (Community Ubuntu Documentation)</a>