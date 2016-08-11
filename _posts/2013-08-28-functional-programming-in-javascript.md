---
ID: 2034
post_title: Functional Programming in JavaScript
author: Shwuzzle
post_date: 2013-08-28 15:28:11
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2013/08/28/functional-programming-in-javascript/
published: true
---
Procedural programming is where you define a procedure to solve a problem. Functional (aka declarative) programming is distinct from this in that you describe the "what" of the problem. With functional programming the results depend upon only the inputs and not on the program state. JavaScript is actually a multi-paradigm language, because it supports object-oriented, imperative, and functional programming styles.

In JavaScript, functions are first-class and are objects themselves. This means that they can have properties and methods, which is similar to how classes have properties and methods in object-oriented programming. You can even nest functions within one another. This plus the prototypes offered by JavaScript allow for you to simulate class-based features of object-oriented languages.

In addition, there are a few features of JavaScript that help in programming in a functional style, a few of these are: anonymous functions, ability to use functions as values, and the ability for functions as parameters for other functions.

Example 1 - Procedural vs Functional
Procedural Version:
var paragraphs = mailArchive[mail].split("\n");
for (var i = 0; i &lt; paragraphs.length; i++)
handlePara(paragraphs[i]);

Functional Version:
forEach(mailArchive[mail].split("\n"), handlePara);

Example 2 - Self-Executing Anonymous Function
(function (name) {
console.log(name + " functions can be automatically executed on defining them")
})("Anonymous");
console.log("JavaScript provides functional scope in place of block scoping");
(function () {
if (true) {
var x = true;
console.log("Is 'x' available inside block? " + x);
}
console.log("Is 'x' available outside block? " + x);
})();

Example 3 - Using Functions as Parameters to Other Functions
function anim(property, duration, endCallback) {
if (typeof endCallback === 'function') {
endCallback.apply(null);
}
}
anim('background-color', 1000, function () {
console.log('finished');
});

Additional Resources:
• <a href="http://www.ibm.com/developerworks/library/wa-javascript/index.html">Use functional programming techniques to write elegant JavaScript (ibm.com)</a>
• <a href="http://eloquentjavascript.net/chapter6.html">Functional Programming -- Eloquent JavaScript</a>
• <a href="http://www.srirangan.net/2011-12-functional-programming-in-javascript">An Introduction to Functional Programming in JavaScript (srirangan.net)</a>
$bull; <a href="http://blog.mgechev.com/2013/01/21/functional-programming-with-javascript/">Functional Programming with JavaScript (blog.mgechev.com)</a>