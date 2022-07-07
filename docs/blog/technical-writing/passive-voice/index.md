---
title: The Passive Voice was Used by Someone
revision_date: June 19, 2022
tags:
  - Technical Writing
#hide:
#  - navigation
#  - toc
#  - footer
---

![Featured](_media/pexels-chris-clark-5604850-1600x600.webp){ width=50% align=left loading=lazy }

Most technical writing guides suggest you "write in second-person" or "use active voice." I wrote a [style guide for Vultr](https://www.vultr.com/docs/vultr-docs-style-guide) with those instructions, and published [a Markdown toolkit](https://github.com/vultr/vultr-mdtk/blob/main/styles/Vultr/Passive.yml) that includes a Vale linting rule for active voice &mdash; which is great for anyone doing Docs-as-Code.  I've read and written a lot about active voice, and in my research, I haven't found many guides explaining when it's okay or even preferred to use passive voice. So, I thought it would be an excellent time to talk about a few exceptions to the active voice rule.

Here are times when you _should_ use the passive voice in technical writing.

## What are active and passive voice?

First, let's refresh on how to identify the voice of a sentence.

A **passive voice** sentence, such as "The server was rebooted by the administrator," usually follows this structure:

| Part of speech  |  Example  |
| --| -- |
| The thing receiving action | The server |
| A version of verb _to be_ | was |
| Past participle of a verb | rebooted |
| The thing doing the action (optional) | by the administrator. |

An **active voice** sentence moves the thing performing the action into the subject. In a simple present tense sentence, the structure looks like this:

| Part of speech  |  Example  |
| --| -- |
| The thing doing the action | The administrator |
| Present tense of a verb | rebooted |
| The thing receiving the action | the server. |

## Why is active voice preferred?

Active voice is usually shorter, more direct, and easier to understand. But, sometimes passive voice works better. Here are a few specific situations.

### To shift emphasis

If the thing receiving action is more important that what did it, you may want to move it into the subject of the sentence, which carries more weight. We care more about a city full of people than the volcano, so the sentence that mentions the city first is preferred.

**Pompeii was buried by a volcano.**

"A volcano buried Pompeii," is a weaker statement. It only makes sense to mention the volcano first if you are mentioning it by name, and also probably a volcanologist. 

Likewise, if you want to describe **which database** to purge, it makes sense to say, "The employee database is purged by the monthly cleanup script." However, if you need to explain **what purges** the database, stick to active voice, "The monthly cleanup script purges the employee database."

### When the actor is unknown

Sometimes you don't know who or what is doing the action and trying to force it into the sentence results in something awkward like, "An unknown process purges the employee database each month," which is just awful. Passive voice is often a better choice when you don't know what process is purging the employee database. 

"**The employee database is purged each month,**" is a straightforward statement, and perfectly fine.

### To avoid assigning blame or to obscure information

Software error messages are famous for their attempts to avoid blaming the user. You've probably seen messages like, "**A phone number wasn't entered**," when filling out a form. A website processing a payment would pefer not to use the more blunt, perhaps more honest response, "You didn't enter a phone number," which sounds a little harsh.

Passive voice is also a popular way to obscure data in an error message. If you want to avoid leaking information to attackers, a message like `The account was not found` is more secure than `SRV27 did not find ACCOUNT_ID in the CUSTOMER table.`

### When the actor is obvious

Sometimes the actor is obvious. If you say, "**The web page is reloaded after five minutes**," it's probably obvious that a web browser will reload the web page. It's straightforward. The active version, "The web browser reloads the web page after five minutes," is redundant.

### To state a general truth

**Most passenger cars are designed for paved roads.**

There's no need to shoehorn the history of car designers into that sentence. "Automobile designers and engineers design most passenger cars for paved roads," is a silly alternative. It's a general statement and leaving it as a passive statement is preferred.

## Other situations

These are not the only times you'll make a judgement call, they are just a few common situations I've noticed. When I encounter an awkward sentence while editing, I rephrase it both ways to see which is easier to understand.

## Tips for identifying passive voice

Learning how to distinguish between active and passive voice is the first step to using them effectively. 

### To be

One good tip is to search your article for forms of the verb _"to be"_, because those are integral to passive voice constructions. Look for **is**, **am**, **are**, **was**, **were**, **be**, **being**, and **been**. These are usually found in passive voice sentences, so review those and look for improvements.

!!! Tip "Tip for Docs-as-Code Fans"
    The Markdown Toolkit has [a nice passive-voice linting test](https://github.com/vultr/vultr-mdtk) that uses this search as a regular expression. It works in Visual Studio Code, and you can export the rule to any platform Vale Server supports, including Google Docs.

### ...by Smurfs

Another common pattern with passive voice sentences is the practice of omitting the prepositional phrase at the end. If you can add one, such as "…by Smurfs," and it makes sense, then you probably have a passive voice sentence.[^1] For example:

* The server has been rebooted. (…by Smurfs.)
* The meeting is being rescheduled. (…by Smurfs.)
* The transaction was canceled. (…by Smurfs.)

If you can complete a sentence this way, it's written in passive voice. And that's not a necessarily bad thing, as long as you know why it's written that way and it was done on purpose.

## Summary

As a rule, you should write technical articles in active voice unless you have a good reason. But, there are some good reasons, so pay attention to your choice of voice and your articles will be crisp and easy for the readers to understand.

[^1]: Or, you can use any plural noun of your choice. A lot of guides suggest "by zombies." I like Smurfs better, but you could use ferrets, rubber ducks, or even Minions if it makes you happy.
