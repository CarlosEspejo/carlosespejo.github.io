---
layout: post
title: Kick off 2015 with a fresh install
tags: install yosemite ruby rails
---

Since my MacBook Pro (Retina, Mid 2012) started to feel very slugish.
After almost 3 years it was time for a fresh install.

I will be covering the following:

  * Fresh install of Yosemite
  * How to install ruby
  * How to install Postgresql
  * How to install mongodb

### Fresh Install of OSX Yosemite:
*Warning:* Before beginning make sure you backup all your files.

First you have to download Yosemite from the App store and get a blank USB drive with at least 6GB of storage (Warning: The USB drive will be erased).
Run the following command and make sure that --volume is pointing to your blank USB drive

``` bash
sudo /Applications/Install\ OS\ X\ Yosemite.app/Contents/Resources/createinstallmedia \
--volume /Volumes/MYBlANKDRIVE --applicationpath /Applications/Install\ OS\ X\ Yosemite.app --nointeraction
```

  * When the above process completes reboot your machine while holding down the option key
  * When the OSX Startup Manager appears select your USB drive to boot from
  * Select Disk Utility go to the Erase tab, select Mac OS Extended (Journaled) for the file system
    and format your Mac's starup drive
  * Then select Install OS X

