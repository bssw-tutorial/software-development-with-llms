---
title: "Outline and Learning Objectives"
teaching: 0
exercises: 0
questions:
- "Key question (FIXME)"
objectives:
- "First learning objective. (FIXME)"
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---

Outline for INTERSECT, developed by David E. Bernholdt, Lauren E Milechin, and Dave Rumph

## Learning Objectives

* Understand the role of copyright and licenses in guiding how developers approach contributing to the code and users approach using it.Understand why open-source licenses are popular in scientific software.
* Understand why using existing open-source licenses is preferable to creating new ones.
* Understand what tools are available to help select open-source licenses.
* Understand the necessity and value of clearly documenting the choice of license in your code repository and in the code itself.

## Outline

  * Since 1989 (in the U.S.) creative works, including software, are “born copyrighted”.
      * The owner of the copyright is either the author or (more commonly, in practice) the author’s employer as “work for hire”.
      * Most employment contracts include clauses about intellectual property rights (copyright, patents, trademarks)
      * The default “license” associated with copyright is “all rights reserved” to the holder of the copyright.
  * Specifying a license provides clarity as to how others can contribute to or use the software.
      * Contributors: How can maintainers use the contributions?  What rights do contributors maintain in their contributions?
      * Users: Interaction with licenses of other software (e.g., an application or tool and its dependencies).  Potential for vendor adoption, commercialization, etc.
      * The choice of license should be treated as a _tool_ for the greater goals of the project and the software.
  * Open source licensing is widely (though not exclusively) used in the scientific software community.
      * Visibility into the software producing scientific results is considered by most to be consistent with the scientific method.
      * Many may see open source licensing as an approach to sustainability of the software – getting others to contribute.  This is magical thinking, and rarely happens in practice. Open source licensing is (probably) necessary, but not sufficient to attract outside contributors.
  * The de facto arbiter of whether a license is, in fact, “open source” is the Open Source Initiative (OSI, [https://opensource.org/](https://opensource.org/)).  
      * The Free Software Foundation (FSF) is also influential in open source licensing discussions ([https://www.fsf.org/licensing/](https://www.fsf.org/licensing/)). 
      * Choose an existing OSI-approved license rather than creating a new one.  There are ~80 to choose from that cover most situations.
      * OSI has been reluctant to add to the proliferation of open source licenses by approving new ones.
      * Some publication venues (e.g., Journal of Open Source Software), will only accept OSI-approved licenses.
      * There are tools available to walk you through decision trees to select open source licenses, such as [https://choosealicense.com/](https://choosealicense.com/).  They can be very useful.
  * The primary decision point in open source licensing is “permissive” versus “restrictive” (also referred to as “copyleft” or “viral”).  As with all software licensing, there are many considerations that may apply.
      * Permissive licenses allow derivative works to be released under a different license, even a proprietary one (though in practice, this is rare). Copyleft licenses require that derivative works be released under the same license as the original, although they do not require the release of the derivative works. (They can be kept private.)
      * Because of the “viral” nature of copyleft licenses, many commercial organizations prohibit use or dependence on copyleft-licensed software or libraries. For example, if you want an HPC vendor to be able to take your numerical library and optimize it for their platform and offer it as a “built-in” part of their software stack, you should probably choose a permissive license.
  * Once you’ve chosen a license, you should ensure that it is indicated clearly in your software and documentation.
      * A LICENSE file in the repository is a common starting point.  Typically it contains the actual text of the chosen license.
      * Best practice is to also mark individual source code files with copyright notices at the top of each file.  Whether you need to include the entire license is debatable.   You can probably refer to the text of the license elsewhere, along the lines of “License: 3-clause BSD, see file LICENSE”.
  * This discussion has merely scratched the surface of software licensing.  If you wish to delve deeper, consider taking a look at [Introduction to Software Licensing](https://ideas-productivity.org/events/hpc-best-practices-webinars/#webinar024) from Best Practices for HPC Software Developers webinar series, and the many resources mentioned therein. 
* Activities:
  * 10 min: Find out who owns the copyright on software that you produce in the course of your work.
  * 10 min: Pick a piece of software that’s relevant to your work, e.g. NumPy. Find out what license it uses.
* External resources: [Introduction to Software Licensing](https://ideas-productivity.org/events/hpc-best-practices-webinars/#webinar024) from Best Practices for HPC Software Developers webinar series

{% include links.md %}
