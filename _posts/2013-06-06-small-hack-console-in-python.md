---
layout: post
title: "[small hack] console in python"
description: ""
category: code
tags: [python, hack, readline]
---
{% include JB/setup %}

1) Console in python?
----------------------

I do NOT mean python interactive shell. If you're not about to make gui-style or daemon-style program, you're probably about to create console in your program.

{% highlight python %}
cmd = raw_input(' > ')
while not (cmd == 'quit')
	# some commands
	cmd = raw_input(' > ')
{% endhighlight %}

As you can see, it should work like this:

{% highlight html %}
 > mycommand
 >
{% endhighlight %}

2) How to improve it?
---------------------

This short program is not really perfect -- it does not behave like python interactive shell, it does not allow to use history, etc. However, there is package 'readline' coming to the rescue! You just need to import readline and your console will work just as interactive console.

{% highlight python %}
try:
	import readline
except:
	# be careful! it's easy to build python without readline!
	pass
{% endhighlight %}

