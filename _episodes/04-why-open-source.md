---
title: "Why Choose Open Source Licensing?"
teaching: 18
exercises: 20
questions:
- "What are some of the reasons for preferring open-source licensing over proprietary?"
- "Does open-source licensing prevent you from making money off of your software?"
- "Does open-source licensing guarantee the sustainability of your software?"
objectives:
- "Understand some of the reasons for preferring open-source licensing over proprietary."
- "Understand that the choice of license is a tool for your software and your project goals."
keypoints:
- "Philosophical reasons to choose open-source licenses include consistency with the scientific method and openness of publicly funded research results.  Another reason is that it facilitates building a community around your software."
- "Most software-related business models work as well for open-source software as for proprietary."
- "Open-source doesn't guarantee that outsiders will engage with your software.  You'll need to work to build a community of contributors and users."
---

## The philosophical reasons

One of the most common reasons that developers of scientific software choose open-source over proprietary licensing is because they consider it to be consistent with the scientific method.
The scientific method requires transparency and reproducibility, and in computationally-based science, this implies that the "apparatus" (i.e., the software) be available for others to inspect and understand and that others should be able to use it to reproduce the relevant (computational) experiments.

Another philosophical reason that many cite is that the results of publicly-funded research (e.g., software produced with research funding) should be publicly available.

And, finally, there's the altruistic reason that releasing the software as open source may help others.

## Other considerations favoring open source

Even if you're not completely swayed by the philosophical arguments above, there may be other, more practical reasons to lean towards open-source licensing.

One very simple, but often compelling, reason is that the sponsor of your research may require (or encourage) you to release your software products as open source.
At this point in time, many (most) U.S. federal research sponsors are encouraging "open science" with policies that explicitly or implicitly encourage open source.
Within the U.S. Department of Energy, several programs have adopted a [policy](https://science.osti.gov/-/media/ascr/pdf/research/docs/Doe_lab_developed_software_policy.pdf) that prefers open-source release unless there is a reason not to do so.

Another common reason to favor open-source licensing is to facilitate building a community around your software.
Understandably, an open and accessible code base is likely to be more attractive and have a lower barrier to entry for potential contributors than closed source.
On the other hand, having to complete an explicit license agreement is a barrier to use (or contribution) of closed-source software.
At most institutions, only a few people are authorized to sign legal agreements on behalf of the organization.
Usually, a license agreement would have to be reviewed and executed by an IP lawyer, which can cause delays.
In some cases, the institution and the licensor may be unable to come to an agreement on the terms and it may be impossible to obtain the license.

And, on a related note, if you're using a proprietary license, you have to manage and archive all of the paperwork associated with those licenses so that you know who your licenses are.
Some find that this is more trouble than it's worth.

## Debunking some arguments *against* open-source

There are also a variety of reasons that some people argue against open-sourcing software, which don't hold up if you dig a little deeper.

### Myth: You can't sell open-source software

It is a common misconception that open-sourcing software prevents you from making money off of it.
In fact, there are many different business models that are commonly used around software, and nearly all of them are as applicable to open-source as to proprietary software.


| Approach | Proprietary | Copyleft  | Permissive  |
| :-- | :-: | :-: | :-: |
| Sell the software | yes | yes | yes |
| “Freemium” or “dual licensing” allows free use by some, paid by others | yes | yes | yes |
| Relicense to proprietary | n/a | no | yes |
| Sell convenience, e.g., packaging, installation media, pre-compiled executables | yes | yes | yes |
| Sell professional services around the software, e.g., training, technical support, consulting | yes | yes | yes |
| Sell custom development services, e.g., proprietary extensions, accelerated development | yes | yes | yes |
| Sell software-as-a-service (SaaS) | yes | yes | yes |
| Sell the research | yes | yes | yes |

### I don't want others to profit from my open-source software

If you're using a permissive license, someone else can take derivatives proprietary.
But, with the wealth of permissively licensed software out there, this is not a common experience.
If you're still concerned, you might prefer a copyleft license, which will prevent this scenario.

But there might be other considerations at play, too.
For example, what if you *do* want a commercial entity to use your software -- for example, for it to be adopted by a computer vendor or distributed in a Linux or similar large distribution of software?
This is a way of getting your software broader exposure and broader distribution.
Assuming you're not expecting financial compensation, this kind of collaboration becomes much easier with open-source licensing, and more specifically with *permissive* licenses.

#### Commercial entities prefer permissive licenses

Many commercial entities find copyleft licenses scary.
They are concerned about how far the viral nature of copyleft licenses reaches into other parts of their product.
Legal opinions on this differ, and that is little or no case law on this yet.
Since lawyers tend towards conservative answers, they will often advise their commercial clients to avoid copyleft software.
As a result, many companies will not consider working with copyleft software, only permissively licensed software.
Some (typically larger) companies consider staff working on copyleft software to be "contaminated" and will not allow them to work on other software.

#### The software-as-a-service conundrum

"Software-as-a-service" (SaaS) is a popular way of making software products available today.
Many SaaS products make extensive use of open-source software.
Some developers don't like the possibility that another company can trivially monetize (other people's) software by turning it into a SaaS product.
It may compete with the developer's own SaaS offering.
And the SaaS provider can keep enhancements proprietary while making the benefits available in the SaaS product.

