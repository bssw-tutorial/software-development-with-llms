---
title: "Collaboration and Licensing"
teaching: 17
exercises: 15
questions:
- "What are the concerns with accepting code from collaborators?"
- "What mechanisms are there to ensure collaborators agree to license terms?"
- "What concerns are there with using code from online forums?"
- "Why are LLMs challenging for copyright and licensing?"
objectives:
- "Understand the challenges surrounding code contributed from outside the project."
keypoints:
- "Collaborators may be resctricted in their ability to contribute to open source projects (e.g. industrial partners) or unable to copyright their work (government employees)."
- "You can include a Contributor License Agreement (CLA) to ensure collaborators agree to license terms prior to committing code."
- "Stackoverflow content is licensed as CC BY-SA, which is incompatible with permissive or proprietary licenses."
- "License and copyright around LLM-generated content is actively being litigated."
---

If you are lucky, you have an open-source project with an active user base and
a few developers to help field issues.  As a project grows, it's possible you
will get pull requests from people you've never met.  Even if the code looks great,
it's possible the has author inadvertently has caused a licensing issue.

A somewhat related topic is how to handle code snippets from external sources
like web forums or large language models.

## Contributors and Licenses

There are two cases where a contributor can cause problems with licensing your code.

First, if you have a copyleft license, contributors from industry may be reluctant
to contribute over fear of accidentally violating the terms of the GPL license.
Since GPL requires derivative works to be copyleft, if the contributor were to
incorporate some of the code into a larger project, they would be obligated to
release the entire code base under the license terms.

Alternatively, if you have a restrictive license, it's possible a contribution may not be
subject to copyright at all!  Any work from a government employee, say a researcher at a
federal agency, is not subject to copyright and is in public domain.

It is important to communicate your license terms to all collaborators and decide
on a license early in a project's life cycle.  Changing a license is possible,
but may require the explicit approval of all contributors; for larger, older
projects the prospect is daunting.

Part of being proactive is developing and publishing your CONTRIBUTING guidelines.
You can also choose to use a Contributor License Agreement (CLA), which is a legal
document that new contributors must sign prior to merging their code.  While
protective of the software project, CLAs may limit inclusivity by acting as
a barrier to first time contributors.  They can also create a power imbalance between
maintainers and contributors.  Practically, CLAs often require review and
approval by the legal department of the contributor.

A Developer Certificate of Origin (DCO) is a lighter agreement that allows
contributors to confirm the code they commit is suitable for the project license.
They can be integrated into a PR or commit message instead of a separate legal document.
In either case, the policies for contributors should be clear and easy to find
and verify if legal issues do arise.

> ## Activity
>
> What are the contributor guidelines for some open source code you use?
>
> Pick one dependency or utility you regularly use.
> Does the project have a CONTRIBUTING file? CLA? DCO?  Does the license
> mention contributors?
{: .challenge}

## Code from internet forums

Question and answer forums like stackoverflow provide a valuable avenue for
developers to connect with knowledgeable users covering a range of topics from
installation, language usage, and debugging.  It is satisfying to find the exact
answer to your problem so you can get back to work, but how can you integrate
the answer in accordance with the license agreement of the forum?

The best case is to take the answer and distill it to your application.  Say
you are searching for how to plot a scatter plot with transparency given by
another column in your dataframe.  An answer may suggest matplotlib, seaborn,
or another plotting library.  When you integrate the answer into your code,
you will have to modify the answer to fit your variables and when finally put
in place, the one line could have come directly from the documentation.  Ideally
you would use the suggested answer to further research the documentation and
develop a distinct call.  In this case, you are using an internet forum as a
shortcut to library documentation.  You don't have to disclose where the original
idea came from, but for your own benefit it is a good idea to include the URL
in a comment.

But what if you are searching for something like a binary search written in python,
or the answer contains a function snippet for performing the task you need?
Fair use does not use length as a factor, if you directly copy and paste code
and you want to distribute that code, it would then fall under the original license,
for stackoverflow, that is CC-BY-SA.

