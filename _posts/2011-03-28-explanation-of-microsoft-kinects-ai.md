---
ID: 1546
post_title: 'Explanation of Microsoft Kinect&#8217;s AI'
author: Shwuzzle
post_date: 2011-03-28 09:37:38
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2011/03/28/explanation-of-microsoft-kinects-ai/
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
Microsoft has published a scientific research paper (<a href="http://research.microsoft.com/pubs/145347/BodyPartRecognition.pdf">[PDF] Real-Time Human Pose Recognition in Parts from Single Depth Images (Microsoft Research)</a>) detailing how Microsoft Kinect's body tracking algorithm works. There is also a video (<a href="http://www.youtube.com/watch?v=HNkbG3KsY84">Kinect Research (youtube.com)</a>) to go along with it. Also, I came across a separate article (<a href="http://www.i-programmer.info/news/105-artificial-intelligence/2176-kinects-ai-breakthrough-explained.html">Kinect's AI breakthrough explained (I-Programmer.info)</a>) which summaries how the algorithm works. Here is a small quote from that article:

"<em>What the team did next was to train a type of classifier called a  decision forest, i.e. a collection of decision trees. Each tree was  trained on a set of features on depth images that were pre-labeled with  the target body parts. That is, the decision trees were modified until  they gave the correct classification for a particular body part across  the test set of images. Training just three trees using 1 million test  images took about a day using a 1000-core cluster.</em>"

More Information:
<ul>
	<li><a href="http://www.i-programmer.info/news/105-artificial-intelligence/2176-kinects-ai-breakthrough-explained.html">Kinect's AI breakthrough explained (I-Programmer.info)</a></li>
	<li><a href="http://research.microsoft.com/pubs/145347/BodyPartRecognition.pdf">[PDF] Real-Time Human Pose Recognition in Parts from Single Depth Images (Microsoft Research)</a></li>
	<li><a href="http://www.youtube.com/watch?v=HNkbG3KsY84">Kinect Research Video (youtube.com)</a></li>
</ul>