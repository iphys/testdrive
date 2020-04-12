---
created: 2020-04-12T21:32:54+01:00
modified: 2020-04-12T21:49:31+01:00
title: Jekyll on WSL on Windows
---

## Install WSL (1) and Ubuntu

My PC has Windows 10 Pro, Build 18362.

Install **Windows Subsystem for Linux** (not WSL 2, which is still Preview).

Reboot the PC.

Install Ubuntu 18.04 LTS from Microsoft Store.

As the installation process progresses, bash starts. Asked to create user and set pw.  Home directory is created in

- `C:\Users\_windowsUserName_\AppData\Local\Packages\Canonical.....\LocalState\rootfs\home`.

Once bash prompt is ready, do `sudo apt update`, then `sudo apt upgrade`.

## Install Ruby and Jekyll

On WSL bash, install ruby and jekyll.

```sh
sudo apt install ruby-dev
sudo gem install bundler jekyll
```

Installed versions are: Ruby 2.5.1p57, Jekyll 4.0.0.

## Set up Directory for Website

On WSL bash, create a directory for a website. The following
procedure is a summary of what I actually did.

```sh
sudo jekyll new foo
sudo rm -rf foo
jekyll new foo
```

Then `cd` to the directory and build the first static web page.
A local webserver will start.

```sh
cd foo
bundle exec jekyll serve
```

In a web browser, open `http://localhost:4000/`. This loads the web page.
Close the page. Hit Control-C on the command line to kill the jekyll process.

## Next Step

I should read and understand [Jekyll Step-by-Step Tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/).
