---
template: post
title: >-
  What's old is new again: why Extreme Programming works really well for remote
  teams
slug: consider-xp-for-distributed-teams
draft: false
date: 2020-05-28T05:58:41.206Z
description: >-
  With the pandemic, our social patterns have shifted overnight. Video calls
  have become the norm for both social and work engagements. Adapting to a
  long-term remote work lifestyle is challenging, but after some
  experimentation, I've discovered practices that have made me much more
  productive. I realized many of these ideas have already been introduced to the
  programming community for decades -- but they've been unfairly written off as
  irrelevant or impractical, despite making more sense now than ever before.
  Let's dig in.
category: productivity
tags:
  - remote
  - productivity
  - remote work
  - XP
  - extreme programming
  - agile
  - project management
  - organizational theory
---
Here's a contrarian opinion: we're doing project management all wrong. Well, at least since COVID started. We're struggling to adapt to a new routine and a new style of work that feels very foreign. Yet the the tools and processes we currently employ haven't been re-examined and re-thought. 

Due to the cultural shift caused by COVID, remote work in modern development teams can benefit from adopting the practices of XP, a project management strategy that was unfairly dismissed when it originally came out 20 years ago.  

## First off, what is XP (Extreme Programming)?

Extreme Programming is a software development style that takes the ideas from the Agile Development process and drives them to their "logical extremes", which culminates in a set of practices and philosophies that we should adopt to be happier, more productive software engineers. I'll add a link to the 12 practices at the bottom of the article for those curious, but I find that this [comment on a web forum from 2004](https://web.archive.org/web/20120101190943/http://www.satyakomatineni.com/akc/display?url=DisplayNoteIMPURL&reportId=862&ownerUserId=satya) captures the ethos of the movement succinctly.

![A screenshot of the web comment](/media/screen-shot-2020-06-17-at-6.48.14-pm.png "The 12 Principles of XP, according to the early internet.")

### Where did XP come from? A quick history

We're gonna keep this brief. Here's a 30 second crash course on the history of XP:

