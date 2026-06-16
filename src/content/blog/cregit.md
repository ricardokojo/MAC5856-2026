---
title: "Phase 2: contributing to cregit"
description: ""
pubDate: "2026/06/15"
heroImage: "../../assets/blog-placeholder-5.jpg"
---

**Last updated at**: June 15th, 2026.

This is the post about our contributions to a different project. [Ellian Carlos](https://elliancarlos.com.br/posts/tag/mac0470/) was already involved in this project, so [Gabriel Braga](https://gabrielbraga7.github.io/blog/posts/desenvolvimento_software_livre/) and I decided to keep working as a trio and contribute to [cregit](https://github.com/cregit/cregit).

## About cregit

[Cregit](https://github.com/cregit/cregit) is a pretty interesting tool that creates a token-based view of code contribution. Just like [git-blame](https://git-scm.com/docs/git-blame) does line-by-line, cregit does it token-by-token, which allows for more granular and in-depth analysis. This tool is endorsed and used by [Linux Foundation](https://www.linuxfoundation.org/).

However, looking at the repository and source code, we found out that the project is not actively maintained. The last commit was merged 3 years ago. Before that, it was 7 years ago. There are also some issues and PRs open, but no responses.

We discussed points of improvement together and tried to tackle them.

## Trying to contribute

Cregit is pretty clever, but there plenty of room for improvements. Since the project was created years ago, and not actively updated, the first challenge was making it run  locally. It was necessary to update some of the dependency versions and source code.

Ellian worked on those updates, also creating some [devenv](https://devenv.sh/) files to run the project with [Nix](https://nixos.org/), and opened a [PR on cregit's repo](https://github.com/cregit/cregit/pull/16). Since we got no answers (kind of expected), we decided to create our own fork.

## Next try: create a fork

It was decided to create a GitHub Organization with our fork of cregit: [cregit-codev](https://github.com/cregit-codev/cregit). Now, with our own cregit, we started tackling all the other improvements that we discussed earlier.

Gabriel created a single shell script to run all steps of cregit, that were manual prior to this. We also discussed the possibility of parallelize some steps, which will be implemented later on. I worked on a couple of documentation improvements, like updating READMEs to Markdown and creating a contributing guide. We even got a PR from an unknown user :D

We created plenty of [issues](https://github.com/cregit-codev/cregit/issues) to keep track of the process. There's still a lot that can be improved, so we'll keep working on it.

That's it for phase 2.
