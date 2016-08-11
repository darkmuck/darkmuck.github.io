---
ID: 1978
post_title: >
  Organizing JavaScript, HTML, and CSS
  Code
author: Shwuzzle
post_date: 2013-08-19 10:14:53
post_excerpt: ""
layout: post
published: true
---
Many web applications these days contain a ton of HTML, CSS, and JavaScript code. If you don't have a good plan before starting to code it can get really messy really fast. It's important to plan and organize your code well. Although we want to separate and organize our code as best as possible, the different types and pieces of code will inevitably need to be linked together in many ways.

<strong>Directories
</strong>The directory structure in which your code files are organized in is something you can easily set up in the beginning of a project. A good structure will help you to separate different types of files from one another, thereby making it easier to find things when you need them. An example of a fairly good structure may be something like:
<pre style="padding-left: 60px;">app-root
    resources
        css
            images
            blue-theme
            blue-theme.css
        js
            main.js
        img
            company-logo.png
        data
            lots-of-data.xml
            more-data.csv
    vendor
        jquery
            jquery-min.js
    index.html
    about.html</pre>
<strong>JavaScript
</strong>There are a number of things you can do to keep your JavaScript code files organized. A few things that I usually do are:
<ul>
	<li>Keep as much JavaScript separate from the markup code as possible</li>
	<li>Put all dependencies at the top of each file<strong></strong></li>
	<li>Move large reusable sections of code to a separate file</li>
	<li>Group together similar types of functions (init functions, selectors, event bindings, etc.)</li>
	<li>Name functions and variables as descriptively as possible (within reason)</li>
	<li>Name the code files in a descriptive manor, but also concise</li>
	<li>Make use of namespaces when possible to keep related bits of code grouped together</li>
</ul>
<strong>CSS</strong>
With CSS there are also a number of things you can do to keep the code organized. When coding my stylesheets I usually try to adhere by a few things, such as:
<ul>
	<li>Group together and label (with comments) related items</li>
	<li>Write each property on a separate line</li>
	<li>Combine multiple selectors that share the same properties
e.g.: h1, h2, h3, h4 { color: #666; 0 0 .5em; }</li>
	<li>Avoid using universal selectors to improve performance</li>
	<li>Try to use classes as much as possible and avoid using IDs</li>
	<li>Make liberal use of white space so it is easier to read and skim</li>
	<li>Avoid inline styles on your markup pages when possible</li>
	<li>Avoid header styles on your markup pages</li>
	<li>Reduce complexity by separating code in separate files (within reason), and you can use tools to 'compile' them together before deployment if you so desire</li>
	<li>Use a CSS minifier to 'compile' your code into a smaller file for deployment to improve performance</li>
	<li>Layout the stylesheet such that it somewhat mirrors the page(s)/template(s). For example:</li>
</ul>
<pre style="padding-left: 60px;">base-style.css
    general styles
    header
    navigation
    content
    footer
[page_name]-style.css</pre>
<strong>External Resources:</strong>
<ul>
	<li><a href="http://philipwalton.com/articles/decoupling-html-css-and-javascript/">Decoupling Your HTML, CSS, and JavaScript</a></li>
	<li><a href="http://appcropolis.com/blog/web-technology/organize-html-css-javascript-files/">How to Organize Your HTML, CSS, and JavaScript Files</a></li>
	<li><a href="http://www.slideshare.net/lachlanhardy/beautiful-maintainable-css">Beautiful Maintainable CSS</a></li>
	<li><a href="http://www.slideshare.net/maxdesign/efficient-maintainable-css-presentation">Efficient Maintainable CSS</a></li>
</ul>
