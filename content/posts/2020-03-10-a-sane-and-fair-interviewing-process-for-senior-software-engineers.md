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

![A screenshot of my most recent interview cycle](/media/screen-shot-2020-03-10-at-9.15.29-pm.png "C's get Degrees, amirite hahaha? *nudge nudge*")

Interviewing with so many companies, however, provided me a very useful breadth of data points: I could observe the nuances and differences in the interviewing styles. Some companies have much better interview processes than others. But before we jump into potential alternatives, let's break down this interview into its individual components, so we can understand the motivations for why we continue this practice.

## What are the (purported) benefits of LeetCode Interviews?

The world is not black and white; there are a few reasons why companies prefer LeetCode interviews. 

Companies are on a constrained timeline and budget to conduct interviews. Interviewing is costly, so companies look for ways in which they can maximize the signal of a potential candidate without wasting too many resources on a "dud".  Many companies believe that the most damaging thing that can happen to a company is hiring the wrong person. In this vein, interviewers are encouraged to pass over potential "good" candidates until they find their one "great" candidate. LC style interviews provide a quick and easy, binary decision making process. "Did the person solve the problem? No? Ok then, let's move on." 

The second benefit is that for junior engineers, this type of interview is still the best. Most recent graduates have never been exposed to modern software development practices, because academia often lags a decade or two behind the industry. When I got my first software internship , I didn't even know how to use git. I had only coded in C and in Java; Python and JavaScript weren't taught at my university. My databases class taught me about B-trees, not about how to use Mongo. As for alternatives: Either you skip the technical portion altogether (which is uncommon), or you make the candidate do a take-home, which they will need to spend a disproportionate amount of time on reading basic documentation and understanding how asynchronous requests work for web servers. 

Finally, there is a widely circulated belief that the engineers who can solve these LC problems are either hard workers who take their career seriously and prepared adequately, or naturally gifted problem solvers. The former represent the aspects of hard work and grit ("the ideal worker"), and the latter embody the traits of a mythical 10x engineer. In either case, these engineers will be a boon to your organization, so it makes sense to wait for one of these guys (or gals) to show up so you can reap the benefits. 

## What's wrong with these interviews

#### They are a terrible proxy for everyday development.

First and foremost, they are absolutely nothing like what you would be doing on the job. I can tell you with 100% certainty that I have **NEVER** needed to use a heap to solve a real-world programming problem, nor have I seriously considered the benefits of iterating through an array in reverse order to improve the efficiency of an application. These kinds of problems *don't exist* in modern day software engineering because the power and speed of recent computers make these performance tricks negligible.  It's a better use of someone's time if they spent the same effort solving more problems than optimizing a single problem.

It's also worth noting that [one of the most popular problems on LeetCode](https://leetcode.com/problems/number-of-islands) actually advocates "breaking the rules" and committing a programming faux-pas (overwriting state in the passed in matrix) in order to get the optimal solution. You shouldn't expect that a candidate, in 25-40 minutes, should consider breaking a tenet of good software engineering in order to solve a problem more efficiently. Thats not really fair, is it? Nor is that something that you would encourage them to do if they were working on your team, because they would be leaving a trail of bugs everywhere they go. 

#### They benefit only a small class of software engineers. 

Let's talk about the kinds of people who benefit from this kind of interview. Off the top of my head, I can think of two major groups: competitive programmers, and/or young, single candidates who have recently studied computer science in college. 

