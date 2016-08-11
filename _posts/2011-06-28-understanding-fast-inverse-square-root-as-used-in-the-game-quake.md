---
ID: 1687
post_title: >
  Understanding Fast Inverse Square Root
  (as used in the game Quake)
author: Shwuzzle
post_date: 2011-06-28 08:08:10
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2011/06/28/understanding-fast-inverse-square-root-as-used-in-the-game-quake/
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
"<em>An <a href="http://www.beyond3d.com/articles/fastinvsqrt/">article</a> and <a href="http://www.lomont.org/Math/Papers/2003/InvSqrt.pdf">research paper</a> describe a fast, seemingly magical way to compute the inverse square root (1/sqrt(x)), used in the game Quake.</em>

<em>I’m no graphics expert, but appreciate why square roots are useful. The <a href="http://betterexplained.com/articles/measure-any-distance-with-the-pythagorean-theorem/">Pythagorean theorem</a> computes distance between points, and dividing by distance helps  normalize vectors. (Normalizing is often just a fancy term for  division).</em>

<em>3D games like Quake divide by distance zillions (yes zillions) of  times each second, so “minor” performance improvements help immensely.  We don’t want to take the square root and divide the regular way:  exponentiation and division are really, really expensive for the CPU.</em>

<em> Given these conditions, there is a magic formula to get 1/sqrt(x) found in the game Quake.</em>"
<table border="0">
<tbody>
<tr>
<td><code>float InvSqrt(float x){
float xhalf = 0.5f * x;
int i = *(int*)&amp;x; // store floating-point bits in integer
i = 0x5f3759d5 - (i &gt;&gt; 1); // initial guess for Newton's method
x = *(float*)&amp;i; // convert new bits into float
x = x*(1.5f - xhalf*x*x); // One round of Newton's method
return x;
}
</code></td>
</tr>
</tbody>
</table>
<a href="http://betterexplained.com/articles/understanding-quakes-fast-inverse-square-root/">Understanding Quake's Fast Inverse Square Root (betterexplained.com)</a>

<strong>Additional Resources:
</strong>
<ul>
	<li><a href="http://games.slashdot.org/story/06/12/01/184205/Origin-of-Quake3s-Fast-InvSqrt">Origin of Quake's Fast InvSqrt() (slashdot.org)</a></li>
<a href="http://games.slashdot.org/story/06/12/01/184205/Origin-of-Quake3s-Fast-InvSqrt"> </a>
	<li><a href="http://games.slashdot.org/story/06/12/01/184205/Origin-of-Quake3s-Fast-InvSqrt"></a><a href="http://www.beyond3d.com/content/articles/8/">Origin of Quake's Fast InvSqrt() (beyond3d.com)</a></li>
</ul>