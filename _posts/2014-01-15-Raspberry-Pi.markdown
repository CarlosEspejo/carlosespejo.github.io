---
layout: post
title:  "Raspberry Pi, Arch Linux and Ruby"
date:   2014-01-15 21:22:42
tags: raspberrypi arch-linux
---

###Setup

After you follow the other guides and create the image boot up and [resize](http://www.thefruitycomputer.com/forums/tutorials/article/7-full-guide-to-arch-linux-on-the-raspberry-pi/) the partition. Make sure to run pacman -Syu to uprade everything.


###Install Sudo
{% highlight bash %}
 pacman -S sudo

#To give your regular user permission to use sudo, you need to edit the configuration file using visudo:
EDITOR=nano visudo

#Locate the section marked as:
##
## User privilege specification
##
#and uncomment the line below to say
 %wheel ALL=(ALL) ALL

#Save and exit.
{% endhighlight %}


###Wifi

Nothing beats the Arch Linux Wiki its packed with useful information about how to configure everything. For wifi i used Netcfg

###Ruby
[see the docs](https://wiki.archlinux.org/index.php/Ruby#Ruby_2.1)
{% highlight bash %}
# To install ruby run
pacman -S ruby

# add this to your PATH variable
PATH="`ruby -e 'print Gem.user_dir'`/bin:$PATH"

# for bundle to work correctly
export GEM_HOME=$(ruby -e 'print Gem.user_dir')
{% endhighlight %}

