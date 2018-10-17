---
layout: post
title: "dpkg issue resolved"
date: 2018-08-19
---

I was having problem with installing new applications on application because of the constant reminder because of this:

	E: dpkg was interrupted, you must manually run 'sudo dpkg --configure -a' to correct the problem. 

Took a little while for me to figure this out. Luckily I found a [solution](http://linux.cloudypoint.com/forums/topic/ubuntu_14-04-solved-message-edpkg-was-interrupted-you-must-manually-run-sudo-dpkg-configure-a-to-correct-the-problem/) to resolve this issue. Thank you, Google.

In addition, another issue that kept popping was the version of `six`, a package used for older Python versions. I was able to fix this by:

	pip install six==1.11.0 