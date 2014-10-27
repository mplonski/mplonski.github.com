---
layout: post
title: "What to do to create better code?"
description: ""
category: theory
tags: [code]
---
{% include JB/setup %}

6 steps of creating code, good code.

1) Plan it, stupid!
-------------------

Before starting writing your next application supposed to earn $1 000 000, simply plan it. Think about all modules, all functions, all data-structures, everything, every part of your new app. If you don't, you will have to change everything in some time just because you forgot to add one small functionality. It's better to use object-oriented languages, e.g. python/java/c++ -- it's much easier to change anything in one class then in every line of your code.

2) KISS
-------

Keep It Simple, Stupid!

There is no worst nightmare for a programmer than to try to understand and fix some quite big and complicated code, even if it's your code written the day before. It's really important not to make it too long, to make your code as simple as possible. Why should you use 10 lines of code if you can write the same code in 1 line? What if it's not Hello World, but application containing 20 files, each of them with 500 lines of code?

Example? Let's say that we have to write function getting an variable, which may contain "yes" or "no" and returning 1 in case of "yes" and 0 in case of "no". How is it going to be done by newbie in python?

{% highlight python %}
def yesorno(t):
	n = -1
	if (t == "yes"):
		n = 1
	if (t == "no"):
		n = 0
	return n
{% endhighlight %}

And what about old-python-man?

{% highlight python %}
def yesorno(t):
	return 1 if (t == "yes") else 0
{% endhighlight %}

Which one is better?

3) Read your code.
------------------

I don't know why, but some programmers don't read their code. How are you supposed to keep your code clear and professional if you're simply writing it, without reading? How many times did I see 2 functions in one file, named the same, doing the same, but in different way? How many times your code would be better if you read it and noted that you should use 2 ifs instead of 10?

4) Test it.
-----------

While working at the university, many student had sent to me their code... not working code. They simply wrote it, quickly sent to subversion and were waiting for my opinion. They were really surprised when I told them that I cannot compile their code. Sometimes they were so sure about the quality of their code, they didn't run any tests and it crashed while running some operations.

Some people say that if you make some mistake in c++, compiler says it to you, but if you do in PHP, client sends you list of errors. Please, assign this part of development to yourself and test it.

5) Comment it.
--------------

It doesn't matter if you're writing something for yourself, your company or your client. Comment everything, even if it's simple if statement, which one you assume as really simple. In some time it might be really difficult (even for you!) to understand what is done at some point. With comments you'll remember evething, forever :-)

6) Keep trying.
---------------

The best way of learning how to create good code is to try, and try, and try. Practice is the best.

