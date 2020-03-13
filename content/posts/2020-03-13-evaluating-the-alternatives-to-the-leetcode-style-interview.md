---
template: post
title: Evaluating the alternatives to the LeetCode Style Interview
slug: leetcode-alternatives-compared
draft: false
date: 2020-03-10T22:25:07.743Z
description: >-
  There is no one-size-fits-all approach to interviewing, but at least we have
  some common criteria now. Let's look at some alternative approaches to
  interviewing and highlight the aspects in which they do well or address the
  problems caused by LC interviews.  Let's also determine where they still fall
  short, and why they aren't adopted by more companies. 
category: interviews
tags:
  - interviewing
---
In the [last blog post](https://www.naveed.dev/posts/senior-engineer-interviews-broken), I discussed my frustrations with the ubiquitous LeetCode interview, and why it was a poor litmus test for determining competency in senior engineers. Let's look at some alternatives.  

## Current alternative #1: Take-Home Assessments

On one hand, we have LeetCode. On the other, we have Take-Home Assessments. Previously, I used to think of these assessments as a superior solution, but after this last round of interviews, I've found it to have mixed results.

#### What they get right

* They allow the interviewee the flexibility to do the interview over a longer period of time, so the "time crunch" isn't a factor. Given the amount of time, a candidate can usually analyze the problem more deeply. Given a clearer understanding of the problem, they can build and present a higher quality solution, which is more analogous to their work output on the job.
* They are more pragmatic in nature, testing a coder's ability to demonstrate depth of knowledge in areas that are analogous to their everyday work (like design patterns, documentation, testing, architecture decisions) -- stuff that would be hard to communicate effectively in the span of an hour long interview.

  This is especially valuable for specific roles. For example, my friend was asked to build a program that would parse gigs of log messages and determine potential intrusion attempts -- a pretty solid test for a  Senior Security Engineer. Likewise, being asked to build a scraper for an e-commerce website is reasonable as a take-home project if you are applying for an engineering integration team. Take homes allow you to test for distinct skills that matter for that role. 

#### What they get wrong

* They are higher effort for the candidate. Because of the asynchronous nature of these projects, getting clarifications on ambiguous wording via email can take anywhere from a couple hours to a few days, throwing you off your groove if you're coding the assessment. Candidates are usually interviewing with a handful of companies at a time, and these take-homes take a disproportionate amount of time and effort when compared a quick LeetCode style interview. This is the real reason why this interview type isn't more widespread. Many candidates would simply prefer to skip and work with companies where the interview timeline is tighter to maximize their chances of success. This is especially true for Senior Engineers -- "why should I work off the clock if I'm not getting paid for it?"  
* They are also higher effort for the company. For the engineers reviewing these projects, you have to code review a candidates project alongside your other work, whereas with an interview, you have a concrete window in which to handle the interviewing task. And, if you work at a company where you might have a few hundred candidates, this process of individual code review does not scale -- you can't possibly review them all as well as you'd like. 
* Take Homes can balloon in scope. Some companies give lengthy projects as a way to judge efficacy, and there isn't an agreed upon standard on what a candidate should and shouldn't accept. The ambiguity makes it difficult for the candidate to know how much effort to invest, especially if they are interviewing with a few companies at once. Whats the time frame? 3 hours or 6? Should I have a full test suite as well? Not having clear expectations can muddle the results, making it difficult for candidates to choose an appropriate amount of time on the project, or commit to it altogether.
* It's hard to gauge a candidate's problem solving speed, or whether they did the assignment independently. A really committed candidate wouldn't hesitate to ask their friends for a "spare set of eyes", or spend all night tinkering with the project to make sure it's perfect. While it is is awesome that a candidate has the  drive to succeed at all costs -- they might be falsely advertising their skills when you look at the project at face value. 

#### Conclusions

The benefits of a take home are undeniable: 

* they provide a much more realistic proxy for everyday development, 
* the difficulty of the assessment scales better with the role, 
* they don't cram too many things into one interview
*  they are amenable to more classes of software engineers like Bootcamp Graduates.

That being said, they're too expensive in terms of time and effort. Lots of candidates don't like them, and companies can't scale that kind of interview once you have over 200 engineers because of the outsized effort in reviewing all the projects. (I totally made that number up, but you get the point).

In my own experience, I found myself actually wanting to do a LeetCode interview after getting rejected by a company after doing their take home. For me, doing that one programming project took the span of scheduling and completing about 3 LC style phone screens. It's just not a good use of my time when I'm hunting for jobs. Would I do one if I had to? Absolutely. But would I jump for the opportunity?

<iframe src="https://giphy.com/embed/lokUlZaZgMAQlI05pu" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/chef-key-and-peele-keyandpeele-lokUlZaZgMAQlI05pu">via GIPHY</a></p>

However, for some people, I know this is still a great way to interview, and for the companies offering it, I applaud you for not cargo-culting. If this is your jam, I would highly recommend taking a look at [the list of companies that don't do whiteboard interviews.](https://github.com/poteto/hiring-without-whiteboards)

## Alternative #2: Behavioral & System Design Interviews only

