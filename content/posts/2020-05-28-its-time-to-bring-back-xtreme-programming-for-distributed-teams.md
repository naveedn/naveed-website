---
template: post
title: >-
  What's old is new again: why Extreme Programming / mobbing works well for
  remote teams
slug: consider-xp-for-distributed-teams
draft: true
date: 2020-05-28T05:58:41.206Z
description: >-
  Since the start of the pandemic, our social patterns have shifted almost
  overnight. Video calls have become the norm for both social and work
  engagements. Adapting to a long-term remote work lifestyle is challenging, to
  say the least. 


  However, the process of experimentation has allowed me to discover practices
  that have increased my work productivity significantly. After reflecting on
  these new strategies, I realized many of these ideas have already been
  introduced to the programming community for decades, but for a variety of
  reasons, they've been written off as irrelevant or impractical. 


  But now, the confluence of factors that led to our massive societal shift have
  breathed new life into these software development approaches -- allowing them
  to shine in ways that seem unintuitive at first glance.
category: productivity
tags:
  - remote
  - productivity
  - remote work
---
Since the start of the pandemic, our social patterns have shifted almost overnight. Video calls have become the norm for both social and work engagements. Adapting to a long-term remote work lifestyle is challenging, to say the least. 

However, the process of experimentation has allowed me to discover practices that have increased my work productivity significantly. After reflecting on these new strategies, I realized many of these ideas have already been introduced to the programming community for decades -- but for a variety of reasons, they've been written off as irrelevant or impractical. But now, the confluence of factors that have led to this massive societal shift have allowed software development approaches like XP and mob programming to really shine in ways that are unintuitive at first glance. 

## First off, what is XP (Extreme Programming) and where did it come from?

Extreme Programming is a software development style that takes the ideas from the Agile Development process and drives them to their "logical extremes", which culminates in a set of practices and philosophies that we should adopt to be better software engineers. I'll add a link to the 12 practices at the bottom of the article, but I find that [this blog post from 2004](https://web.archive.org/web/20120101190943/http://www.satyakomatineni.com/akc/display?url=DisplayNoteIMPURL&reportId=862&ownerUserId=satya) captures the ethos of the movement succinctly. 

### A quick history lesson

We're gonna keep this brief. Here's a 30 second crash course on the history of XP:

* In the land before time, software teams used a waterfall approach to software development. Most software projects were failures.
* In the early 2000's, a new generation of software engineers [met at a famous ski resort](https://agilemanifesto.org/history.html) and came up with a new paradigm for how we should do software development. That birthed the "agile development" workflow that's ubiquitous in software engineering these days.
* The original agile movement became fragmented the more popular it grew. Over time, the Agile movement was co-opted by business folks and process-oriented project managers.

  * Rigid formalizations of the practices and process bloat infiltrated development teams, big and small. 
  * People began forking off and experimenting with alternative styles of software development, which is where XP, [Mob Programming](https://en.wikipedia.org/wiki/Mob_programming#:~:text=Mob%20programming%20(informally%20mobbing)%20is,code%20at%20the%20same%20time.), are derived from.
  * Some methodologies, like Kanban, enjoyed commercial success in niche development teams. Kanban became the preferred strategy in DevOps or client-facing support teams, for example, because it allowed teams to allocate effort for unpredictable events that necessitate high urgency fixes.

XP and Mob Programming were decidedly less popular. These frameworks were in a bit of a limbo -- some of the top practitioners in our field were using XP, such as Martin Fowler, Robert Martin and Kent Beck. But it was considered too unapproachable for the masses, too intense; some practices, like pair programming seem absolutely asinine from a business perspective. Indeed, if you visit the wikipedia page for Extreme Programming, they have a BIG section dedicated to "[Controversial Aspects](https://en.wikipedia.org/wiki/Extreme_programming#Controversial_aspects)" -- not a ringing bell of endorsement for most people. 

Rather than go through the exercise of debating the merits of each principle in detail (which sounds about as boring to read as it is to write), let's discuss why some of the biggest critiques against this methodology no longer hold water.

## Arguments critiquing XP that are not valid anymore

#### Pair Programming is costly and a waste of valuable resources because it limits parallelism

In the past 3 months, I've spent more time pair-programming than I did in my entire career beforehand. Pair-programming is the best substitute we have to co-locating in our current distributed environment. I use it for everything, and do it often.

* I got ramped up very quickly on my team's architecture and codebases. Pivotal Labs, a boutique software consultancy that practices XP, has written a pretty [good article](https://www.pivotaltracker.com/blog/how-pair-programming-and-mob-programming-help-quickly-onboard-new-software-engineers) about this.
* I've spent hours getting unblocked and helping my teammates in configuring their local environment / IDE for various parts of the platform. (We're a polyglot team with front-end, back-end, database, and ETL components)
* I've been able to triage and isolate bugs much faster in pair-debugging sessions, preventing myself from "spinning my wheels" if I've been stuck on a problem for an hour or more. 
* As a team, we've been able to gather consensus and coordinate much more effectively because a discussion about the spec can highlight different assumptions we have about the same requirements, leading to clarifications and shared understanding about what we're trying to do

