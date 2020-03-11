---
template: post
title: A sane and fair process for conducting Senior Software Engineering interviews
slug: alternative-senior-engineer-interview-process
draft: true
date: 2020-03-10T22:15:40.358Z
description: >-
  Let's address the elephant in the room: Interviewing for (senior) software
  engineers is a terrible process that everyone admits is broken. Because of the
  lack of alternatives presented to us, we are forced to use Leetcode style
  interviews. But is there a better way? Read on to find out. 
category: interviews
tags:
  - interviewing
  - technical
---
The bane of every software engineer's existence (if there is one) has got to be interviewing. For reasons unbeknownst to me, scores of engineers every day are subjected to draconian LeetCode style interviews, for which nothing short of a smashing success means failure, and eventual rejection from the company. 

For the uninitiated, these LeetCode interviews are designed to test an engineer's "fundamentals". They place a particular emphasis on using less common data structures or algorithms -- stuff most programmers haven't studied since college --  usually paired with a "trick" to make the problem more difficult. Here's the breakdown of a typical 1 hour long interview:

1. The interviewers introduce themselves, and ask the applicant to introduce themselves \[~5-10 minutes]
2. The interviewers may engage in a few behavioral questions \[~10-15 minutes, often skipped or done at the end]
3. A programmer is presented with a logic / programming problem.  They are usually given anywhere from 25-40 minutes to:

   * Understand the problem 
   * Determine the optimal solution (by figuring out the trick, correct data structure, and algorithm)
   * Write it up on a whiteboard
   * Explain their answer to the interviewers, and modify their solution to solve additional constraints by their interviewers
4. Interviewers allow the programmer to ask the interviewers questions about the company \[~5-10 minutes]

Now imagine doing this 2-4 times in the process of interviewing with 1 company. You may be thinking, "its not so bad", consider this: my last interviewing period lasted about 4 months, and I had repeated this process with 30 companies. Thats a **lot** of interviews, all following the same routine. With every rejection, I felt a sting of pride -- I *knew* I was good, but I struggled with these interviews because I couldn't solve these problems fast enough.

![A screenshot of my most recent interview cycle](/media/job-prospects-screenshot.png "C's get Degrees, amirite hahaha? *nudge nudge*")

Interviewing with so many companies, however, provided me a very useful breadth of data points: I could observe the nuances and differences in the interviewing styles. Some companies have much better interview processes than others. But before we jump into potential alternatives, let's break down this interview into its individual components, so we can understand the motivations for why we continue this practice.

## What are the benefits of LeetCode Interviews?

The world is not black and white; there are a few reasons why companies prefer LeetCode interviews. 

Companies are on a constrained timeline and budget to conduct interviews. Interviewing is costly, so companies look for ways in which they can maximize the signal of a potential candidate without wasting too many resources on a "dud".  Many companies believe that the most damaging thing that can happen to a company is hiring the wrong person. In this vein, interviewers are encouraged to pass over potential "good" candidates until they find their one "great" candidate. LC style interviews provide a quick and easy, binary decision making process. "Did the person solve the problem? No? Ok then, let's move on." 

The second benefit is that for junior engineers, this type of interview is still the best. Most recent graduates have never been exposed to modern software development practices, because academia often lags a decade or two behind the industry. When I got my first software internship, I didn't even know how to use git. I had only coded in C and in Java; Python and JavaScript weren't taught at my university. My databases class taught me about B-trees, not about how to use Mongo. As for alternatives: Either you skip the technical portion altogether (which is uncommon), or you make the candidate do a take-home, which they will need to spend a disproportionate amount of time on reading basic documentation and understanding how asynchronous requests work for web servers. 

Finally, there is a widely circulated belief that the engineers who can solve these LC problems are either hard workers who take their career seriously and prepared adequately, or naturally gifted problem solvers. The former represent the aspects of hard work and grit ("the ideal worker"), and the latter embody the traits of a mythical 10x engineer. In either case, these engineers will be a boon to your organization, so it makes sense to wait for one of these people to show up so you can reap the benefits. 

## What's wrong with these interviews

#### They are an inaccurate proxy for everyday development.

First and foremost, they are absolutely nothing like what you would be doing on the job. I can tell you with 100% certainty that I have **NEVER** needed to use a heap to solve a real-world programming problem, nor have I seriously considered the benefits of iterating through an array in reverse order to improve the efficiency of an application. These kinds of problems *don't exist* in modern day software engineering because the power and speed of recent computers make these performance tricks negligible.  It's a better use of someone's time if they spent the same effort solving more problems than optimizing a single problem.

