---
ID: 2005
post_title: Optimizing Web Assets for Performance
author: Shwuzzle
post_date: 2013-08-23 15:54:04
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2013/08/23/optimizing-web-assets-for-performance/
published: true
---
Although most internet users nowadays have very fast connections it is still important to optimize your web application's assets to ensure optimal performance. This is especially the case for mobile users, which have more constrained resources (data connections and hardware resources). There are a number of things you can do but I'lll highlight just a few that I believe are important to think about.

<strong>Images</strong>
<p style="padding-left: 30px;">Serve Multiple Sizes - Instead of serving the same image used in multiple locations at different sizes on your website, you should try to make use of CSS media queries to define separate images for certain circumstances. Check out <a href="http://css-tricks.com/snippets/css/media-queries-for-standard-devices/">css-tricks's page on media queries</a> for more info.</p>
<p style="padding-left: 30px;">Compression - You should compress your images as well as possible in a photo editor before using them on the web. However, you can also use code to compress them on the fly. For example, this is possible using the various <a href="http://us3.php.net/manual/en/refs.utilspec.image.php">image processing utility functions in PHP</a>.</p>
<p style="padding-left: 30px;">Prefetching - With the new HTML5 specification you can prefetch content before its actually needed. This means that when it is needed, the content will already be available. Check out the <a href="http://www.whatwg.org/specs/web-apps/current-work/#link-type-prefetch">WhatWG page on the prefetch specification</a> for more info.</p>
<p style="padding-left: 30px;">Caching - It's a good idea to try to take advantage of caching in your browser if possible. This way you can reduce the amount of content that needs to be retrieved multiple times. To learn more about controlling your browser's caching in the <a href="http://betterexplained.com/articles/how-to-optimize-your-site-with-http-caching/">HTTP headers check out this page via betterexplained.com</a>.</p>
<strong>Stylesheets (CSS)</strong>
<p style="padding-left: 30px;">Preprocessing - CSS preprocessors help to automatically organize and optimize your stylesheets. Check out <a href="http://lesscss.org/">LESS</a>, <a href="http://sass-lang.com/">SASS</a>, or <a href="http://learnboost.github.com/stylus/">Stylus</a>.</p>
<p style="padding-left: 30px;">Syntax Improvements - By carefully crafting your stylesheets you can reduce the size and increase the performance of rendering them. For some tips on good practices check out <a href="https://developers.google.com/speed/docs/best-practices/rendering">this developers.google.com site</a> and <a href="http://css-tricks.com/efficiently-rendering-css/">this css-tricks.com page</a>. You can also minimize the size of your CSS files automatically with tools such as <a href="http://www.cssoptimiser.com/">CSSOptimizer</a> and <a href="http://www.minifycss.com/css-compressor/">Minifycss</a>.</p>
<strong>Client-Side Code (JavaScript)</strong>
<p style="padding-left: 30px;">Size - You can also minimize the size of your JavaScript code. This reduced file size will allow for it to load quicker. There are quite a few tools out there to help you automatically minimize your JavaScript code.</p>
<p style="padding-left: 30px;">Code Organization - You should try to only load code as its needed in your application. Minimizing HTTP requests will help to increase performance. You can make use of tools such as <a href="http://requirejs.org/">RequireJS</a> to load different modules as needed. There are also ways to <a href="http://elegantcode.com/2011/01/26/basic-javascript-part-8-namespaces/">'simulate' namespaces in JavaScript</a> to help reduce the number of objects and to better organize the code.</p>
<p style="padding-left: 30px;">Design Patterns - You wouldn't want to create everything you want to do from scratch. For many things you want to do there are most likely established efficient methods out there. Some design patterns to look at may be: Constructor Pattern, Module Pattern, MVC Pattern, Observer Pattern, Function Chaining Pattern, etc.</p>