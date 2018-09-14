---
layout: post
title:  "Hello jQuery"
date:   2017-10-26 21:45:01 -0700
categories: progress
---
# Thursday

## Oh...hello there...

Been working with jQuery this week...and I like it. It makes things much faster!

Apparently "you don't need jQuery" according to some people...and I will agree...in some situations you shouldn't use jQuery...I mean...you can accomplish anything you want with Vanilla JS..but I can also walk to work every day, yet I drive...because it makes me WAY faster. For example....

```
var buttons = document.querySelectorAll("button");

for (var i = 0; i < buttons.length; i++){
	buttons[i].addEventListener("click", function(){
		this.style.backgroundColor("purple")
	}
	)};
}

```

Can be written as...

```
$("button").on("click", function(){
	this.css("background","purple")
	})
```

So much easier right???!?!?

Anyway...tomorrow I start my first todo project...built with HTML, CSS, and JS/jQuery.

	
-Mat