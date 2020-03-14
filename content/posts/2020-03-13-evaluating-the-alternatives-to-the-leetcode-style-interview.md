---
template: post
title: Evaluating the alternatives to the LeetCode Style Interview
slug: leetcode-alternatives-compared
draft: false
date: 2020-03-10T22:25:07.743Z
description: >-
  There is no one-size-fits-all approach to interviewing, but at least we have
  some common criteria now. Let's look at some alternative approaches to
  interviewing and highlight the aspects in which they address the problems
  caused by LC interviews.  Let's also determine where they still fall short,
  and why they aren't adopted by more companies. 
category: interviews
tags:
  - interviewing
---
*Reading Time: 6 Minutes*

*This is the first post of a 3 part blog series focused around improving our interviewing practices as a development community. Check out the other parts, too:*

* [Part 1: Interviews for Senior Software Engineers are F*cking Broken](https://www.naveed.dev/posts/senior-engineer-interviews-broken)
* [Part 3: A sane and fair process for conducing Senior Software Engineering Interviews](https://www.naveed.dev/posts/alternative-senior-engineer-interview-process)

- - - 

In the [last blog post](https://www.naveed.dev/posts/senior-engineer-interviews-broken), I discussed my frustrations with the ubiquitous LeetCode interview, and why it was a poor litmus test for determining competency in senior engineers. Before we discuss alternatives, let's recap what skills our interviews should be testing for. 

## A refresher: what should the Technical Interview evaluate a candidate on?

* **Problem Solving**: Given a problem, can the candidate think on their feet and come up with a solution? Are their proposed solutions reasonable, and can they leverage their experiences effectively? Are they coachable, and can they work well with feedback?
* **Raw Technical Chops**: Can this person actually code at a reasonable speed? Are they familiar with the language’s standard API? Are they familiar with Data Structures and Algorithms?
* **Design Patterns / Coding “Style”:**Does this person write clean code? Do they use descriptive variable names, and appropriately sized functions? Do they display other hallmarks of maintainable software?
* **Communication / Behavioral**: Is this person effective at explaining what they are thinking about, and describing a solution that can be understood by others?
* **Attitude / Demeanor**: Is this person a brilliant jerk? Are they stand-offish? Cocky? Are they independent? Are they low-energy? Is this someone I can see myself working with? Does their values align with our company credos?

OK, so now that we've gotten that taken care of, let's look at some alternatives in practice today.

## Alternative #1: Take-Home Assessments

On one hand, we have LeetCode. On the other, we have Take-Home Assessments. Previously, I used to think of these assessments as a superior solution, but after this last round of interviews, I've found it to have mixed results.

#### What they get right

* They allow the interviewee the flexibility to do the interview over a longer period of time, so the "time crunch" isn't a factor. Given the amount of time, a candidate can usually analyze the problem more deeply. With a clearer understanding of the problem, they can build and present a higher quality solution, which is more representative to their work output on the job.
* They are more pragmatic in nature, testing a coder's ability to demonstrate depth of knowledge in areas that are relevant to their everyday work (like design patterns, documentation, testing, architecture decisions) -- stuff that would be hard to communicate effectively in the span of an hour long interview.

  This is especially valuable for specific roles. For example, being asked to build a program to parse log messages and determine potential intrusion attempts is a pretty solid test for a Security Engineer. Likewise, building a scraper for an e-commerce website is reasonable as a take-home if you are applying for an engineering integration team. For specialized roles, take-homes allow you to test for distinct skills that matter for that role. 

#### What they get wrong

* They are higher effort for the candidate. Because of the asynchronous nature of these projects, getting clarifications on ambiguous wording via email can take anywhere from a couple hours to a few days, throwing you off your groove if you're coding the assessment. Candidates are usually interviewing with a handful of companies at a time, and these take-homes take a disproportionate amount of time and effort when compared a quick LeetCode style interview. This is the real reason why this interview type isn't more widespread. Many candidates would simply prefer to skip and work with companies where the interview timeline is tighter to maximize their chances of success. It's easier to rationalize the sunk cost of losing an hour than a few nights or a weekend. This is especially true for Senior Engineers -- "why should I work off the clock if I'm not getting paid for it?"  
* They are also higher effort for the company. For the engineers reviewing these projects, you have to code review a candidates project alongside your other work, whereas with an interview, you have a concrete window in which to handle the interviewing task. And, if you work at a company where you might have a few hundred candidates, this process of individual code review does not scale -- you can't possibly review them all as well as you'd like. 
* Take-homes can balloon in scope. Some companies give lengthy projects as a way to judge efficacy, and there isn't an agreed upon standard on what a candidate should and shouldn't accept. The ambiguity makes it difficult for the candidate to know how much effort to invest, especially if they are interviewing with a few companies at once. Whats the time frame -- 3 hours or 6? Should I write a full test suite as well? Not having clear expectations can muddle the results, making it difficult for candidates to choose an appropriate amount of time on the project, or commit to doing it altogether.
* It's hard to gauge a candidate's problem solving speed, or whether they did the assignment independently. A really committed candidate wouldn't hesitate to ask their friends for a "spare set of eyes", or spend all night tinkering with the project to make sure it's perfect. While it is is awesome that a candidate has the  drive to succeed at all costs -- they might be falsely advertising their skills when you look at the project at face value. 

#### Conclusions

The benefits of a take home are undeniable: 

* they provide a much more realistic proxy for everyday development
* the difficulty of the assessment scales better with the role
* they don't cram too many things into one interview
* they are amenable to more classes of software engineers

That being said, they're too expensive in terms of time and effort. Lots of candidates don't like them, and companies can't scale that kind of interview once you have over 200 engineers because of the out-sized effort in reviewing all the projects. (I totally made that number up, but you get the point).

In my own experience, I found myself reluctantly preferring to do a LeetCode interview after getting rejected by a company that gave me a take-home assessment. For me, doing that one programming project took the span of scheduling and completing about 3 LC style phone screens -- it just wasn't a good use of my time when I was hunting for jobs. Would I do one if I had to? Absolutely. But would I jump for the opportunity?

<iframe src="https://giphy.com/embed/lokUlZaZgMAQlI05pu" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/chef-key-and-peele-keyandpeele-lokUlZaZgMAQlI05pu"></a></p>

However, for some people, I know this is still a great way to interview, and for the companies offering it, I applaud you for not [cargo-culting](https://en.wikipedia.org/wiki/Cargo_cult_programming#Cargo_cult_software_engineering).

## Alternative #2: Behavioral & System Design Interviews ONLY

A few of the companies I had interviewed with (small startups) relied on behavioral and system design interviews as the sole determinant of a candidate's skill. Let's discuss the pros and cons. 

#### What they get right

* They require the least amount of effort for both parties. You only need a whiteboard and a conference room. Many system design questions are available online, and it's relatively easy to adapt a problem the company has solved into a system design question.
* They fit nicely into the 1 hour time-frame, which makes them cheap to scale.
* The free-form nature makes it possible for the interviewer to probe and explore various topics of interest. Interviewers can focus on getting signal on the behavioral aspects and technical communication skills.
* System Design questions are a good test for higher level problem solving. Gluing together systems, understanding the relationships between different software components -- this is directly analogous to the work Senior Engineers do on a daily basis

#### What they get wrong

* It doesn't test whether you can actually code. You could be great at discussing high level architecture and terrible at actually building things; these interviews by themselves can't screen out the latter
* For an interviewer, it's hard to filter out bullshit. The interviewers are susceptible to [getting overwhelmed](https://rationalwiki.org/wiki/Gish_Gallop) by a slick-talking candidate. 
* the lack of defined criteria for this interview style makes it more subjective than the LeetCode style interview. When there are multiple interviewers, one interviewer may focus on specific topic or level of granularity they care about, that the other interviewer does not value as much. This interview is difficult to coordinate effectively with other team members. 
* Most of the practice system design questions available online only focus on web based architectures, which present a real challenge to senior engineers that focus on a particular part of the stack, like front-end or mobile engineers. When I was practicing these questions on [Pramp](https://www.pramp.com/), I felt guilty for asking my peer to "design a scalable web architecture for Uber" when they had been an android engineer for the past 5 years. 

#### Conclusions

Both the Behavioral Interview and the System Design have rightfully earned their place in the roster of interview assessments for Senior Engineers. However, a company who only employs these 2 kinds of interviews does not insure themselves adequately against people who lack the raw technical coding chops to be effective at the Senior Engineer level. 

The best thing about this approach is that it is quick, easy, and scalable. The worst thing is that you still can't determine whether a candidate is actually as good as they say they are -- which is why we need to pair them with a coding assessment to see if a candidate can walk the walk after talking the talk. 

## Alternative #3: The Pragmatic Practical

This is a pretty new kind of assessment, and it was offered by a few companies, usually via a coding platform like [Codility](https://www.codility.com/) or [CoderPad](https://coderpad.io/). This interview style was very straightforward -- 4 small, pragmatic tests which would test a specific subject, technology, or skill. One example was a "refactoring test", where you were given a function that was 80 lines long and asked to refactor it and clean up the logic. Another test might be how to build a bare-bones API server to handle a single web request, stuff like that.  

#### What they get right

* It is a realistic proxy for everyday development, and tests whether you can actually code
* The assessment leverages the actual experience engineers may have accrued in their career
* They are not cramming multiple types of interviews into 1 session
* They fit into the hour long time-frame taken by LeetCode, System Design, and Behavioral Interviews
* They have defined and concrete deliverables, unlike the System Design

#### What they get wrong

* The bite-sized length of each assessment would make it hard to differentiate a mid-level engineer from a senior-level engineer
* The assessments were often testing the fluency of a language or tool more than the problem solving skills
* The assessment heavily favored engineering breadth over depth

#### Conclusions

This assessment is a big step in the right direction. The "Pragmatic Practical" combines the speed of a LeetCode interviews with the pragmatism of a take-home. We've successfully crossed over into territory where we can evaluate a candidate based on their technical chops, while allowing them to leverage their  prior experience in a time efficient manner!  Woo-hoo!

But... (there's always a but), there is something left to be desired. It feels to me that I wasn't able to demonstrate *how much* of a given topic I knew. Once you could demonstrate that you could navigate the API and understand the concepts behind a technology, the assessment was trivial. Being constrained to the 1 hour time-box meant simplifying problems down to a point that feels reductive. While definitely harder to fake than the system design or behavioral assessment, it doesn't seem like an effective test to separate a good mid-level engineer from a senior one. We need some criteria to be able to distinguish engineers of different ranks, and that is missing from this kind of assessment.

All in all though, I would endorse this style of test over a LeetCode. You could pair this style of assessment with System Design and Behavioral Tests, and get a pretty good read on a candidate. Is this the best style of interviewing? Actually, I found another exercise that I think is even better. But before we dive in, let's define what makes a good software assessment. 

## What is the criteria for a sane, but fair interview process for Senior Software Engineers?

1. It needs to be short-medium length; not too short or too long.
2. It needs to be comprehensive, with sufficient technical complexity to allow a candidate to demonstrate competence across multiple areas at an appropriate depth. This is necessary to distinguish them from mid-level engineers
3. It needs to scale in terms of cost / time / effort. It respects the candidate's time, and can work for engineering teams of 10 or 10,000. 
4. It should be a realistic proxy for everyday development, and is designed so a candidate can leverage prior experience in demonstrating tech skills

The solutions above, while close, don't fully satisfy my criteria for a sane and rigorous interview process -- although if I saw more of Alternative 1 or 3, I'd be happy. 

In my experience, there was a certain class of interview that met all the criteria above and hasn't been discussed yet. So, without further ado, check out a [sane and fair process for conducting senior software engineering interviews](https://www.naveed.dev/posts/alternative-senior-engineer-interview-process). 

**NOTE:** As I alluded to earlier, there is no one-size-fits all. If the current non-LC based assessments are your jam, then more power to you! I would recommend taking a look at [Hiring Without Whiteboards](https://github.com/poteto/hiring-without-whiteboards) so you can find your next company! <3

- - -

Thanks for reading! If you have any suggestions, feel free to tweet me: [@nudgemybody](https://twitter.com/nudgemybody)