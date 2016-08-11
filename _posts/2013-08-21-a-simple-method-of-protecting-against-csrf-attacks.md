---
ID: 1992
post_title: >
  A Simple Method of Protecting Against
  CSRF Attacks
author: Shwuzzle
post_date: 2013-08-21 10:13:31
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2013/08/21/a-simple-method-of-protecting-against-csrf-attacks/
published: true
---
A simple method to protect your web application against CSRF (cross-site request forgery) attacks is to generate and validate a unique token of some sort. This can help to prevent automated CSRF attacks. Basically, you will generate a unique token for the user, place it on the page, and then check the token to verify that its valid. You could implement this in just about any server side language, but here is a PHP example.

<strong>1. Generate Token and Place it Hidden on Page
</strong><tt>function getToken() {
return hash("sha256", "your-random-salt" . userSesssionId());
}
echo "&lt;input type='hidden' name='token' value='" . getToken() . "' /&gt;";</tt><strong> </strong>

<strong>2. Check the Token to Validate Its Authenticity</strong><tt>
function validateToken() {
// If we generate the token again, does it still match?
return $_POST["token"] == getToken();
}
if (!validateToken())
trigger_error("Invalid session token.");</tt>

source: <a href="http://lucb1e.com/?p=post&amp;id=89">CSRF: It's not trivial (lucb1e.com)</a>