That's not to say I agree with pair-programming **all the time.** I need my own time to chew on problems, to try out solutions, and organize my thoughts to make sure I'm not wasting the other person's time when we meet. I think this is where most people get it wrong; they think that have to be chained to the hip with their teammates and always lock-step with them, when that's not really how it works in practice. 

It's not some formal process where we spend an uncomfortable amount of time in our teammates personal space -- instead, it's more like a game of football, where we huddle between plays to strategize before we execute some chunk of work.

The need for discrete chunks of IC time is very real in the workplace. It's been talked about at great length in the book "Deep Work" By Cal Newport, and many companies have [independently verified](https://www.google.com/search?q=no+meeting+day+policy) that having distraction-free blocks for developers has yielded impressive productivity gains (duh!). 

But this is another area where Remote teams really benefit. For most non-parents, the home workspace is much more distraction-free than the office workplace. There isn't as much of an interest or need for water cooler chit-chat, and external distractions in the office such as a birthday or firing aren't nearly as disruptive. We don't need to pretend to be busy, because we're being  more carefully scrutinized on our output than our effort.

#### Continuous Design Approach is inefficient, impossible to measure, prone to getting off track, and "enormously expensive" to customers

#### Requires too much change to adopt, and can only work with Senior Engineers

#### XP's practices are interdependent but few practical organizations are willing/able to adopt all the practices; therefore the entire process fails.

Ok, so now we realize that maybe all the reasons why we hated on these frameworks are wrong. But why should we switch? Why *now*?

## Conclusion

In the end, I'm not saying that we need to follow each of these principles dogmatically or that Agile "is over". But, more than anything, I think teams that are struggling to adjust to a geographically distributed workplace environment should experiment with some of the ideas I highlighted above, and see if it works for them. The nature of work is evolving as we speak; we should evolve our relationship with it as well.

Further Reading:

* Coders at Work: **[Interview with Jamie Zawinski](https://github.com/ndina/acm/blob/master/coders-at-work.pdf)**
* [An Introduction to XP](https://www.agilealliance.org/glossary/xp/#q=~(infinite~false~filters~(postType~(~'post~'aa_book~'aa_event_session~'aa_experience_report~'aa_glossary~'aa_research_paper~'aa_video)~tags~(~'xp))~searchTerm~'~sort~false~sortDirection~'asc~page~1))
* [A recent take on mob programming](https://www.remotemobprogramming.org) (2018)
* [Industrial XP: Making XP Work in Large Organizations](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.694.2506&rep=rep1&type=pdf#:~:text=Industrial%20XP%20(IXP)%20is%20a,often%20face%20when%20implementing%20XP.)
* [When Is Xp Not Appropriate](http://wiki.c2.com/?WhenIsXpNotAppropriate) 
* [Wikipedia: 12 Practices of Extreme Programming](https://en.wikipedia.org/wiki/Extreme_programming_practices)