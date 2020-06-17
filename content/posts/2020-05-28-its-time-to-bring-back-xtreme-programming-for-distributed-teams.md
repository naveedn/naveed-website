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

Extreme Programming is a software development style that takes the ideas from the Agile Development process and drives them to their "logical extremes", which culminates in a set of practices and philosophies that we should adopt to be better software engineers. I'll add a link to the 12 practices at the bottom of the article, but I find that [this blog post from 2004](https://web.archive.org/web/20120101190943/http://www.satyakomatineni.com/akc/display?url=DisplayNoteIMPURL&reportId=862&ownerUserId=satya) captures the ethos of the movement pretty succinctly. 

### A quick history lesson

We're gonna keep this brief. Here's a 30 second crash course on the history of XP:

* In the land before time, software teams used a waterfall approach to software development. Most software projects were failures.
* In the early 2000's, a new generation of software engineers [met at a famous ski resort](https://agilemanifesto.org/history.html) and came up with a new paradigm for how we should do software development. That birthed the "agile development" workflow that's ubiquitous in software engineering these days.
* The original agile movement became fragmented the more popular it grew. Over time, the Agile movement was co-opted by business folks and process-oriented project managers.

  * Rigid formalizations of the practices and process bloat infiltrated development teams, big and small. 
  * People began forking off and experimenting with alternative styles of software development, which is where XP, [Mob Programming](https://en.wikipedia.org/wiki/Mob_programming#:~:text=Mob%20programming%20(informally%20mobbing)%20is,code%20at%20the%20same%20time.), and Kanban come from.
  * Some methodologies, like Kanban, enjoyed commercial success in niche development teams. Kanban became the preferred strategy in DevOps or client-facing support teams, for example, because it allowed teams to allocate effort for unpredictable events that necessitate high urgency fixes.

XP and Mob Programming were decidedly less popular. These frameworks were in a bit of a limbo -- some of the top practitioners in our field were using XP, such as Martin Fowler, Robert Martin and Kent Beck. But it was considered too unapproachable for the masses, too intense; some practices, like  mob programming seem absolutely asinine from a business perspective. Indeed, if you visit the wikipedia page for Extreme Programming, they have a BIG section dedicated to "[Controversial Aspects](https://en.wikipedia.org/wiki/Extreme_programming#Controversial_aspects)" -- not a ringing bell of endorsement for most people. 

Rather than go through the exercise of debating the merits of each principle in detail (which sounds about as boring to read as it is to write), let's discuss why some of the biggest critiques against this methodology no longer hold water.

## Arguments critiquing XP that are not valid anymore

#### XP's practices are interdependent but few practical organizations are willing/able to adopt all the practices; therefore the entire process fails.

#### Pair Programming is costly and a waste of valuable resources because it limits parallelism

#### Continuous Design Approach is inefficient, impossible to measure, prone to getting off track, and "enormously expensive" to customers

#### Requires too much change to adopt, and can only work with Senior Engineers

Ok, so now we realize that maybe all the reasons why we hated on these frameworks are wrong. But why should we switch? Why *now*?

## Benefits to XP that have clear advantages in a remote environment

## Conclusion

In the end, I'm not saying that we need to follow each of these principles dogmatically or that Agile "is over". But, more than anything, I think teams that are struggling to adjust to a geographically distributed workplace environment should experiment with some of the ideas I highlighted above, and see if it works for them. The nature of work is evolving as we speak; we should evolve our relationship with it as well.





Further Reading:

* Coders at Work: **[Interview with Jamie Zawinski](https://github.com/ndina/acm/blob/master/coders-at-work.pdf)**
* [An Introduction to XP](https://www.agilealliance.org/glossary/xp/#q=~(infinite~false~filters~(postType~(~'post~'aa_book~'aa_event_session~'aa_experience_report~'aa_glossary~'aa_research_paper~'aa_video)~tags~(~'xp))~searchTerm~'~sort~false~sortDirection~'asc~page~1))
*  [A recent take on mob programming](https://www.remotemobprogramming.org) (2018)
* [Industrial XP: Making XP Work in Large Organizations](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.694.2506&rep=rep1&type=pdf#:~:text=Industrial%20XP%20(IXP)%20is%20a,often%20face%20when%20implementing%20XP.)
* [When Is Xp Not Appropriate](http://wiki.c2.com/?WhenIsXpNotAppropriate) 
* [Wikipedia: 12 Practices of Extreme Programming](https://en.wikipedia.org/wiki/Extreme_programming_practices)