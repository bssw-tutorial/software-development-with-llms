---
title: "Documenting Your Choice of License"
teaching: 10
exercises: 10
questions:
- "What are the two basic strategies for documenting your choice of license?"
- "What information should you include in each file in your software?"
objectives:
- "Understand the importance of marking your software with your chosen license and copyright information."
keypoints:
- "License and copyright information can be documented in a centralized manner (at the repository level) and within individual files."
- "Individual files should include enough information to identify that they are copyrighted and licensed and point the recipient to the details."
---

So you've chosen a license for your software.
Now you need to ensure that people are aware of it!
This is particularly important for open-source software because you won't have the interaction of someone having to sign and return or otherwise indicate their acceptance of the terms that you would have with a proprietary license.

## Two strategies for documenting your license

There are, in essence, two strategies for indicating your choice of license.
The first is to put it in a file at the repository level.
The second is to put it inside the individual files.
The centralized approach has the advantage of simplicity and maintainability.
However, if an individual file is separated from the distribution or repository, the recipient won't see the copyright and license information if the notice only appears in a central file.

The [Software Freedom Law Center](https://softwarefreedom.org/)'s (SFLC's) whitepaper on [Managing copyright information within a free software project](https://softwarefreedom.org/resources/2012/ManagingCopyrightInformation.html) suggests that the best practice is to do *both*.

> ## Discussion
>
> Have you ever received a file by itself, outside of the context of a version control repository or complete distribution of the package, for example as a potential solution to a problem or a bug?
> Was the origin of the file and its copyright and licensing evident to you?
> Or perhaps the person who gave it to you told you about the license and copyright terms?
>
> Did that file (or parts of it) end up in another software package that you were working on at the time?
{: .discussion}

## Centralized license and copyright information

You should place the complete copyright information together with the text of the license you've chosen in a prominent location in the main directory of your repository.
In the past `COPYING` used to be a popular recommendation for this file, but `LICENSE` seems like a more obvious choice and is probably more commonly used these days.

If your package is more complicated, with multiple licenses, they can often naturally be grouped into subdirectories with consistent licensing and each subdirectory can include an appropriate `LICENSE` file.
If the licensing structure is sufficiently complex, it may be worth placing a "roadmap" to the various licenses applying to different parts of the code in the top directory.

## Tracking authorship and copyright information

Every person who makes a non-trivial contribution to a software package has a copyright interest in that package.
(There's no legal definition for what constitutes a non-trivial contribution.
The package maintainers need to determine that on a case by case basis.
Fixing a typo, or even perhaps a simple bug fix may not be considered substantive.  But a complex bug fix or implementing new functionality probably would be.)
Such a list can get rather long and could change frequently as new contributors join.
(Though if many of the contributors are performing work for hire and their employers actually own the copyright, the list of rightsholders may not be so long after all.)
But it is important to maintain this information to the best of your ability to ensure that contributors get the credit they deserve and contributors can be identified if legal issues arise.

If used carefully, version control systems provide a good means to track authorship.
But you need to use the version control tools in such a way that maintains the file histories as files are moved, renamed, etc.
In other words, instead of changing the name of a file by `git rm`ing the old name and `git add`ing the new name, use `git mv` so that the history (of commits and the authorship of those commits) follows the file through the name change.

But this authoritative information about authorship is only available in the version control repository, using your version control tool.
If the package is bundled up and distributed as a tarball, or in some other form outside of the repository, this information may be inaccessible to the recipient.
The same is true for individual files which might be distributed outside of the package for various reasons.

So the recommendation is to construct a copyright notice for the entire repository (as opposed to for each individual file), and try to do a reasonable job of keeping it up to date.
The most likely place for the copyright notice to live is in your `LICENSE` file because the license normally includes a copyright notice.
But another option, if you prefer, could be a separate `COPYRIGHT` or `AUTHORS` file.
Note, however, that the copyright holders are not necessarily the authors of the code, depending on whether the authors or their employers are the rightsholders.

## File-scope license and copyright information

As a point of reference, the recommendation of the FSF is to include the following in the header (beginning) of *every* file in the package:

1. one sentence naming and briefly describing the program,
2. the copyright notice of the authors,
3. the name(s) of the license(s) under which the software is available,
4. a brief warranty disclaimer, and
5. a URL pointing to the full copy of the license.

Others recommend including the full text of the license rather than just the name and a URL.
This is a lot of information to insert into every file and a lot of information to maintain.
Note that the contributors to each individual file are likely to be different, so in principle, each file could have a *different* copyright notice, each of which would need to be maintained.
All of which seems a little overboard for most purposes.

The SFLC's suggestion is to boil the per-file header down to the essentials.
You want enough information that if the file was distributed separately from the rest of the repository, the recipient could identify the origins of the file and know where to look for the remaining details.
Something along the following lines:

```
Copyright 2012 The Foo Project Developers. See the LICENSE file at the top-level directory of this distribution and at http://www.example.com/foo/LICENSE.

This file is part of Foo Project. It is subject to the license terms in the LICENSE file found in the top-level directory of this distribution and at http://www.example.com/foo/LICENSE. No part of Foo Project, including this file, may be copied, modified, propagated, or distributed except according to the terms contained in the LICENSE file.
```

Consider writing scripts to help you insert and maintain the file-scope copyright and license headers you decide upon.

> ## Discussion
>
> Is there any software that you work with directly, or in your community, which you know has a license associated with it but is not marked in at least one of the two ways we've discussed here (centralized and file-scope)?
{: .discussion}

## Badges

Badges at the top of `README.md` files are a popular way to summarize a variety of information about the software package.
Such badges often include testing status and other dynamic information.
Licenses are pretty static, so it may be more and so more fun than functional, but badges are available to reflect many popular licenses.

The badge generation site <https://shields.io> can automatically render a badge for any license that GitHub recognizes by simply referencing the repository as follows:

```
![GitHub](https://img.shields.io/github/license/:user/:repo)
```

for example, `![GitHub](https://img.shields.io/github/license/hpc-simtools/ips-framework)` which renders as ![GitHub](https://img.shields.io/github/license/hpc-simtools/ips-framework)

The site also provides many license badges which can be selected explicitly, such as the badge for this lesson: `[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)` which renders as [![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

While the [shields.io](https://shields.io) site lists many licenses directly, a developer named [Lukas Himsel](https://gist.github.com/lukas-h) has posted a [Gist](https://gist.github.com/lukas-h/2a5d00690736b4c3a7ba) which provides badges for even more licenses.

{% include links.md %}