Think about it; would someone have the same chance of success in these interviews if they didn't have the same amount of time to prepare as the groups listed above? Probably not. So what about the person who is starting a family? What about the bootcamp graduate who hasn't studied computer science theory? Or the engineer with 10+ years of experience? What about the candidate who has adult-onset ADD / ADHD? You have to put in a serious amount of work to learn or refresh these concepts. And people wonder [why ageism is such a large problem in the software industry](https://softwareengineering.stackexchange.com/questions/61980/is-ageism-in-software-development-based-on-anything-other-than-bias). Let me be explicit: companies that rely solely on LeetCode style interviews cannot be considered "diverse" if their recruiting practices disproportionally discriminate against certain kinds of candidates.  

Which points to an obvious problem: If people don't have the means to be able to work on these esoteric exercises in their personal time, how do they study? Here's an unspoken "dirty secret" -- they do it on the job. They practice LeetCode during their work hours, often putting off of work in order to train because [we are incentivized to jump across companies to get raises](https://daedtech.com/notes-on-job-hopping-you-should-probably-job-hop/) instead of trying to work our way up the ranks. This is something I've observed in the workplace in almost every job I've had, and something I've guilty of doing as well. If only there was a better way... 

#### They cram too much into too small of a timeframe.

So, enough with the moral qualms about the interview; let's discuss the structure. I noted above how the typical interviewing process works. Having interviewed a few hundred candidates, it makes sense what people are testing for in each phase of the interview. The purpose of the introduction and the behavioral questions is to get a sense of culture fit with the candidate. Here, we are looking for answers that present insightful views into their decision making process, and their ability to communicate and gel with the team. Cool, makes sense. With the technical portion of the interview, we hope to get enough information to make a judgement on the candidate's:

* ability to code in a language of their (or our) choosing,
* analyze and solve a problem
* demonstrate knowledge of design patterns, testing, and clean code architecture
* familiarity with data structures, algorithms of the problem
* technical communication skills and coach-ability if they are stuck

And the last part of the interview is designed so we can allow the candidate some time to ask us questions so we can pitch the company favorably to them (aka make them drink the kool-aid). 

While its admirable to try and evaluate each of these important aspects, it's unreasonable to think that 1 or 2 interviewers can accurately glean this information in a single 1 hour interview. This is why some interviewers can wildly disagree with each other about a candidate's skill. Whats the common solution? Let's introduce a tool like greenhouse, and have a whole suite of engineers take time out of their day and rapid-fire interview the poor candidate (who is probably sweating profusely right now in the conference room you left them in). The law of averages will save us! If we all agree we *like* this candidate, then let's let her pass. But if one of us didn't get a good vibe? Well, "iTs bEtTeR to PaSs oN a GoOd CaNdiDaTe ThAn HiRe a BaD OnE", so it's sayonara and good luck to you.

We are trying to cram 3 interviews into 1. What's the old, tired joke about project managers? 

> Definition of Project Manager: 
>
> A person who thinks 9 women can deliver a baby in 1 month.

Oh right. Clearly, we have a habit in this industry of over extending our resources and delivering suboptimal solutions. It's no wonder why Fred Brooks is quoted as saying that "adding manpower to a late software project makes it later". We're doing the same thing with our interviews. 

#### Depending on the interviewer, you are rewarded little to no credit for communication, problem solving, or coach-ability -- just the results of your solution

Just to throw another wrench into this whole process, many interviewers pay lip-service to the idea that candidates should be judged holistically, but then judge them by very strict standards. Its not enough to try and articulate your approach, code a solution, and iterate in a real-life manner. If you get stuck and ask for hints, you get docked points. If you don't solve the problem the way your interviewer wants you to solve the problem, your solution is considered "messy" and "confusing". A sub-optimal solution? "Lacks Problem Solving Skills". 

Having someone coach you to a  workable solution means the highest score you can expect to get for the interview is a "Neutral". We don't observe the process of problem solving, we just reward people who already know the problem and get it right. Oh, you're supposed to show these steps to your interviewer, but you can't take too long on any one. 

#### They disenfranchise the middle 60% of all applicants. 

Up until now, dear reader, you've had to take me at my word -- but your patience is about to be rewarded. In my most recent interviewing process, I got a chance to interview with one of the bigger software job applicant websites and was able to peel back the lid on how interviews look like from the other side. As part of my interview, I was given a sample of actual data collected by the organization regarding job interviews and job hiring. Given a dataset of 800 actual candidates who all scored average or higher in a LC style assessment, how many of them got a call back from a company? Rather, how many calls did the best candidates get vs anyone who "passed"?

**NOTE: my goal is not to "out" any company, but highlight discrepancies in the hiring process. As a result, I will not be providing specifics about the company or providing information that would compromise their identity.** 



![Y axis: Number of Applicants, X axis: Number of Callbacks from companies](/media/screen-shot-2020-03-10-at-7.33.59-pm.png "The power curve of test performance vs. job opportunities")



In this graph, X axis represents the actual number of calls that a candidate in that bucket would get, and the Y axis represents the number of applicants receiving X calls.  As you can see, a large percentage of candidate got between 1 and 5 calls back, despite all candidates passing the test. Some candidates at the far end got as much as 120 different companies to callback! My first assumption is that this would be look more like bell curve, you know -- where most candidates would get an equal distribution of calls, and the outliers (people doing exceptionally well) would get proportionally more calls. 

I suppose, after some reflection, that this actually makes sense -- the best candidates are in short supply, so why wouldn't companies fight tooth-and-nail for them? So, I guess this graph isn't all bad, assuming that all the people getting calls are really incredible and knocked the test out of the park.



![Reality does not reflect expectations](/media/screen-shot-2020-03-10-at-7.44.12-pm.png "Comparing test performance to ")

Ok, what the fuck? Do you see that top line in the scatter plot? Those are people that scored perfect (5/5) on the assessment, but still didn't get the same number of calls as their peers. If this assessment was truly valuable, shouldn't all the people with the crazy high test scores be in the top right corner? Why are so many candidates on the left hand side of the graph? Again, these are people who *already passed the assessment*.

This definitely threw me for a loop in the interview. When I was talking to the other engineers, they admitted that while the platform was exceptional for the top 20% of candidates, the middle 60% often struggled to convert into full-time hires and would churn. In fact, this was an active area of development for the company. Pretty wild. So even if, say, you did well with this kind of assessment -- there is still quite a bit of disparity between testing well and actually landing the job.    

## How did these interviews get so popular?

By this point, I hope we can agree that LC interviews are trash. But why are they so prevalent? All roads point to FAANG. Since the early days of the internet era, companies like Microsoft, Yahoo, and other FAANGs have been employing these kinds of interviews in order to screen out as many applicants as they could. Part of this is logistics -- hence why we believe in this assumption that good candidates aren't actually "good enough", and why we need to only hire "the best" and have "bar raisers" to continually set higher expectations for our applicants. The less obvious reason was that it was good for the brand. [Like McKinsey](https://www.theatlantic.com/ideas/archive/2020/02/how-mckinsey-destroyed-middle-class/605878/), companies could improve their own image by generating applications that it could then reject, to establish its own eliteness. And by golly, wouldn't you know it. Every fresh-faced grad wants to eventually work for a FAANG because we've all been conditioned to think that working at a company at that level represents the zenith; that we can really, finally, and truly shake off this imposter syndrome and call ourselves "good engineers". 

Another reason is that this opened up a huge market for enterprising individuals: Cracking the Coding Interview, LeetCode, and the market for self-help guides began to boom. Not only did this add to the mystique of these FAANGS, it also meant that your original "hard" questions would become well-known given enough time. Now, we are in a rat race to "re-discover" new faces of computer science theory to test our candidates on. New questions means new editions of the book, renewed subscriptions for LeetCode and interviewcake.io and the like. It's not a coincidence that Dynamic Programming problems have become the new norm (which they teach in **grad school**). It's a self-perpetuating machine. 

Finally, for the average joe or jane that gets into a company based on their LC performance, some of them fall victim to their confirmation bias. Well, because *they* made it, everyone should make it to be considered "on the same level". They begin to view themselves as upholders of meritocracy, and pride themselves on being considered a "tough interviewer". Sadly, I think I fell into this camp for a long time. The toxic behavior of gate-keeping is very much enabled by this style of interview. It's important to clarify that this exists in other styles of interviews as well, but it seems especially rampant with LeetCode interviews.

## Current alternatives to LC interviews: Take-Homes

On one hand, we have LeetCode. On the other, we have Take-Home Assessments. Previously, I used to think of these assessments as the solution, but I've found the solution to be wonky at best, and actually worse than LeetCode interviews in the average case. 

 

Honorable Mention: No whiteboard interviews.

# Introducing a new style of Engineering Interviews

\- Remove Leetcode Mediums / Hard

\- Don't schedule more than 2 interview periods

\- Do a full day interview assessment