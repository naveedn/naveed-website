---
template: post
title: >-
  What's old is new again: why Extreme Programming works really well for remote
  teams
slug: consider-xp-for-distributed-teams
draft: false
date: 2020-05-28T05:58:41.206Z
description: >-
  Adapting to a long-term remote work lifestyle in the era of COVID is
  challenging, to say the least. 


  But, the process of experimentation has allowed me to develop effective
  strategies for remote work. After reflecting on these new strategies, I
  realized many of the core ideas have already been introduced to the
  programming community for decades, but for a variety of reasons, they've been
  written off as irrelevant or impractical, even though they make more sense now
  than ever. Let's dig in.
category: productivity
tags:
  - remote
  - productivity
  - remote work
---
Since the start of the pandemic, our social patterns have shifted almost overnight. Video calls have become the norm for both social and work engagements. Adapting to a long-term remote work lifestyle is challenging, to say the least. 

However, the process of experimentation has allowed me to discover practices that have increased my work productivity significantly. After reflecting on the strategies, I realized many of these ideas have already been introduced to the programming community for decades -- but for a variety of reasons, they've been written off as irrelevant or impractical.

Now, the factors that have led to our on-going, massive societal shift have incidentally **also** allowed development approaches like XP and mob programming to shine in ways that are unintuitive at first glance. 

## First off, what is XP (Extreme Programming) and where did it come from?

Extreme Programming is a software development style that takes the ideas from the Agile Development process and drives them to their "logical extremes", which culminates in a set of practices and philosophies that we should adopt to be better software engineers. I'll add a link to the 12 practices at the bottom of the article, but I find that this [comment on a web forum from 2004](https://web.archive.org/web/20120101190943/http://www.satyakomatineni.com/akc/display?url=DisplayNoteIMPURL&reportId=862&ownerUserId=satya) captures the ethos of the movement succinctly.

### A quick history lesson

We're gonna keep this brief. Here's a 30 second crash course on the history of XP:

