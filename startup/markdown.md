---
layout: default
title: Markdown
---
Markdown is a simple markup language that makes developing the site much
easier. Jekyll automatically converts files with a .md extension to HTML when it
processes them. All of the markdown syntax in the file is converted to its
equivalent in HTML.

## Links

To create a hyperlink, the "`[]()`" syntax is used. The square brackets contain
the text you want to convert into a URL, and the brackets contain the URL
itself.

### External Links
To link to an external URL, you just use the address of the page you want to
link to.

`This is a [link](www.ros.org) to the ROS homepage.`

When processed into HTML looks like:

`This is a <a href='www.ros.org'>link</a> to the ROS homepage.`

### Internal Links
For internal URLS, like the Robots or Members pages, the syntax is exactly the
same, but you instead provide a path to the page you want to link to based on
the directory structure of the website. If we wanted to create a link to this
page, then we would do something like the following.

`This is a [link](/startup/jekyll.html) to the Jekyll tutorial.`

This gives us 

`This is a <a href='/startup/jekyll.html'>link</a> to the Jekyll tutorial.`

in HTML.

To refer to the homepage, use `[Home](/)`.

## Headers

Markdown has various ways of defining headers like the one above. The largest
and second larges headers (HTML `h1` and `h2`) can be defined in two ways.


	This is a h1
	============

	# This is also a h1

	This is a h2
	-----------

	## And so is this

Which looks like

	<h1 id='this_is_a_h1'>This is a h1</h1>

	<h1 id='this_is_also_a_h1'>This is also a h1</h1>

	<h2 id='this_is_a_h2'>This is a h2</h2>

	<h2 id='and_so_is_this'>And so is this</h2>

when converted to HTML.

Each additional `#` you add gives a lower level header, up to a maximum of 6
levels. 

## Lists

Markdown has syntax for both ordered and unordered lists.

### Unordered Lists

Unordered lists are specified by the use of the \*, \- or \+ symbols before a line of
text, and all produce the same output. You should have a newline before and
after the list.

	- This
	- is an
	- unordered list

In HTML, this looks like

	<ul>
	<li>This</li>

	<li>is an</li>

	<li>unordered list</li>
	</ul>

### Ordered Lists

Ordered lists are specified by the use of numbers and periods before each line.

	1. This
	2. is an
	3. ordered list

In HTML, this looks like

	<ol>
	<li>This</li>

	<li>is an</li>

	<li>ordered list</li>
	</ol>

## Code

There are two ways in which you can define a code block. For inline code like
`x = y`, you wrap text in backtick quotes or grave accents (\`), for which the equivalent HTML is `<code>x = y</code>`.

You can specify code blocks by indenting each line by 4 spaces or a single tab. Code blocks look like

	<pre><code> Preformatted code
		goes in
		here
	</pre></code>

## More

More detailed documentation can be found at the
[project website](http://daringfireball.net/projects/markdown/).
