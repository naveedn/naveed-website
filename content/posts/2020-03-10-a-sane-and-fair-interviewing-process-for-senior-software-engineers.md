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

Now imagine doing this 2-4 times in the process of interviewing with 1 company. You may be thinking, "its not so bad", consider this: my last interviewing period lasted about 4 months, and I had repeated this process with 30+ companies. Thats a **lot** of interviews, all following the same routine. With every rejection, I felt a sting of pride -- I *knew* I was good, but I struggled with these interviews because I couldn't solve these problems fast enough.

Interviewing with so many companies, however, provided me a very useful breadth of data points: I could observe the nuances and differences in the interviewing styles. Some companies have much better interview processes than others. But before we jump into potential alternatives, let's break down this interview into its individual components, so we can understand the motivations for why we continue this practice.

## What are the (purported) benefits of LeetCode Interviews?

The world is not black and white; there are a few reasons why companies prefer LeetCode interviews. 

Companies are on a constrained timeline and budget to conduct interviews. Interviewing is costly, so companies look for ways in which they can maximize the signal of a potential candidate without wasting too many resources on a "dud".  Many companies believe that the most damaging thing that can happen to a company is hiring the wrong person. In this vein, interviewers are encouraged to pass over potential "good" candidates until they find their one "great" candidate. LC style interviews provide a quick and easy, binary decision making process. "Did the person solve the problem? No? Ok then, let's move on." 

The second benefit is the widely circulated belief that the engineers who can solve these LC problems are either hard workers who take their career seriously, or naturally gifted problem solvers. The former represent the aspects of hard work and grit (the ideal worker), and the latter embody the traits of a mythical 10x engineer. In either case, these engineers will be a boon to your organization, so it makes sense to wait for one of these guys (or gals) to show up so you can reap the benefits. 

## What's wrong with these interviews

#### They are a terrible proxy for everyday development.

First and foremost, they are absolutely nothing like what you would be doing on the job. I can tell you with 100% certainty that I have **NEVER** needed to use a heap to solve a real-world programming problem, nor have I seriously considered the benefits of iterating through an array in reverse order to improve the efficiency of an application. These kinds of problems *don't exist* in modern day software engineering because the power and speed of recent computers make these performance tricks negligible.  It's a better use of someone's time if they spent the same effort solving more problems than optimizing a single problem.

It's also worth noting that [one of the most popular problems on LeetCode](https://leetcode.com/problems/number-of-islands) actually advocates "breaking the rules" and committing a programming faux-pas (overwriting state in the passed in matrix) in order to get the optimal solution. You shouldn't expect that a candidate, in 25-40 minutes, should consider breaking a tenet of good software engineering in order to solve a problem more efficiently. Thats not really fair, is it? Nor is that something that you would encourage them to do if they were working on your team, because they would be leaving a trail of bugs everywhere they go. 

#### They benefit only a small class of software engineers. 

Let's talk about the kinds of people who benefit from this kind of interview. Off the top of my head, I can think of two major groups: competitive programmers, and/or young, single candidates who have recently studied computer science in college. 

Think about it; would someone have the same chance of success in these interviews if they didn't have the same amount of time to prepare as the groups listed above? Probably not. So what about the person who is starting a family? What about the bootcamp graduate who hasn't studied computer science theory? Or the engineer with 10+ years of experience? You have to put in a serious amount of work to learn or refresh these concepts. And people wonder [why ageism is such a large problem in the software industry](https://softwareengineering.stackexchange.com/questions/61980/is-ageism-in-software-development-based-on-anything-other-than-bias). Let me be explicit: companies that rely solely on LeetCode style interviews cannot be considered "diverse" if their recruiting practices disproportionally discriminate against certain kinds of candidates.  

Which points to an obvious problem: If people don't have the means to be able to work on these esoteric exercises in their personal time, how do they study? Here's an unspoken "dirty secret" -- they do it on the job. They practice LeetCode during their work hours, often putting off of work in order to train because [we are incentivized to jump across companies to get raises](https://daedtech.com/notes-on-job-hopping-you-should-probably-job-hop/) instead of trying to work our way up the ranks. This is something I've observed in the workplace in almost every job I've had, and something I've guilty of doing as well. If only there was a better way... 

#### They cram too much into too small of a timeframe.

\- They disenfranchise the middle 60% of all applicants. 

\- Depending on the interviewer, you are rewarded little to no credit for communication, problem solving, or coach-ability -- just the results of your solution

## How did these interviews get so popular?

\- Google / FAANG companies 

\- Cracking the coding interview and the market for self-help guides

\- The facade of meritocracy, the toxic behavior of gate-keeping 

## Current Alternatives to LC interviews: a comparison

\- No whiteboard interviews

\- Take Home projects

## Introducing a new style of Engineering Interviews

\- Remove Leetcode Mediums / Hard

\- Don't schedule more than 2 interview periods

\- Do a full day interview assessment