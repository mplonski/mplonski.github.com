---
layout: post
title: "Checking if python's module is installed"
description: ""
category: code
tags: [python, bash]
---
{% include JB/setup %}

How to check if specified python's module is installed in our system?

One day I decided to make `./configure` script for the [lightnews](https://github.com/mplonski/lightnews) and I had no idea how to check if all requires libraries are installed. Then I found one, I think the simpliest, way -- just trying to import modules and checking if there're any exceptions.

Python file responsible for checking:

{% highlight python %}
try:
	import getpass
	print "ok"
except:
	print "nok"
{% endhighlight %}

This script (let's call it `test.py`) is trying to load `getpass` and printing `ok` if he succeeds, or `nok` if he doesn't. We could do nothing if it cannot load `getpass`, but it looks better and it's easier to debug / implement something more.

Next part of our script is `./configure`, main script responsible for checking our system. Let's deal with bash this time:

{% highlight bash %}
echo "Checking for python-module"
lntest=`python test.py 2>/dev/null`
if ! test $lntest = "ok" ; then
	echo "Cannot find python-module"
	exit 1
fi
{% endhighlight %}

As you can see, we're running `test.py` (remember to check if python is installed!), next we're analyzing response and throwing an error or passing and executing code below.

