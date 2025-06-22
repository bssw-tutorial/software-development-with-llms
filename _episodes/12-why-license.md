---
title: "Why You Should Choose a License"
teaching: 6
exercises: 20
questions:
- "What are the two basic categories of software licenses?"
- "What are the benefits of specifying a license for your software?"
objectives:
- "Understand the reasons to specify a license for your software."
keypoints:
- "The two basic categories of software licenses are *proprietary* and *open-source*."
- "Specifying a software licenses provides guidance for would-be contributors and users about how they can engage with the software."
---

## The spectrum of software licenses

As we've mentioned, licenses provide a means to convey selected rights from the owner of those rights to others.
Different licenses can be defined that convey different rights.
You can think of software licenses as spanning a spectrum.

![Software licenses span a spectrum of possibilities depending on what rights they convey to the licensee.]({{ page.root }}/fig/license-spectrum2.png)

At one extreme, all rights are reserved to the owner of the copyright.
This is the situation that applies when you do not specify a license, but it is also common to see "All rights reserved" stated explicitly as a form of license.

Proprietary licenses, also referred to as closed-source licenses, typically convey rights to use the software but reserve rights to access or distribute the source code.
Software that is distributed under a proprietary license is most often provided in the form of an executable, though in some cases, licensees may receive the source code (e.g., so that they can build it on platforms that the copyright owner may not have access to), but be restricted from redistributing it.

Free or open licenses generally convey more rights to the licensee, typically including access to the source code and the right to redistribute it.
Within the range of open licenses, they can be broadly categorized as "copyleft" or "permissive".
We'll take a deeper look at open licenses in the next episode.

At the other extreme of the licensing spectrum is the public domain, which is not so much a license as a disclaimer of all rights in the work.
Works in the public domain do not have a copyright or a copyright holder.
Anyone can do whatever they want with such works.

> ## Activity
>
> Identify one software package that's important to your work that has a proprietary license.
>
> Identify one software package that's important to your work that has an open-source license.
>
> Is there a software package that's important to your work that doesn't specify a license?
{: .challenge}

## Why license your software

Licenses play an important role for both developers and users of software.
The license provides guidance as to how developers can contribute to the software and how users can approach using it.

Developers should expect that their contributions to the code base will be licensed on the same terms as the original work (unless other arrangements are made).
With closed-source licenses, the developer may lose subsequent access to their contributions once they are subsumed into the proprietary code base.
Open source licenses, on the other hand, provide for access to the source code and the ability to redistribute the code.
Developers contributing to open-source projects can therefore expect ongoing access to their contributions and the ability to redistribute the code.

The user's perspective is somewhat similar.  With a proprietary license, they are likely to be limited to using executables that the copyright holder chooses to make available.
If the source code is not available, the user has no way of understanding what the code is actually doing.
Open-source licenses, on the other hand, ensure the availability of the source code, and so the user's ability to (try to) build the software on different computer platforms.
The user can review the code to see what it is doing when it is run.
While there may well be helpful user communities in either case, the fact that everyone in the community has access to the source code of an open-source package may make it more likely that the user can obtain assistance from people besides the copyright holder.

> ## Discussion
>
> Suppose you hear someone at a conference talk about a software package that might be very useful in your work with a few modifications.
> You chat with them about the possibility of collaborating around their software.
>
> If they mention that the software is proprietary, would that influence your decision about pursuing a collaboration?
>
> If they mention that the software is open source, would that influence your decision about pursuing a collaboration?
{: .discussion}

Ultimately, the choice of how to license your software should be thought of as a *tool* in pursuing the greater goals of your software and your project.

{% include links.md %}
