---
created: 2020-04-12T21:32:54+01:00
modified: 2020-04-12T21:49:31+01:00
title: Jekyll on WSL on Windows
---

# Set up

Windows 10 Pro, Build 18362

Install **Windows Subsystem for Linux** (not WSL 2, which is still Preview).

Reboot

Install Ubuntu 18.04 LTS from Microsoft Store

As the installation process progresses, bash starts. Asked to create user and set pw.  Home directory is created in C:\Users\_windowsUserName_\AppData\Local\Packages\Canonical.....\LocalState\rootfs\home

Once bash prompt is ready, do "sudo apt update", then "sudo apt upgrade".

## Set up Ruby and Jekyll

On WSL Bash;

```
sudo apt install ruby-dev
sudo gem install bundler jekyll
```

## Set up Directory for Website

On WSL Bash;

```
sudo jekyll new foo
sudo rm -rf foo
jekyll new foo
```

```
cd foo
bundle exec jekyll serve
```

Then in a browser, go to `http://localhost:4000/`