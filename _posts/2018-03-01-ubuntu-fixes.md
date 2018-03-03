---
layout: post
title: "Ubuntu fixes"
date: 2018-03-02
use_math: true
---

I have experience some problems in Ubuntu installation on my MacBook Air 2012. Granted my favorite laptop is aging, 5 years to be exact, but I still love it.

The following are some hacks that I did to make Ubuntu run a bit better on my machine:

MacOS Version 10.13.3
VirtualBox Version 5.2.6
Ubuntu Version 17.10.1
GuestAdditions Version 5.2.6 but it's really 5.2.7

*Problem* Cannot perform "Insert Guest Additions CD image..."

[move the GuestAdditions image outside of default directory](https://askubuntu.com/questions/979955/ubuntu-17-10-screen-blinks-in-virtualbox-on-macbook-pro).


[commands to install GuestAdditions](https://askubuntu.com/questions/985815/vboxclient-seamless-failed-to-start-stage-setting-guest-irq-filter-mask-err)

sudo apt-get install gcc make perl
cd /media/lorenzo/VBox_GAs_5.2.6/
sudo ./VBoxLinuxAdditions.run
sudo reboot

[install a new version of GuestAdditions](https://www.virtualbox.org/download/testcase/VBoxGuestAdditions_5.2.7-120528.iso)

[Wayland to Xorg](https://askubuntu.com/questions/961304/how-do-you-switch-from-wayland-back-to-xorg-in-ubuntu-17-10)

/etc/gdm3/custom.conf and uncomment the line

#WaylandEnable=false by removing the # in front.

x
Delete a character

:wq
Write and quit


