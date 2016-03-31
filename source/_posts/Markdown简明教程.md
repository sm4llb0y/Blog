title: Markdown简明教程
date: 2013-09-19 22:18:40
tags: Markdown, cheatsheet, 教程
categories: 编程
---

**强调：**  

    *italic*   **bold**
    _italic_   __bold__

<!--more-->

**Links**

_Inline样式:_

	An [example](http://url.com/ "Title")

_Reference样式 (titles是可选的):_

	An [example][id]. Then, anywhere
	else in the doc, define the link:
	
	[id]: http://example.com/  "Title"

**图片**

_Inline样式 (titles可选的):_

	![alt text](/path/img.jpg "Title")

_Reference样式:_

	![alt text][id]
	
	[id]: /url/to/img.jpg "Title"

**标题**

_Setext-样式:_

	Header 1
	========
	
	Header 2
	--------

_atx样式 (闭合#是可选的):_

	# Header 1 #
	
	## Header 2 ##
	
	###### Header 6

**列表**

_有序, 无中间段落:_

	1.  Foo
	2.  Bar

_无序, 有中间段落:_

	*   A list item.
	
	    With multiple paragraphs.
	
	*   Bar

_可以进行嵌套:_

	*   Abacus
    	* answer
	*   Bubbles
	    1.  bunk
	    2.  bupkis
    	    * BELITTLER
    	3. burper
	*   Cunning

**块引用**

	> Email-style angle brackets
	> are used for blockquotes.
	
	> > And, they can be nested.
	
	> #### Headers in blockquotes
	> 
	> * You can quote a list.
	> * Etc.

**代码span**

	`<code>` spans are delimited
	by backticks.

	You can include literal backticks
	like `` `this` ``.

**预先格式化好的代码块**

_每行至少 4 个空格或者 1 个 tab._

	This is a normal paragraph.

	    This is a preformatted
	    code block.

**水平线**

_3个或者多个-，_或者*:_

	---

	* * *
	
	- - - - 

**强制换行**

_行末3个或者多个空格:_

	Roses are red,   
	Violets are blue.

**[注]: 翻译自[Daring Fireball](http://daringfireball.net/projects/markdown/dingus)**