---
ID: 2027
post_title: >
  JavaScript Functions as Object
  Constructors
author: Shwuzzle
post_date: 2013-08-27 18:36:10
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2013/08/27/javascript-functions-as-object-constructors/
published: true
---
JavaScript is a prototype-based language and doesn't exactly support actual constructors, but we can sort of simulate constructors with functions. One thing to be weary of in JavaScript is scope management. JavaScript doesn't support classes; it only has support for functions. So you would be using functions in place of classes as well. Also, scope can be an issue with the 'this' keyword because 'this' operates different than in object-oriented languages. In JavaScript, the 'this' keyword refers to the global scope (window object), whereas in most object-oriented languages 'this' refers to the parent object.

With those things in mind, we can craft a solution to the no-constructor and no-class situation. You can create instances of a function using the 'new' keyword, much like how you'd create instances of a class in object-oriented languages. We can actually use this method to fix the scope problem of the 'this keyword'. When we create a new instance the 'this' keyword is then assigned the scope of the new function instance and no longer the window object. For example:
<pre style="white-space: pre-wrap; font-size: 11px;">function theFunction() {
  this.doSomething = function() { //Here 'this' refers to window object
    return message;
  }
}
var myTheFunction = new theFunction(); //Here 'new' controls the scope
myTheFunction.doSomething();</pre>