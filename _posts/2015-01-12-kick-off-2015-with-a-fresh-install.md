---
layout: post
title: Kick off 2015 with a fresh install
tags: install yosemite ruby rails
---

Since my MacBook Pro (Retina, Mid 2012) started to feel very slugish.
After almost 3 years it was time for a fresh install.

### Fresh Install of OSX Yosemite:

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
  * Then select Install OS X and continue    the installation

### Development tools

#### Xcode & Command Line Tools
Install Xcode from App Store
Go to [developer.apple.com/downloads](https://developer.apple.com/downloads/) and download
Command Line Developer Tools (OS X 10.10)

#### Home Brew
Open a terminal and run `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)”`

```bash
brew install git openssl imagemagick rbenv ruby-build \
             rbenv-gem-rehash libxml2 libxslt automake ssh-copy-id graphviz
```

#### Oh My ZSH!

```bash
brew install zsh
curl -L http://install.ohmyz.sh | sh
chsh -s /bin/zsh
```

#### rbenv

```bash
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(rbenv init -)"' >> ~/.zshrc

```

#### Install Ruby
```bash
rbenv install 2.2.0
rbenv global 2.2.0
```

#### Mac Vim & Janus: Vim Distribution
```bash
brew install macvim
curl -Lo- https://bit.ly/janus-bootstrap | bash
```

#### PostgreSQL
```bash
brew install postgresql
```
after installing postgres add the following to your .zshrc or .bashrc

```bash
export PGDATA=/usr/local/var/postgres
alias start_pg="pg_ctl -D $PGDATA -l $PGDATA/server.log start"
alias stop_pg="pg_ctl -D $PGDATA stop -m fast"
```

#### Other Development Apps
  * Sublime Text
  * Slack
  * HipChat
  * Dash
  * Navicat Premium Essentials
  * Microsoft Remote Desktop
  * Evernote
  * LimeChat
  * VirtualBox
  * Vagrant



### Day to Day Applications
  * Chrome
  * Firefox
  * LastPass
  * Lightroom
  * Marked
  * Soulver
  * Clear
  * Pages
  * Numbers
  * Keynote
  * Pocket
  * Spotify
  * Pandora
  * Drobo Dashboard