* In the land before time, software teams used a waterfall approach to software development. Most software projects were failures. (See: [The Mythical Man-Month](https://amzn.to/30QHn8F))
* In 1999, programmer Kent Beck released a book called [Extreme Programming Explained](https://amzn.to/2YLNE2S), wherein he outlines a radically new and different approach to software development.
* In early 2001, the industry's most well-regarded engineers (including Beck) [met at a famous ski resort](https://agilemanifesto.org/history.html) and distilled the ideas of XP into a new paradigm for how organizations should do software development. That paradigm is known as the Agile Software Development movement that's ubiquitous in software engineering these days.
* The Agile movement became fragmented as it grew in popularity. Over time, the Agile movement was co-opted by business folks and process-oriented project managers.

  * Rigid formalizations of the practices and process bloat infiltrated development teams, big and small. 
  * People began forking off and experimenting with alternative styles of software development, which is where [Mob Programming](https://en.wikipedia.org/wiki/Mob_programming#:~:text=Mob%20programming%20(informally%20mobbing)%20is,code%20at%20the%20same%20time.) is derived from.
  * Some methodologies, like Kanban, enjoyed commercial success in niche development teams. Kanban became the preferred strategy in DevOps or client-facing support teams, for example, because it allowed teams to allocate effort for unpredictable events that necessitate high urgency fixes.

XP and Mob Programming were decidedly less popular. These frameworks were in a bit of a limbo -- some of the top practitioners in our field were using XP, such as Martin Fowler and Robert C. Martin (Uncle Bob). In the end, XP was considered too unapproachable for the masses, too intense. Some practices, like pair programming or test-driven development, seem absolutely asinine from a business perspective. Indeed, if you visit the wikipedia page for Extreme Programming, they have a lengthy section dedicated to "[Controversial Aspects](https://en.wikipedia.org/wiki/Extreme_programming#Controversial_aspects)" -- not a ringing bell of endorsement if you ask me. 

Rather than describing each principle in detail and debating its merits (which sounds as boring to read as it is to write), let's discuss why some of the biggest critiques against this methodology don't hold water anymore.

#### Argument: Pair Programming is an inefficient allocation of valuable resources because it limits parallelism

In the past 3 months, I've spent more time pair-programming than I did in my entire career beforehand, but I've also been able to launch a large feature on our roadmap despite only being at the company for 3 months.  Pair-programming is the best substitute we have to colocating in our current distributed environment. I use it for many different tasks, and I do it often.

* I was able to ramp up very quickly on my team's product, architecture, and codebases. Pivotal Labs, a boutique software consultancy that practices XP, has written a pretty [good article](https://www.pivotaltracker.com/blog/how-pair-programming-and-mob-programming-help-quickly-onboard-new-software-engineers) about how XP is great system for onboarding new engineers.
* I've saved hours of dev time getting unblocked and helping my teammates configure their local environment / IDE. (We're a polyglot team with front-end, back-end, database, and ETL components). Sharing shortcuts about the tools we use have allowed us to shave off so much time in delivering tasks.
* I've been able to triage and isolate bugs much faster in pair-debugging sessions, preventing myself from "spinning my wheels" if I've been stuck on a problem for an hour or more. 
* As a team, we've been able to gather consensus and coordinate much more effectively because a discussion about the spec can highlight different assumptions we have about the same requirements, leading to clarifications and shared understanding about what we're trying to do. We're able to pivot and SPIKE on tasks more easily, allowing us to give better timelines to our business partners. 

That's not to say I agree with pair-programming **all the time.** I need my own time to chew on problems, to try out solutions, and to organize my thoughts so I'm not wasting the other person's time when we meet. I think this is where most people get it wrong; they think that have to be chained to the hip with their teammates and always operate lock-step with them, when that's not really how it works in practice. 

It's not a formal *thing* where we spend an uncomfortable amount of time in each other's personal space -- instead, it's like a game of football, where we huddle between plays to strategize before we execute some chunk of work. 

A beautiful example of this is in the book: "[Coders at Work: Reflections on the Craft of Programming](https://amzn.to/2ABX7SB)". In Chapter 2, Peter Seibel interviews [Jamie Zawinkski](https://www.jwz.org/about.html), one of the early engineers of Netscape and a founder of Mozilla. I'll post the part of the interview that stands out:

> *... \[discussion about building netscape 1.0] ...*
>
> **Seibel**: At some point you also worked on the mail reader, right?
>
> **Zawinkski**: In 2.0 Marc comes into my cubicle and says, "We need a mail reader." And I'm like, "OK, that sounds cool. I've worked on mail readers before." I was living in Berkeley and basically I didn't come into the office for a couple weeks. I was spending the whole time sitting in cafes doodling, trying to figure out what I wanted in a mail reader. Making lists, crossing it off, trying to decide how long it would take me. What should the UI look like?
>
> Then I came back and started coding. And then Marc comes in again and says, "Oh, so we hired this other guy who's done mail stuff before. You guys should work together." It's this guy Terry Weissman, who was just fantastic -- we worked together so well. And it was a completely different dynamic than it had been in the early days with the rest of the browser team. 
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

As the interview may have unintentionally highlighted, having discrete chunks of coder time was a key component in the success of their collaboration. The idea has been talked about ad nauseum in the book "[Deep Work](https://amzn.to/2zKQzR6)" by Cal Newport, and many companies have [independently verified](https://www.google.com/search?q=no+meeting+day+policy) that having distraction-free blocks for developers has yielded impressive productivity gains. (duh!)

This is another area where remote teams really benefit. For most non-parents, the home workspace is  more distraction-free than the office workplace. There isn't as much of an interest or need for water cooler chit-chat, and external distractions in the office such as a birthday or firing aren't nearly as disruptive. We don't need to pretend to be busy, because we're being  more carefully scrutinized on our output than our effort. (I'm not a parent, so unfortunately I can't comment for them). 

#### Argument: Continuous Design Approach is inefficient, impossible to measure, prone to getting off track, and "enormously expensive" to customers

Ok, most of these criticisms came from Matt Stephens and Doug Rosenberg, who co-authored a book called "[Extreme Programming Refactored: The Case against XP](https://amzn.to/30SIyVg)". And pretty much on all counts here, they're totally f*cking wrong.

I don't want to bash these guys too hard -- I mean, they wrote this in 2004, and I have the benefit of hindsight that they certainly did not have. But, in the 16 years since their book was released, the software engineering community has collectively agreed that a Continuous Design Approach (aka Continuous Innovation) is an ideology that not only works, but in fact is largely responsible for the success of many notable B2C startups in the post dot-com bust generation (e.g. AirBnb, Facebook). 

Eric Reis wrote the seminal book [the Lean Startup](https://amzn.to/2AAS6JZ), extolling the virtues continuous innovation while making the argument that it saves money in the long-run because you don't end up "building the wrong thing".

VC investor Peter Thiel gave further praise of Continuous Innovation and a "fail-fast and pivot" approach in his book [Zero to One](https://amzn.to/30P8b9k), while Paul Graham, co-founder of the Y Combinator startup accelerator, penned the famous essay "[Do things that don't scale](http://paulgraham.com/ds.html)". You can see it in the ethos of Facebook's old company motto: "[Move fast and break things](https://www.businessinsider.com/mark-zuckerberg-innovation-2009-10?r=US&IR=T)".

It's not just VCs and founders talking about it. Edward Lau, in his book [the Effective Engineer](https://amzn.to/2UWDbke), discusses tight-feedback loops and continuous delivery as the flywheel that powers the knowledge-discovery engine, which enable developers to iterate quickly and create leverage on their projects. 

And finally, Google Ventures has [their own process for applying a Continuous Design Approach](https://www.gv.com/sprint/) for all of their sprints, which struck a chord in the HCI / UX space. GV's design sprint bears striking resemblance to the company IDEO, which had their own [ABC Nightline special in 1999 about re-designing the shopping cart](https://www.youtube.com/watch?v=M66ZU2PCIcM&vl=en-US) that blew America's mind.  

Safe to say, I think Continuous Innovation isn't some fluke. It's been around for a while, and it's gonna stick around for a while, too.

#### Argument: XP requires too much change to adopt, and can only work with Senior Engineers

The point that "XP only works with Senior Engineers" relies on the premise that XP is a high-discipline mental framework, and that only professionals in the industry with the hard-earned wisdom can pull it off. Ordinary people are creatures of habit, they argue, so after the first major speed bump, the organizational adherence to these Extreme Principles will fall precipitously. 

But, this point was made in 2004, where the technology and tooling to automate these tasks simply didn't exist. Almost every modern software company has some sort of CI / CD process, where tasks like linting, unit tests, artifact building, and deployment are run automatically. Git has made branching and interleaving work across different developers trivially easy. Jira, Asana, and a plethora of other tools exist to help us track our work and project progress. Slack allows us to communicate asynchronously with one another and receive notifications from automated monitoring systems, allowing context to be shared quickly and efficiently. Many of these technologies reduce our need to be disciplined and strict with ourselves, freeing us to focus our mental efforts the adhering more closely to fewer principles. Introducing bite-sized chunks of change increase our chances of retaining these new work habits.

#### Argument: XP's practices are interdependent but few practical organizations are willing/able to adopt all the practices; therefore the entire process fails.

See above -- we've already adopted the vast majority of these practices without even knowing it. Many of the original arguments are no longer valid, because well, times are different. No need to belabor the point.

Ok, so now we realize that maybe all the reasons why we hated on these frameworks are wrong. But why should we switch? Why *now*?

I'm not saying that we need to rush to adopt all of these principles dogmatically or that Agile "is over". But, more than anything, I think developers and teams who are struggling to adjust to a remote workplace environment should experiment with some of the ideas I highlighted above, and see if it works for them. The nature of work is evolving as we speak; we should evolve our relationship to it as well. Don't be scared to challenge your assumptions! 

## Ok, fine. How can I get started?

If you're interested in giving XP a shot, here are a few recommendations I have:

1. Watch this talk by Dan North called "[Patterns for Effective Delivery](https://vimeo.com/24681032)". Pay special attention to all the strategies he lays out: (Ginger Cake, Dancing Skeleton, Spike & Stabilize). This talk has influenced me the most in my career, its 45 minutes of poignant insight-after-insight. If there is one thing a person should take away after watching this video, it's *what working on an XP team should feel like*.


2. It's time to wash ourselves clean of the toxic traits of "Enterprise Agile" and our unhealthy obsession with time-based planning. We need to be able to distill the elements of Agile / XP down to their core, so we can identify which practices we agree with and want to bring into our organizations.  Watch [this video by Allen Golub on the #noestimates movement](https://www.youtube.com/watch?v=QVBlnCTu9Ms), to get an appreciation for how Agile is much more open-ended than what we usually see in the office. (I've had mixed results with #noestimates, but it does provide food for thought).


3. Take the time to observe the the team's culture with respect to ad-hoc video calls. This is where we can make the most gains in our remote environment. We need to build a culture within ourselves and our teams where it is OK to pair for 5 minutes on a bug or sync on some product spec. It's important to be respectful of each other's time, but we shouldn't sacrifice team alignment and group intelligence for the sake of inconveniencing each other.


4. When you do grooming or sprint planning meetings with the team, take care to observe what items are high-risk. What are our known-unknowns? How familiar are we with the task? If it feels like we don't already have the solution in mind when we're discussing a ticket, treat this as an opportunity to do a SPIKE. Remember, it's totally fine to not know how a project will end up when we're still in the beginning phases. Expect to have curve balls thrown at you. Spike and de-risk things as they come up. It's ok to come up with Spike's mid-sprint if you hit a blocker and need to pivot. Velocity Planning, all that stuff -- it doesn't matter as much as  actually shipping a good, working solution. 


5. Do regular retrospectives where we reflect upon how efficient and productive we feel as a team. Try new ideas to improve our process. Get rid of things that don't work. Try to use some proxy for quantitative progress as well (Jira Tickets closed per sprint, or number of commits in Github, or whether the sprint goal was achieved). Use this is a feedback loop to determine what your team's optimal work flow is. Every team is different, at the end of the day XP is as much as shift in perspective as it is a process for doing software engineering.



I hope you enjoyed the essay, thanks for reading! If you have any comments or responses, just tweet me [@nudgemybody](https://twitter.com/nudgemybody/status/1273174737980723201)!

Further Reading:

* Coders at Work: **[Interview with Jamie Zawinski](https://github.com/ndina/acm/blob/master/coders-at-work.pdf)**
* [An Introduction to XP](https://www.agilealliance.org/glossary/xp/#q=~(infinite~false~filters~(postType~(~'post~'aa_book~'aa_event_session~'aa_experience_report~'aa_glossary~'aa_research_paper~'aa_video)~tags~(~'xp))~searchTerm~'~sort~false~sortDirection~'asc~page~1))
* [A recent take on remote mob programming (2018)](https://www.remotemobprogramming.org/)
* [Industrial XP: Making XP Work in Large Organizations](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.694.2506&rep=rep1&type=pdf#:~:text=Industrial%20XP%20(IXP)%20is%20a,often%20face%20when%20implementing%20XP.)
* [When Is Xp Not Appropriate](http://wiki.c2.com/?WhenIsXpNotAppropriate) 
* [Wikipedia: 12 Practices of Extreme Programming](https://en.wikipedia.org/wiki/Extreme_programming_practices)