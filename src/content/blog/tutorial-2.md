---
title: 'Tutorial 2'
description: 'Following tutorial 2'
pubDate: '2026/03/16'
heroImage: '../../assets/blog-placeholder-3.jpg'
---

This post is about my experience following [tutorial 2](https://flusp.ime.usp.br/kernel/build-linux-for-arm-kw/).

I learned about lots of different concepts and tools that I had never heard before.

I didn't know about `kw` (and that there are so many kernel-specific files). It was a pleasant surprise to know that this tool was developed inside ourside institute, and it worked flawlessly during the tutorial. I knew how powerful `Makefiles` can be, but once again, it worked like magic and I had no problems with them.

I also didn't know about the concept of cross-compilation, but it makes a lot of sense after learning about it. Once again, it worked without problems.

Although this tutorial is long, and it looked like there were lots of steps that could fail, it went all the way to end without issues. It took around 12 minutes to compile the Linux kernel and I was able to run the VM with the new image.

At first, it looked like the image was not running properly, as I was not able to connect with the OS' `stdio` and had no logs of what was happening, but after talking with the TAs and other students, it's one possible issue that has an easy fix. The problem is that, when creating the new VM instance, there's no reference to attach my terminal to the VM's I/O, so I get no logs. However, after the VM is up (so just wait a couple of minutes), it's possible to connect to it using `kw ssh`. After waiting a little, the VM was up and running, and I was able to connect to it and check that the new image was running.

I did this tutorial before our third class, so most of it was done at home. I only had to check this last issue with the TA, then I went on to do the tutorial 3.
