---
title: "First contributions"
description: ""
pubDate: "2026/04/19"
heroImage: "../../assets/blog-placeholder-4.jpg"
---

This is the first post about our Kernel contributions. Since I'm in a trio with [Ellian Carlos](https://elliancarlos.com.br/posts/tag/mac0470/) and [Gabriel Braga](https://gabrielbraga7.github.io/blog/posts/desenvolvimento_software_livre/), we have to send two patches.

We briefly got together and decided for a `mutex lock -> guard` and a code duplication one.

## First patch on guard locks

To select a file to contribute, I simply ran a `find` command to see in which C files the `mutex_lock` and `mutex_unlock` were being used. There were some candidates, but some of them were too complicated, with too many things tangled with the locks. On the other hand, others were too simple, with only one or two locks to be changed. We decided to go for the `/drivers/block/null_blk`, which looked like an important driver, while still looking approachable.

Ellian and I worked closer on this one, while Gabriel looked at the other patch. We discussed the changes, while sending the `git diffs` to each other, compiling and checking if it worked. In the end, we update 3 files: `main.c`, `zoned.c` and `nullblk.h`. In the contribution, we also included `spin_lock` and `spin_unlock` changes, as Ellian suggested.

After sending the simulation patches to our emails and course's CI, we then sent the patch to the world by the end of Friday, April 17th.

We got a rapid response from the maintainer on Saturday, which pointed out some parts of our refactor that didn't make sense. He made it pretty clear that it was an stupid error xD. We quickly fixed it and sent the v2 on Sunday.

We're still waiting for another review.

## Second patch on code duplication

The second patch was a 90% code duplication, suggested inside the pad, inside the `light/veml6030.c` file.

Gabriel was the one tackling it. He created the patch, while Ellian and I reviewed it and tested it. After some small suggestions, we sent the patch on Monday, April 20th.

Once again, we got a quick review, pointing out a different way to implement the refactor. This time, the reviewer was candid and looked interested in the contribution, although we needed to adapt some things to their code standards.

At the time of this post, April 21st, we still need to start coding the v2.
