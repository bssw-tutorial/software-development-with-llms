---
title: "Choosing an Open Source License"
teaching: 13
exercises: 15
questions:
- "What are some of the reasons for going with an established open-source license instead of creating a new one?"
- "What are some of the most popular open-source licenses?"
- "Name a tool that can help with a more detailed understanding of common open-source licenses?"
objectives:
- "Be able to identify some of the most common open-source licenses."
- "Know about a tool that can help you select an open-source license that meets your needs."
keypoints:
- "There are many OSI-approved licenses already available covering most needs.  Some publications or other venues require OSI-approved licenses."
- "The variants of the GNU GPL license are among the most popular copyleft licenses, while Apache, BSD, and MIT are among the most popular permissive licenses."
- "[ChooseALicense.com](https://choosealicense.com) has analyses of more than 40 open-source licenses along 13 different characteristics."
---

## Don't reinvent the license

If you want to use an open-source license with your software, the first advice is to use an existing license rather than inventing your own.
The OSI has approved more than 80 different licenses as qualifying as open source.
They cover a wide range of situations, and with that many options, you're pretty unlikely to have a need that's not already covered.
Moreover, the OSI feels that there are too many open-source licenses already, and has been reluctant to review and approve new licenses to control the proliferation.

Another reason to choose an OSI-approved license is that there are some publication venues (e.g., the [Journal of Open Source Software](https://joss.theoj.org/) (JOSS)) that will only accept OSI-approved licenses.
There is at least one case in which JOSS rejected a submission for a software package that was licensed under an institution-specific variant of the [3-Clause BSD License](https://opensource.org/license/bsd-3-clause/) which was not OSI-approved.
While there are other options besides JOSS for publishing your software, it is important to be aware of such restrictions when selecting a license.

## Considerations in selecting an open-source license

The most significant decision in open-source is between permissive or copyleft licenses.
Technically, this is a decision as to whether derivative works can be changed to a new license or not.
But it can have knock-on effects, particularly in the area of license compatibility.

License compatibility comes into play when you start combining software to get your work done.
As we discussed earlier, there are different interpretations of what kinds of combinations do or do not result in derived works which, under copyleft licensing, might become subject to the terms of the original work's license.
Permissive licenses have fewer compatibility issues.

On a related note, it is worth considering the norms of the community you and your software are engaging with.
If, for example, "everyone" in your field uses a particular license, it may be easier for your software to be accepted by others if you follow the same approach -- unless, of course, you have strong reasons for doing otherwise.

Another clause that appears in many open-source licenses has to do with the labeling of derived works, requiring that derived works be identified differently than the original.
Why would we want this?
What if someone took your code, and in modifying it introduced a bug that made all of the results it produced subtly wrong?
That could easily give your code a bad name -- unless the problem code had a *different* name that enabled the community to easily distinguish them.

## Patents in software licenses

A patent is a different form of intellectual property than a creative work like a piece of software.
But they are often connected in the software, and increasingly software licenses also include patent-related clauses.

Patents cover an invention that is useful and non-obvious.
That invention could be embodied in software.
Some people make strong arguments against the idea that inventions embodied in software should be patentable at all.
But in the legal sense, they are a reality.
If you're using a piece of software (even open source) that is covered by a patent and you don't have a license for the patent, you're infringing.
Not being aware of the patent does not excuse the infringement.
And you could be sued for monetary damages.

Historically, many open-source licenses were silent on patents -- they said nothing at all about them.
More recently, since the courts have decided that software inventions are patentable, some open-source licenses have started including patent-related clauses.

The most common type of patent clause grants royalty-free (i.e. no cost) right to use patented content owned by the copyright holder(s) (e.g. [Apache 2.0](https://opensource.org/license/apache-2-0/), [GPLv3](https://opensource.org/license/gpl-3-0/)).
(Obviously, the copyright holders can't provide licenses for other people's patents -- which is important to remember.
It is still possible that a code has (presumably unknowingly) infringed on some other patent.)
Another form of patent clause involves retaliation, effectively saying "If you sue me for patent infringement, your license to use this software is terminated", (e.g. [Apache 2.0](https://opensource.org/license/apache-2-0/)).
A weak retaliation clause is triggered by an action related to the specific software, whereas a strong retaliation clause is triggered by any patent action against the licensor.

Although it is no longer listed by the OSI, there is also a [BSD 3-Clause Clear License](https://choosealicense.com/licenses/bsd-3-clause-clear/) which explicitly states that no patent rights are granted by the license.

## Popular OSI-approved licenses

Some of the most widely used OSI-approved licenses are listed below, along with notes as to their permissiveness, compatibility, and what type of patent clause(s) it has.
Any license on this list is a good choice because they are among the most popular and well-known open-source licenses.

| License | Type | GPL-Compatible | Patent Clause(s) |
| :-- | :-- | :-- | :-- |
[Apache License, Version 2.0](https://opensource.org/license/apache-2-0/) | Permissive | v3, not v2 | Grant, Weak retaliation |
[Common Development and Distribution License 1.0](https://opensource.org/license/cddl-1-0/) | Permissive | No | Grant, Weak retaliation |
[Eclipse Public License version 2.0](https://opensource.org/license/epl-2-0/) | Weak Copyleft | Yes | Grant, Weak retaliation |
[GNU General Public License version 2](https://opensource.org/license/gpl-2-0/) | Copyleft | Yes | Implied grant |
[GNU General Public License version 3](https://opensource.org/license/gpl-3-0/) | Copyleft | Yes |  Grant, Weak retaliation |
[GNU Lesser General Public License version 2.1](https://opensource.org/license/lgpl-2-1/) | Weak Copyleft | Yes | Implied grant |
[GNU Lesser General Public License version 3](https://opensource.org/license/lgpl-3-0/) | Weak Copyleft | Yes | Silent |
[GNU Library General Public License version 2](https://opensource.org/license/lgpl-2-0/) | Weak Copyleft | Yes | Implied grant |
[Mozilla Public License 2.0](https://opensource.org/license/mpl-2-0/) | Permissive | Yes | Grant, Weak retaliation |
[The 2-Clause BSD License](https://opensource.org/license/bsd-2-clause/) | Permissive | Yes | Silent |
[The 3-Clause BSD License](https://opensource.org/license/bsd-3-clause/) | Permissive | Yes | Silent |
[The MIT License](https://opensource.org/license/mit/) | Permissive | Yes | Silent* |

\* In [Why so little love for the patent grant in the MIT License?](https://opensource.com/article/18/3/patent-grant-mit-license), Scott Peterson argues that the MIT license, which  provides the right to "deal with the Software without restriction," includes the right to use associated patents based on the language used.

## ChooseALicense.com

If you want more choices for your open-source license or are interested in clauses other than those in the table above, check out [ChooseALicense.com](https://choosealicense.com).
This tool, which was developed by GitHub and is openly curated through a [GitHub repository](https://github.com/github/choosealicense.com) starts with three very simple suggestions:

* Use the license preferred by your community
* If you want a permissive license, they recommend MIT
* If you want a copyleft license, they recommend GPLv3

But then their [Licenses](https://choosealicense.com/licenses/) page lists eight licenses that span a broad spectrum and provide analyses of thirteen different characteristics.
And their [Appendix](https://choosealicense.com/appendix/) has a table of more than forty licenses analyzed in terms of the thirteen different characteristics.
The characteristics include:

* Commercial use
* Distribution
* Modification
* Patent use
* Private use
* Disclose source
* License and copyright notice
* License and copyright notice for source
* Network use is distribution
* Same license
* Same license (file)
* Same license (library)
* State changes
* Liability
* Trademark use
* Warranty

By understanding which characteristics are important for how you want to license your software, you can use the table in the ChooseALicense.com [appendix](https://choosealicense.com/appendix/) to identify specific licenses that are worth looking at more deeply.
Once you have some candidates, you should read each of them carefully -- there may be additional clauses that you may or may not want in your license.

And remember, even the list of licenses that ChooseALicense.com has analyzed is less than half of the number of OSI-approved open-source licenses.
So don't give up!

![A snapshot of https://choosealicense.com/appendix/ taken 2023-06-28]({{ page.root }}/fig/choosealicense-appendix-2023-06-28.png)

> ## Activity: Open-source licenses in your community
>
> Try to identify 2-3 open-source software packages within your community that use different licenses.
>
> Which licenses do they use?
> Or does a single license strongly dominate your community?
> Are they permissive or copyleft?
> In what other ways do they differ?
>
> (Hint: the <https://choosealicense.com/appendix/> page might be helpful.)
{: .challenge}

{% include links.md %}