> ## Pop Quiz
>
> If you use CC-BY-SA work in your project, what kind of license should you use?
>
{: .challenge}

## LLMs and code assistants

A recent development for software engineers is the rise of large language models
capable of producing code from English descriptions.  The utilities are integrated
in many search engines, IDEs, or as standalone assistants.  While performance
and utility can vary wildly, LLMs can increase developer productivity by removing
some of the tedious jobs.  Just be wary, correct-seeming code can be worse than
something clearly wrong!

Just as the technological limits of LLMs are still being discovered, the legal
aspect of AI and licenses are actively being determined in court.  There are three
phases where licensing and copyright concerns appear in utilizing LLMs:

1. During training, what code has been ingested?  How do the licenses of the
code affect what is produced?
2. If you want to refine an LLM, what license is the model distributed with?
3. If I use code generate by an LLM, what attribution does it need and will it affect
my license?

### Ingested code

Unless you are training your own LLM, this is more of an interesting case study
in copyright than a day-to-day concern.  Since the implementation details of
many LLMs are proprietary, you may not know what code a model was trained on,
what license the code used, or if permission was attained to use the software
for training.

Legal challenges against AI companies have been brought up by artists and
authors, who allege the generation of verbatim passages or replication of
artistic style indicate training data included copyrighted material against
the creators wishes.  Code generation hasn't been included in these lawsuits
so far, but rulings on other domains could affect how LLMs are trained.  If you
are concerned about the origin of code used to train an LLM, look for LLMs that
provide information on the training set and uses a training set aligned with your
license and values.

### Refining an LLM

Refining a published network is somewhat straight forward!  Just like any other
piece of software, you can follow the license distributed with the material in
creating derived works from the original network.  However, the weights of
the foundation model could "contain" copyrighted material from data
on which they were trained.  It's possible that during refinement, the network
will retain the copyright material in a form that can be recovered.  Litigation
will be needed to sort out fair use, but keep in mind that refined networks
may contain the foundation model largely unchanged.

### Using code from LLMs

You may have already used code from an LLM, either to play with a new technology
or even in production to save time on development.  Continuing with the theme
of this section, we don't know all the answers until legislation and lawsuits
settle.

Consider the following scenario, you use an LLM to generate a function that is
later discovered to be verbatim from a copyrighted code base, violating the
license.  Are you liable for damages, the company that trained the network,
or the company you pay to use the LLM?  Due to the difficulties with tracking
down what input data has contributed to LLM output, you may be the most likely
party targeted for damages.

Some tools have been developed to scan LLM output to flag large snippets which
are present in other sources. Many tech companies don't allow code generation
from outside products due to privacy concerns, as well as licensing issues.
Keep in mind if you are interested in industry that reliance on an LLM for
code generation is probably not a good strategy.

The US government recently declared that AI generated work can not be
copyrighted if it's produced without human intervention beyond prompt engineering.
This is likely to apply to a work as a whole instead of snippets, e.g. if your
project has a few generated functions it could still have a copyright.  If instead
you instruct an LLM to "make a game" (and it's able to do so), that could would
not be copyrighted.  As an example, ["Zaraya of the Dawn"](https://www.copyright.gov/docs/zarya-of-the-dawn.pdf)
is a comic book where the images were produced by Midjourney.  While the text
and layout were human generated and therefore subject to copyright, the US
Copyright Office found the images could not be copyrighted.  Extending this to
software, if you have AI produce all of your UI, that portion of your code could
be public domain.

If you are developing code you intend to monetize, the safest advice would be
to avoid LLM snippets altogether.  Were it brought to light in discovery,
AI-generated code could open the door to damages over the entire code base.
Otherwise, treat LLM output like code from an internet forum, you can use it
for information and to point you towards a library call, but don't copy its
entire output.  If you do copy and paste code, you may also want to mark in the
source code what is LLM-derived.  Doing this consistently could safeguard parts
of your project that may resemble proprietary code by chance.
