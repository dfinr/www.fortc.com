---
title: Overview
revision_date: June 19, 2022
#tags:
#  - Docs as Code
#hide:
#  - navigation
#  - toc
#  - footer
---

# Doc-as-Code Overview

Documentation as Code is a method of writing documentation using the same tools as a typical software development project.

In a [Docs-as-Code](https://www.writethedocs.org/guide/docs-as-code/) workflow, you'll use:

* Issue trackers
* Version control
* Plain Text markup
* Code reviews
* Automated tests

Docs-as-Code facilitates an environment where technical writers and software developers both feel ownership of the documentation.

At my current position, we do not use a Docs-as-Code workflow, and the technical writers are often quite remote from the development process. I've been building a prototype system to demonstrate at work, which has led me to experiment with several Docs-as-Code tools, version control systems, static site generators, publishing platforms, and Markdown variants.

I've worked with these tools recently in my quest:

### Issue Trackers

I've tried working with Notion, Redmine, and Jira.

**Redmine** is dreadful. Just avoid this at all costs.

**Notion** is super flexible. With some custom formulas and some creative views, you can make Notion into a fairly powerful project management system. I built a reasonably complex workflow in Notion. I wish it had more rules and field validation, but it was fairly capable. It's inexpensive if you are willing to write some formulas, or you can pay for templates and hire Notion consultants.

**Jira** is super powerful. After we adopted Jira at work, I migrated off Notion as fast as possible and built a Jira workflow. Primarily, I was looking for compatibility with the rest of the company. Up to this point, I had been using Notion while the rest of the company was on Redmine. After we started using Jira company-wide, the synergy was attractive enough to justify re-building the workflow in Jira, even if that required copying all the Notion work-in-process to new Jira issues. I'm cautiously optimistic that Jira can manage a large Docs-as-Code system. The instance I have access to doesn't currently have Git integration, which would be ideal.

### Version Control

The system works equally well with local `git`, a private GitLab repo inside your firewall, or a public GitHub repository.

### Plain Text Markup

This decision is usually driven by your output renderer, which is often a static site generator like Hugo, MkDocs, Jekyll, or Sphinx. This typically means you have some Markdown variant for your basic formatting, or in the case of Sphinx, you use reStructuredText. Then, you often have access to various theme-specific extensions: things like admonishment boxes, or lazy-loading graphics with alignment, or captions, and many other examples. 

All of these small decisions -- what renderer to use, what theme extensions to use -- dictate enough changes in your plain text that you are effectively locked-in to that environment. Even if we rule out reStructuredText and only focus on Markdown, each system uses different macros and parameter syntax. Hugo's shortcodes are very different than the python-ish style of MkDocs, even when the base Markdown flavor is the same.

I've re-coded parts of this website through several generations using most of the tools I've mentioned, and it was a significant amount of toil. I started early-on with MkDocs and the Material theme. It was full-featured and had a rich set of extensions. The only drawback was that it looked really *the same as every other doc site on the net*. So, I decided I'd see what else I could find and learn more. 

I moved to Hugo, and worked my way through several themes. I re-wrote a good portion of one theme and built my own dynamic random quote plug-in for it. There's a lot to like about Hugo. I think it's a solid contender for my employer, but I wanted to spend more time writing than working on the Hugo theme. So, I again looked around for a nice out-of-the-box experience. 

I tried a lot of them. And I didn't want to just give up and go back to MkDocs/Material... but after three months of nights and weekend playing with static site generators, here I am. It's actually a great system, once you enable a few navigation features. More about that later.

The point being: Before committing a large project to Docs-as-Code, you should roll out a very small demo site in more than one framework and compare the experience and features. I only had a small site, and it was work to move to Hugo and back. I had to reformat and re/write a lot of table code and image macros, and some other things. You want to be sure of your chosen framework before you commit a large project to it.

## Code Reviews and Automated Tests

Vale and GitHub Actions provide
