---
layout: post
title: "[linux] getting fortune"
description: ""
category: code
tags: [linux, fortune, bash]
---
{% include JB/setup %}

It's high time for some technical post in English!

Do you find working in terminal dull'n'borring? What about reading some random joke / quote every time you open the terminal? There's a simple fix for that!

Firstly, I'd like to say that this entry is mainly for Debian/Ubuntu users. I'm not sure if it's working in other distributions, simply haven't tested it.

Secondly, you need to install packages **cowsay** and **fortune**. In Debian/Ubuntu it's done this way (firstly run **su** to log into root's account):

{% highlight bash %}
apt-get install cowsay fortune
{% endhighlight %}

Thirdly, you need to download the code presented below and save it to the file named e.g. fortune.sh.

{% highlight bash %}
#!/bin/bash

function show_fortune {
	RANGE=3
	number=$RANDOM
	let "number %= $RANGE"
	case $number in
		0)
			cow="moose"
			;;
		1)
			cow="tux"
			;;
		2)
			cow="koala"
			;;
	esac

	RANGE=2
	number=$RANDOM
	let "number %= $RANGE"
	case $number in
		0)
			command="/usr/games/cowsay"
			;;
		1)
			command="/usr/games/cowthink"
			;;
	esac
	/usr/games/fortune | $command -f $cow
}

show_fortune
{% endhighlight %}

Lastly, you can execute this file or run command **show_fortune** (after executing this script) and it should give you something like this:

	 ______________________________________
	/ Another good night not to sleep in a \
	\ eucalyptus tree.                     /
	 --------------------------------------
	   \
	    \
	        .--.
	       |o_o |
	       |:_/ |
	      //   \ \
	     (|     | )
	    /'\_   _/'\
	    \___)=(___/

If you require it to start every time when you open new terminal, just add this script to the right file in your profile's directory, e.g. .bash_profile, etc.