It's also worth noting that [one of the most popular problems on LeetCode](https://leetcode.com/problems/number-of-islands) actually advocates "breaking the rules" and committing a programming faux-pas (overwriting state in the passed in matrix) in order to get the optimal solution. You shouldn't expect that a candidate, in 25-40 minutes, should consider breaking a tenet of good software engineering in order to solve a problem more efficiently. Thats not really fair, is it? Nor is that something that you would encourage them to do if they were working on your team, because they would be leaving a trail of state-related bugs everywhere they go. 

#### They benefit only a small class of software engineers.

Let's talk about the kinds of people who benefit from this kind of interview. Off the top of my head, I can think of two major groups: competitive programmers, and/or young, single candidates who have recently studied computer science in college. 

Think about it; would someone have the same chance of success in these interviews if they didn't have the same amount of time to prepare as the groups listed above? Probably not. So what about the person who is starting a family? What about the bootcamp graduate who hasn't studied computer science theory? Or the engineer with 10+ years of experience? What about the candidate who has adult-onset ADD / ADHD? You have to put in a serious amount of work to learn or refresh these concepts. And people wonder [why ageism is such a large problem in the software industry](https://softwareengineering.stackexchange.com/questions/61980/is-ageism-in-software-development-based-on-anything-other-than-bias). Let me be explicit: companies that rely solely on LeetCode style interviews cannot be considered "diverse" if their recruiting practices disproportionally discriminate against certain kinds of candidates.  

Which points to an obvious problem: If people don't have the means to be able to work on these esoteric exercises in their personal time, how do they study? One way is to quit your current company, take a small break, and then "grinding LeetCode" full time until you are ready to interview. In fact, for senior engineers who are considering job hopping, this is probably the best way to get your next job (currently). Well, what about the people who aren't willing to forego their paycheck in order to study? Here's an unspoken "dirty secret" -- they do it on the job. They practice LeetCode during their work hours, often putting off actual work in order to train. This is something I've observed in the workplace in almost every job I've had. 

#### They cram too much into too small of a timeframe.

So, enough with the moral qualms about the interview; let's discuss the structure. I noted above how the typical interviewing process works. Having interviewed a few hundred candidates myself, it makes sense what people are testing for in each phase of the interview. The purpose of the introduction and the behavioral questions is to get a sense of culture fit with the candidate. Here, we are looking for answers that present insightful views into their decision making process, and their ability to communicate and gel with the team. Cool, makes sense. With the technical portion of the interview, we hope to get enough information to make a judgement on the candidate's:

* ability to code in a language of their (or our) choosing,
* analyze and solve a problem
* demonstrate knowledge of design patterns, testing, and clean code architecture
* familiarity with data structures, algorithms of the problem
* technical communication skills and coach-ability if they are stuck

And the last part of the interview is designed so we can allow the candidate some time to ask us questions so we can pitch the company favorably to them (aka make them drink the kool-aid). 

While its admirable to try and evaluate each of these important aspects, it's unreasonable to think that 1 or 2 interviewers can accurately glean this information in a single 1 hour interview. This is why some interviewers can wildly disagree with each other about a candidate's skill. Whats the common solution? Let's introduce a tool like greenhouse, and have a whole suite of engineers take time out of their day and rapid-fire interview the poor candidate (who is probably sweating profusely right now in the conference room you left them in). The law of averages will save us! If we all agree we *like* this candidate, then let's let her pass. But if one of us didn't get a good vibe? Well, "its better to pass on a good candidate than hire a bad one", so it's sayonara and good luck to you.

We are trying to cram 3 interviews into 1. How's that old, tired joke about project managers go? 

> Definition of Project Manager: 
>
> A person who thinks 9 women can deliver a baby in 1 month.

Oh right. Clearly, we have a habit in this industry of over extending our resources and delivering suboptimal solutions. It's no wonder why Fred Brooks is quoted as saying that "adding manpower to a late software project makes it later". We're doing the same thing with our interviews. 

#### Depending on the interviewer, you are rewarded little to no credit for communication, problem solving, or coach-ability -- just the results of your solution

Just to throw another wrench into this whole process, many interviewers pay lip-service to the idea that candidates should be judged holistically, but then judge them by very strict standards. Its not enough to try and articulate your approach, code a solution, and iterate in a real-life manner. If you get stuck and ask for hints, you get docked points. If you don't solve the problem the way your interviewer wants you to solve the problem, your solution is considered "messy" and "confusing". A sub-optimal solution? "Lacks Problem Solving Skills". 

Having someone coach you to a workable solution means the highest score you can expect to get for the interview is a "Neutral". We don't observe the process of problem solving and judge based on that -- we only reward people who get it right. 

#### They disenfranchise the middle 60% of all applicants.

 In my most recent interviewing process, I got a chance to interview with one of the bigger software job applicant websites and was able to peel the lid back on how interviews look like from the other side. As part of my interview, I was given a sample of actual data collected by the organization regarding job interviews and job hiring. Given a dataset of 800 real candidates who all scored satisfactory or higher in a LC style assessment, how many of them got a call back from a company? Based on their test score, how many calls did the best candidates get vs anyone who "passed"?

**NOTE: my goal is not to "out" any company, but highlight discrepancies in the hiring process. As a result, I will not be providing specifics about the company or providing information that would compromise their identity.** 

![Y axis: Number of Applicants, X axis: Number of Callbacks from companies](/media/screen-shot-2020-03-11-at-2.49.52-am.png "The power curve of test performance vs. job opportunities")

In this graph, X axis represents the actual number of calls from a company that a candidate would get, and the Y axis represents the number of applicants receiving the same amount of callbacks.  As you can see, a large percentage of candidate got between 1 and 10 calls back, despite all candidates passing the test. One candidate at the far end got 120 different companies to express interest in them! My first assumption is that this would be look more like bell curve, you know -- where most candidates would get an equal distribution of calls, and the outliers (people doing exceptionally well) would get proportionally more calls, but within reason. 

I suppose, after some reflection, that this actually makes sense -- the best candidates are in short supply, so why wouldn't companies fight tooth-and-nail for them? So, I guess this graph isn't all bad, assuming that the people getting calls are really incredible and knocked the test out of the park relative to their peers.

![Reality does not reflect expectations](/media/screen-shot-2020-03-11-at-2.55.24-am.png "Comparing test performance to ")

But that's not actually the case. Do you see that top line in the scatter plot? Those are people that scored perfect (5/5) on the assessment, but most of them got the same number of callbacks as their peers who only scored 3/5. If this assessment was representative of a meritocracy, shouldn't all the people with the perfect test scores be in the top right quadrant of the graph? Why are so many candidates on the left hand side of the graph, despite having flawless scores and being recommended to the company?

This definitely threw me for a loop in the interview. The interviewers, noticing my perplexed expression, admitted to me that while the platform was exceptional for 20% of candidates, the middle 60% struggled to convert into full-time hires and would churn. In fact, this was an active area of development for the company, playing around with candidate profile visibility so everyone would get a fair shot. All of this is to say that even if you studied hard and did well with this kind of assessment -- there is still no guarantee that you'd actually get the job.    

## How did these interviews get so popular?

By this point, I hope we can agree that LC interviews are trash. But why are they so prevalent? All roads point to FAANG. Since the early days of the internet era, companies like Microsoft, Yahoo, and other FAANGs have been employing these kinds of interviews in order to screen out as many applicants as they could. Part of this is logistics -- the harder the interviews, the smaller the pool of contenders, which allow companies to make hiring decisions more quickly. Hence why we believe in this assumption that good candidates aren't actually "good enough", and why we need to only hire "the best" and have "bar raisers" to continually set higher expectations for our applicants. The less obvious reason was that it was good for the brand. [Like McKinsey](https://www.theatlantic.com/ideas/archive/2020/02/how-mckinsey-destroyed-middle-class/605878/), companies could improve their own image by generating applications that it could then reject, to establish its own eliteness. And by golly, wouldn't you know it. Every fresh-faced grad wants to eventually work for a FAANG because we've all been conditioned to think that working at a company at that level represents the zenith; that we can really, finally, and truly shake off this imposter syndrome and call ourselves "great engineers". 

Another reason is that this opened up a huge market for enterprising individuals: Cracking the Coding Interview, LeetCode, and the market for self-help guides began to boom. Not only did this add to the mystique of these FAANGS, it also meant that your original "hard" questions would become well-known given enough time. Now, we are in a rat race to "re-discover" new faces of computer science theory to test our candidates on. New questions means new editions of the book, renewed subscriptions for LeetCode and interviewcake.io and the like. It's not a coincidence that Dynamic Programming problems have become the new norm (which they teach as a class at my **grad school**, no joke). It's a self-perpetuating machine. 

Finally, for the average joe or jane that gets into a company based on their LC performance, some of them fall victim to their confirmation bias. Well, because *they* made it, everyone should make it to be considered "on the same level". They begin to view themselves as upholders of meritocracy, and pride themselves on being considered a "tough interviewer". Sadly, I think I fell into this camp for a long time. The toxic behavior of gate-keeping is very much enabled by this style of interview. It's important to clarify that this exists in other styles of interviews as well, but it seems especially rampant with LeetCode interviews.

## Current alternatives to LC interviews: Take-Homes

On one hand, we have LeetCode. On the other, we have Take-Home Assessments. Previously, I used to think of these assessments as a superior solution, but after this last round of interviews, I've found it to be wonky at best, and worse than LeetCode interviews in the average case.

#### What they get right

* They allow the interviewee the flexibility to do the interview over a longer period of time, so the "time crunch" isn't a factor. Given the amount of time, a candidate can usually build and present a higher quality solution, which is analogous to the work they would do on the job.
* They are usually more pragmatic in nature, testing a coder's ability to demonstrate knowledge in areas that are analogous to their everyday work (like design patterns, documentation, testing, architecture decisions) -- stuff that would be hard to communicate effectively in the span of an hour long interview.

#### What they get wrong

* They are higher effort for both parties. Because of the asynchronous nature of these projects, getting clarifications on ambiguous wording via email can take anywhere from a couple hours to a few days, throwing you off your groove if you're coding the assessment. Candidates are usually interviewing with a handful of companies at a time, and these take-homes take a disproportionate amount of time when compared a quick LeetCode style interview. For the engineers reviewing these projects, you generally have to review a candidates project alongside your other work, whereas with an interview, you have a concrete window in which to handle the interviewing task. And, if you work at a company where you might have a few hundred candidates, this process of individual code review does not scale -- you can't possibly review them all. 
* Because they take place over a longer period of time, they can often balloon in scope. Some companies give lengthy projects as a way to judge efficacy, and there isn't a good standard on what a candidate should and shouldn't accept. The ambiguity makes it difficult for a candidate to know how much to invest, especially if they are interviewing with a few companies at once. Whats the time frame? 3 hours? 6? Should I have a full test suite as well? Not having a clear time frame can muddle the results, making it difficult for interviewers to get a good litmus test, while making some candidates choose an "incorrect" amount of time on the project.

In my own experience, I found myself actually wanting to do a LeetCode interview after getting rejected by a company after doing their take home. For me, doing that one programming project took the span of scheduling and completing about 3 LC style phone screens. It's just not a good use of my time. 

However, for some people, this is still a great way to interview, and for the companies offering it, I applaud you for not cargo culting. If this is your jam, I would highly recommend taking a look at [the list of companies that don't do whiteboard interviews.](https://github.com/poteto/hiring-without-whiteboards)

# Introducing a new style of Engineering Interviews

From my experiences interviewing, there were a few companies that stand out as having a novel and great interview process. They were short and efficient, thorough and challenging for the senior engineering role. Whats more interesting was that the interviews were structurally very similar to each other, albeit some details are different. I've adapted some of the common ideas into the format below.

They are only 2 interviews periods. One is an initial phone screen with the recruiter or hiring manager. These conversations would be anywhere from 30-60 minutes, where the company gets a feel for you and whether or not they are interested. This isn't different from most interviews currently, so I'll move on. 

The second interview is where things get interesting: It's a full day on-site assessment, broken out into a few parts. It goes something like this:

1. The candidate arrives, and is brought to a conference room. The recruiter provides the candidate with a written spec for a programming project. After 15 minutes, an engineer steps into the room, and provides any clarifications and answers any question the candidate has.
2. The candidate is then left alone and given 3 hours to implement the spec as best as they can. The test is open-book, open everything. They can use whatever IDE, language, or framework they want. The programming project is composed of multiple logical phases, with the goal being to complete the requirements for one phase before moving onto the next one. Each phase tests a different aspect of the project or becomes more difficult than the previous. *I will provide an example below.*
3. At the 3 hour mark, the candidate zips up their project, and sends it to a predetermined destination.
4. The candidate is given a 30-60 minute lunch break / informal interview, where they can talk to an engineer that currently works at the company and get answers to any questions they may have, while getting some food.  
5. After lunch, 2 interviewers come into the room for a 1 hour interview where the candidate will demo their project, walk through their code solution, and field any questions from the stakeholders. The interviewers can ask questions regarding architecture decisions, ask the candidate to implement a later phase, modify some of their code due to a changing  scaling requirement, and / or ask the candidate about what parts were difficult / challenging.

   **NOTE: Every company that performed this kind of interview did it with *every* candidate, including the interviewers themselves. As such, they often were familiar the details, and it was easy to swap interviewers on short notice.** 
6. The candidate is given a 15 minutes break, where the interviewers confer and decide whether to keep going. This is probably the most contentious part: If the candidate did not perform well satisfactorily on the programming project or the project review, then the interview would end there and the candidate leaves. If the candidate passes, then we jump into the final rounds of the interview.
7. The next round(s) is either a system design or a technical communication interview. System design interviews are par for the course in terms of senior software engineering interviews -- not to mention that this is something that a candidate should be familiar with in the course of their everyday work. Technical Communication Interviews are a flavor of System Design Interviews where the candidate is asked to describe a past project they built in technical detail, discussing the trade-offs, the constraints, the solution, and their involvement with the project. 
8.  The day would end with a behavioral interview, where a candidate's culture fit aligns with company values. Pretty standard.

Could one swap out the later interviews with another coding question? Sure. But one thing I've noticed is that doing a 3 hour project is *tiring.* Keeping yourself focused, efficient, and calm for that duration is pretty draining. You have to expect that your candidates are human too -- so expect that their interview performance will degrade over time. If you plan on doing coding questions in addition to the project, perhaps do those questions in the morning, saving the afternoon for the project, and making the project slightly easier. 



## A Sample Programming Project

Here is a slightly modified question I was given from a company.

> Implement a web server link-shortening service, like bit.ly or tinyURL. 

#### Phase 1:

* Your phase 1 deliverables should include a webserver listening on port 5000
* The web server API should accept a POST request that allows the user to submit a URL, and returns a shortened link
* The web server should accept a GET request with the shortened link in the request path, and redirects the browser to original URL
* Implement a DELETE API, where given the original URL and the shortened link, the entry is removed from the service
* Phase 1 deliverables should include both documentation and tests

#### Phase 2 (only do this after finishing Phase 1):

* Support TTLs (time-to-live) expiration for a given URL. The user can pass in an optional TTL in seconds in the POST request for how long they want the link to be "valid". Expired links do not redirect to the original destination, and are removed from the service. An appropriate error is returned. 
* Phase 2 deliverables should include both documentation and tests

#### Phase 3 (Only do this after finishing Phase 2): 

* Support a temporary number of "uses" per shortened link. The user can pass in an integer corresponding to the number of times the shortened url can be used before it is automatically expired.
* Phase 3 deliverables should include both documentation and tests

#### Phase 3 Alternate (Only do this after finishing Phase 2):

* Deploy this on a live server! Your interviewer should have provided you with an Amazon EC2 Instance that you can use as a sandbox. Get the app working on the cloud!

### How to grade this kind of programming project

How do we determine what is a fair, but rigorous question to implement in 3 hours? Make sure all your mid-level and senior engineers can implement Phase 1 in the three hour time period. While this question looks deceptively simple, there are a bunch of gotchas to work through, and doing the setup + project + tests + documentation is already pretty tough. If everyone on the team can't do Phase I in 3 hours, then your question is too hard. Phase 1 should encapsulate an entire functioning project, where Phase 2 and beyond test refactoring, design, or other aspects of software engineering like deployment and infrastructure. Phase 1 is the meat of what is being evaluated, where Phase 2 and beyond are supplementary. 

In one of the instances where I was given this kind of interview, I was only able to barely solve Phase 1 before my time was up. I thought I had failed it. During my one hour review with the interviewers, they had me implement the logic for phase 2 in front of them. Again, I thought I did poorly. At the end of the day, the recruiter told me that I did *really* well on the project. I found it so refreshing to be evaluated by the relative value of each phase. It wasn't a race to implement all the features -- but to pick and choose how to best solve the problem, how to structure your code in a way that would allow you to iterate, but overall, deliver the most important thing to your customer (phase 1 - a complete, demo-able software implementation).

## How this type of interview addresses the needs of both parties