Use in a SaaS product is not considered distribution of the software per se.
But some licenses, such as the [GNU Affero General Public License](https://opensource.org/license/agpl-v3/) include "network" clauses that require that the source be made available to remote users of the service.
Other ways of addressing these concerns tend to result in licenses that are not open source.
In some cases, key modules are changed to proprietary licenses while others remain open.

An article on the [Ars Technica](https://arstechnica.com/) website discusses the SaaS conundrum further: [In 2019, multiple open source companies changed course—is it the right move?](https://arstechnica.com/information-technology/2019/10/is-the-software-world-taking-too-much-from-the-open-source-community/)

### I want to protect my intellectual property

Another concern that people sometimes raise about openly accessible code is that others can use the novel ideas embodied in it to "scoop" them.
Proprietary licenses, by their nature, allow you to keep the source code private, so you can avoid this concern.
But there are also strategies that you can use with open source to provide functional protection.

First, as we discussed earlier, open source licenses do *not* require that you make derived works public, only that *if* you do, you make the source available.
So the basic strategy is not to disclose your novel derived work until you've had a reasonable chance to exploit the results of your work.
For example, you might wait until you've published the initial papers about the method and results that might not be obtainable with other methods.
Or you might give yourself (or your team) a fixed "exploitation period" (e.g., one year) before publishing the source code.
This is similar to a compromise that's often used in academic publishing, where a sponsor wants the publications to be open access, but they allow the publisher a proprietary exploitation period (also often one year) before making the document openly available.

## Licensing as a tool

As we've suggested, the licensing of your software should be viewed as a tool to help you pursue your goals for the software and the associated project.

Basically, you want to ask yourself (and your collaborators) what rights you want to grant to others or retain for yourselves:

* Who can use the program?
* Can users see the source code?
* Can users modify the source code?
* Can the users redistribute the original or modified code?

And think about how these choices will affect your project, would-be contributors to the software, and would-be users of the software.

> ## Discussion
>
> Have you ever been involved in a discussion of proprietary versus open source licensing for a software package?
>
> What arguments were made in favor of proprietary licensing?
> What arguments were made in favor of open-source?
>
> Was there a particular argument that carried the day, in either direction?
{: .discussion}

## Avoid magical thinking: Open-source is no guarantee of sustainability or community

Open-source is a great tool to help you build a community around your software.
But you shouldn't imagine that simply slapping an open source license on your software makes it sustainable.
Besides having software that is potentially useful to others, you'll need to work at it if you want to build a community that contributes to and helps support your software.
Many open source software projects never receive any outside contributions.
In a webinar entitled [What I Learned from 20 Years of Leading Open Source Projects](https://ideas-productivity.org/events/hpc-best-practices-webinars/#webinar056), Wolfgang Bangerth, one of the founders of the deal.II package, offers his experience of what it took to build a small single-group software project into a truly community-based resource -- and what it takes to keep it going.

> ## Discussion
>
> Does your research community include any truly community-based software packages?
> Packages which are both widely used *and* widely contributed to?
>
> If you happen to be involved in such a project, what is your role?
> User?
> Contributor?
> Maintainer?
> What is your experience with the community?
{: .discussion}

{% include links.md %}