* In the land before time, software teams used a waterfall approach to software development. Most software projects were failures. (See: [The Mythical Man-Month](https://amzn.to/30QHn8F))
* In 1999, esteemed programmer Kent Beck released a book called [Extreme Programming Explained](https://amzn.to/2YLNE2S), wherein he outlines a radically new and different approach to software development.
* In the early 2000's, the industry's most regarded engineers (including Beck) [met at a famous ski resort](https://agilemanifesto.org/history.html) and distilled the ideas of XP into a new paradigm for how organizations should do software development. That paradigm is known as the Agile Software Development methodology that's ubiquitous in software engineering these days.
* The Agile movement became fragmented the more popular it grew. Over time, the Agile movement was co-opted by business folks and process-oriented project managers.

  * Rigid formalizations of the practices and process bloat infiltrated development teams, big and small. 
  * People began forking off and experimenting with alternative styles of software development, which is where [Mob Programming](https://en.wikipedia.org/wiki/Mob_programming#:~:text=Mob%20programming%20(informally%20mobbing)%20is,code%20at%20the%20same%20time.) is derived from.
  * Some methodologies, like Kanban, enjoyed commercial success in niche development teams. Kanban became the preferred strategy in DevOps or client-facing support teams, for example, because it allowed teams to allocate effort for unpredictable events that necessitate high urgency fixes.

XP and Mob Programming were decidedly less popular. These frameworks were in a bit of a limbo -- some of the top practitioners in our field were using XP, such as Martin Fowler and Robert C. Martin (Uncle Bob). In the end, XP was considered too unapproachable for the masses, too intense. Some practices, like pair programming, seem absolutely asinine from a business perspective. Indeed, if you visit the wikipedia page for Extreme Programming, they have a lengthy section dedicated to "[Controversial Aspects](https://en.wikipedia.org/wiki/Extreme_programming#Controversial_aspects)" -- not a ringing bell of endorsement if you ask me. 

Rather than describing each principle in detail and debating its merits (which sounds as boring to read as it is to write), let's discuss why some of the biggest critiques against this methodology no longer hold water.

#### Argument: Pair Programming is costly and a waste of valuable resources because it limits parallelism

In the past 3 months, I've spent more time pair-programming than I did in my entire career beforehand. Pair-programming is the best substitute we have to co-locating in our current distributed environment. I use it for everything, and do it often.

* I got ramped up very quickly on my team's architecture and codebases. Pivotal Labs, a boutique software consultancy that practices XP, has written a pretty [good article](https://www.pivotaltracker.com/blog/how-pair-programming-and-mob-programming-help-quickly-onboard-new-software-engineers) about how XP is great for onboarding new engineers.
* I've spent hours getting unblocked and helping my teammates configure their local environment / IDE. (We're a polyglot team with front-end, back-end, database, and ETL components)
* I've been able to triage and isolate bugs much faster in pair-debugging sessions, preventing myself from "spinning my wheels" if I've been stuck on a problem for an hour or more. 
* As a team, we've been able to gather consensus and coordinate much more effectively because a discussion about the spec can highlight different assumptions we have about the same requirements, leading to clarifications and shared understanding about what we're trying to do

That's not to say I agree with pair-programming **all the time.** I need my own time to chew on problems, to try out solutions, and organize my thoughts to make sure I'm not wasting the other person's time when we meet. I think this is where most people get it wrong; they think that have to be chained to the hip with their teammates and always operate lock-step with them, when that's not really how it works in practice. 

It's not a formal process where we spend an uncomfortable amount of time in our teammate's personal space -- instead, it's more like a game of football, where we huddle between plays to strategize before we execute some chunk of work. A visceral example of this is in the book: "[Coders at Work: Reflections on the Craft of Programming](https://amzn.to/2ABX7SB)". In Chapter 2, Peter Seibel interviews [Jamie Zawinkski](https://www.jwz.org/about.html), one of the early engineers of Netscape. I'll post a part of the interview that stands out:

> *... \[discussion about building netscape 1.0] ...*
>
> **Seibel**: At some point you also worked on the mail reader, right?
>
> **Zawinkski**: In 2.0 Marc comes into my cubicle and says, "We need a mail reader." And I'm like, "OK, that sounds cool. I've worked on mail readers before." I was living in Berkeley and basically I didn't come into the office for a couple weeks. I was spending the whole time sitting in cafes doodling, trying to figure out what I wanted in a mail reader. Making lists, crossing it off, trying to decide how long it would take me. What should the UI look like?
>
> Then I cam back and started coding. And then Marc comes in again and says, "Oh, so we hired this other guy who's done mail stuff before. You guys should work together." It's this guy Terry Weissman, who was just fantastic -- we worked together so well. And it was a completely different dynamic than it had been in the early days with the rest of the browser team. 
>
> We didn't yell at each other at all. And the way we divided up labor, I can't imagine how it possibly worked or could ever work for anyone. I had the basic design done and I'd started doing a little coding and every day or every couple of days we'd look at the list of features and I'd go, "Uhhh, maybe I'll work on that," and he'd go, "OK, I'll work on that," and then we'd go away.
>
> Check-ins would happen and then we'd come back and he'd say, "Alright I'm done with that, what are you doing?" "Uh, I'm working on this." "OK, well, I'll start on that then." And we just sort of divided up the pieces. It worked out really well.
>
> We had disagreements -- I thought we had to toss filtering into folders because we just didn't have time to do it right. And he was like, "No, no, I really think we ought to do that." And I was like, "We don't have time!" So he wrote it that night.
>
> The other thing was, Terry and I rarely saw each other because he lived in Santa Cruz and I lived in Berkeley. We were about the same distance to work in opposite directions and because the two of us were the only two who ever needed to communicate, we were just like, "I won't make you come in if you don't make me come in." "Deal!"
>
> **Seibel**: Did you guys email a lot?
>
> **Zawinski**: Yea, constant email. This was before instant messaging -- these days it probably all would have been IM because we were sending one-liner emails constantly. And we talked on the phone.
>
> \--

As an aside: this is a [fantastic book](http://www.codersatwork.com/), and I recommend anyone read it if they're looking for computer science lore that isn't a textbook or manual.

As the interview may have unintentionally highlighted, having discrete chunks of coder time was a key component in the success of their collaboration. The idea been talked about ad nauseum in the book "[Deep Work](https://amzn.to/2zKQzR6)" by Cal Newport, and many companies have [independently verified](https://www.google.com/search?q=no+meeting+day+policy) that having distraction-free blocks for developers has yielded impressive productivity gains. (duh!)

This is another area where remote teams really benefit. For most non-parents, the home workspace is  more distraction-free than the office workplace. There isn't as much of an interest or need for water cooler chit-chat, and external distractions in the office such as a birthday or firing aren't nearly as disruptive. We don't need to pretend to be busy, because we're being  more carefully scrutinized on our output than our effort.

#### Continuous Design Approach is inefficient, impossible to measure, prone to getting off track, and "enormously expensive" to customers

Ok, most of these criticisms came from Matt Stephens and Doug Rosenberg, who co-authored a book called "[Extreme Programming Refactored: The Case against XP](https://amzn.to/30SIyVg)". And pretty much on all counts here, they're totally f*cking wrong.

I don't want to bash these guys too hard -- i mean, they wrote this in 2004, and I have the benefit of hindsight that they certainly did not have. But, in the 16 years since their book was released, the software engineering community has collectively agreed that a Continuous Design Approach (aka Continuous Innovation) is an ideology that not only works, but in fact heavily influenced the success of B2C startups in the generation after the dot-com bust. 

Eric Reis wrote the seminal book [the Lean Startup](https://amzn.to/2AAS6JZ), extolling the virtues continuous innovation while making the argument that it saves money in the long-run because you don't end up "building the wrong thing".

VC investor Peter Thiel gave further praise of Continuous Innovation and a fail-fast approach in his book [Zero to One](https://amzn.to/30P8b9k), while Paul Graham, co-founder of the Y Combinator startup accelerator, penned the famous essay "[Do things that don't scale](http://paulgraham.com/ds.html)". You can see it in the ethos of Facebook's old company motto: "[Move fast and break things](https://www.businessinsider.com/mark-zuckerberg-innovation-2009-10?r=US&IR=T)".

It's not just VCs and founders talking about it. Edward Lau, in his book [the Effective Engineer](https://amzn.to/2UWDbke), discusses tight-feedback loops and continuous delivery as the flywheel that powers the knowledge-discovery engine, which enable developers to iterate quickly and create leverage on their projects. 

And finally, Google Ventures has [their own process for applying a Continuous Design Approach](https://www.gv.com/sprint/) for all of their sprints, which struck a chord in the HCI / UX space. GV's design sprint bears striking resemblance to the company IDEO, which had their own [ABC Nightline special in 1999 about re-designing the shopping cart](https://www.youtube.com/watch?v=M66ZU2PCIcM&vl=en-US) that blew America's mind.  

Safe to say, I think Continuous Innovation isn't a fluke. It's been around for a while, and it's gonna stick around for a while, too.

#### Argument: XP requires too much change to adopt, and can only work with Senior Engineers

The point that "XP only works with Senior Engineers" relies on the premise that XP is a high-discipline mental framework, and that only professionals in the industry with the hard-earned wisdom can pull it off. Ordinary people are creatures of habit, they argue, so after the first major speed bump, the organizational adherence to these Extreme Principles will fall precipitously. 

But, this point was made in 2004, where the technology and tooling to automate these tasks simply didn't exist. Almost every modern software company has some sort of CI / CD process, where tasks like linting, unit tests, artifact building, and deployment are run automatically. Git has made branching and interleaving work across different developers trivially easy. Jira, Asana, and a plethora of other tools exist to help us track our work and project progress. Slack allows us to communicate asynchronously with one another and receive notifications from automated monitoring systems, allowing context to be shared quickly and efficiently. Many of these technologies reduce our need to be disciplined and strict with ourselves, freeing us to focus our mental efforts the adhering more closely to fewer principles. Introducing bite-sized chunks of change increase our chances of retaining these new work habits.

#### Argument: XP's practices are interdependent but few practical organizations are willing/able to adopt all the practices; therefore the entire process fails.

See above -- we've already adopted the vast majority of these practices without even knowing it. Many of the original arguments are no longer valid, because well, times are different. Most organizations have CI / CD, they have some form of a Continuous Innovation Mindset, and now, due to COVID, probably have the technology (Zoom, Slack) to facilitate remote pair programming sessions.

Ok, so now we realize that maybe all the reasons why we hated on these frameworks are wrong. But why should we switch? Why *now*?

I'm not saying that we need to rush to adopt all of these principles dogmatically or that Agile "is over". But, more than anything, I think developers and teams who are struggling to adjust to a remote workplace environment should experiment with some of the ideas I highlighted above, and see if it works for them. The nature of work is evolving as we speak; we should evolve our relationship to it as well. Don't be scared to challenge your assumptions! 

Thanks for reading! If you have any comments or responses, just tweet me [@nudgemybody](https://twitter.com/nudgemybody/status/1273174737980723201)!

Further Reading:

* Coders at Work: **[Interview with Jamie Zawinski](https://github.com/ndina/acm/blob/master/coders-at-work.pdf)**
* [An Introduction to XP](https://www.agilealliance.org/glossary/xp/#q=~(infinite~false~filters~(postType~(~'post~'aa_book~'aa_event_session~'aa_experience_report~'aa_glossary~'aa_research_paper~'aa_video)~tags~(~'xp))~searchTerm~'~sort~false~sortDirection~'asc~page~1))
* [A recent take on remote mob programming (2018)](https://www.remotemobprogramming.org/)
* [Industrial XP: Making XP Work in Large Organizations](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.694.2506&rep=rep1&type=pdf#:~:text=Industrial%20XP%20(IXP)%20is%20a,often%20face%20when%20implementing%20XP.)
* [When Is Xp Not Appropriate](http://wiki.c2.com/?WhenIsXpNotAppropriate) 
* [Wikipedia: 12 Practices of Extreme Programming](https://en.wikipedia.org/wiki/Extreme_programming_practices)