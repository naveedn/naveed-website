---
template: post
title: A sane and fair process for conducting Senior Software Engineering interviews
slug: alternative-senior-engineer-interview-process
draft: true
date: 2020-03-12T22:15:40.358Z
description: >-
  Despite the numerous problems, we still use LeetCode style interviews almost
  exclusively in our hiring process. Is there a better way? Read on to find
  out. 
category: interviews
tags:
  - interviewing
  - technical
---
*For those just jumping in, the previous parts of this essay can be found here:*

* [Part 1: Interviews for Senior Software Engineers are F*cking Broken](https://www.naveed.dev/posts/senior-engineer-interviews-broken)
* [Part 2: Evaluating the alternatives to the LeetCode Style Interview](https://www.naveed.dev/posts/leetcode-alternatives-compared)

# Introducing a new style of Engineering Interviews

From my experiences interviewing, there were a few companies that stand out as having a novel and great interview process. They were short and efficient, thorough and challenging for the senior engineering role. Whats more interesting was that the interviews followed a very similar routine to each other. The title of this post is a bit of misnomer -- while this interview style already exists, it doesn't get NEARLY enough credit.

## The 3-hour on-site, unsupervised coding challenge

##### Followed by a 1-hour technical deep dive afterwards

Essentially, you try to take the best aspects of the Pragmatic Practical, Take-Homes, and System Design while minimizing each solution's downsides. Before we break down why this is an efficient method for Technical Interviewing, lets walk through a hypothetical interview day for both the candidate and the company.

### The interviewing schedule

* Part 1: A recruiter and a candidate connect, and the interview conversation begins
* Part 2: A hiring manager connects with the candidate, doing a 30 minute or 1-hour long phone screen to review candidate experience and determine fit within the team
* Part 3:  The candidate is brought on-site for a full-day assessment
* Part 4: The team meets about a candidate at the end of the day, and makes a go / no-go decision
* Part 5: A recruiter reaches out within 24-48 hours, and relays the decision to the candidate

### The on-site schedule

1. The candidate arrives and is brought into a conference room. The recruiter provides the candidate with a written spec for the programming project
2. After 15 minutes, an engineer steps into the room, and provides clarifications to any questions the candidate has after reading the spec. The engineer provides a phone number for the candidate to text if they need the engineer to come back
3. The candidate is then left alone and given 3 hours from that point to implement the spec as best as they can. The test is open-book, and they can use whatever IDE, language, framework or tools they want. The programming project is composed of multiple logical phases, with the goal being to complete the requirements of each phase before moving onto the next one. Each phase tests a different aspect of the project or becomes more difficult than the previous.
4. At the 3 hour mark, the candidate zips up their project, and sends it to a predetermined destination like a dropbox folder or email
5. The candidate is then given a 30 - 60 minute lunch break with a "buddy". This informal interview is where they get the chance to talk to an engineer that currently works at teh company and can provide answers to any questions about company culture the candidate has
6. After lunch, 2 engineers come into the room and do a technical deep dive with the candidate for an hour. The candidate will demo the project, run the test suite (if part of the spec), and walk through their code solution. Along the way, they will field questions from the interviewers. Afterwards, the interviewers canask questions regarding architecture or design decisions, have the candidate implement a later part of the spec (if they did not finish), and / or discuss some of the challenges they faced when building the project.

   **NOTE: Every company that performed this kind of interview did it with *every* candidate, including the interviewers themselves. As such, they often were familiar the details, and it was easy to swap interviewers on short notice.** 
7. The candidate is given a 15 minutes break while the interviewers confer and decide whether or not to keep going. This is probably the most contentious part of the interview: If the candidate did not perform satisfactorily on the programming project or the project review, then the interview would end there and the candidate leaves. If the candidate passes, then they proceed into the final rounds of the interview.
8. The next round(s) could fit any of the 1-hour interview styles we have previously covered in this blog: Behavioral Interviews, System Designs, Pragmatic Practicals, or LeetCode interviews. 

   * System Design interviews are par for the course for senior software engineering interviews -- this is something that a candidate should be familiar with in the course of their everyday work. 
   * Technical Communication Interviews are a flavor of System Design Interviews where the candidate is asked to describe a past project they built in technical detail, discussing the trade-offs, the constraints, the solution, and their involvement with the project
   * It's worth noting that the programming project is an *intense* exercise. While one could do a pragmatic practical or a LeetCode style interview, it would not add more signal and the interviewer expect that a candidates performance would realistically decrease as the day wears on.

## How this type of interview addresses the needs of both parties

#### For candidates:

* It provides the benefits of a take-home while minimizing the downsides. You are given a practical problem that allows you to take advantage of the skills and experience you've gained over time. You're not forced to process everything on the spot -- being given 3 hours means you can spend more than 10 minutes trying to understand everything and plan a solution. Doing the test on-premises means you can ask for clarifications and get a response on the order of minutes, not hours or days. And, the nature of on-site interviews means that you have a constrained time-box to do the project in. No unnecessarily long projects! After the interview, thats it! You don't need spend your valuable personal time at home working on a project.
* You don't need to spin your wheels for weeks or months grinding LeetCode and studying for a test that has very little signal regarding your actual job performance. Instead, you can take advantage of your experiences and skills to make judicious engineering decisions faster, which matter on the job. 

#### For interviewers:

* Companies can save time and effort on interviews because the first half of the day can be handled with minimal involvement by employees. If the interviewers decide that the project and walkthrough is insufficient, the company can decide to end the interview because they would be able to make a more informed decision of the candidate's skills at that point. The interviewers don't need to review the code asynchronously either, unlike take-homes. They ask the candidate to run the test suite, they ask the candidate to demo the app, and they work through the code together. It fits nicely into the slot of 1 interview that would have otherwise be spent doing LeetCode interviews anyway.
* Doing the programming project knocks out the technical portion, allowing the rest of the interviewers to do system design or behavioral interviews -- which matter more as you become more senior in your role and are more relevant. We skip the 3-in-1 LeetCode interviews, and we can dismiss using the *law-of-averages* as a way to select candidates to hire.

## A Sample Programming Project

Here is a slightly modified question I was given from a company.

> Implement a web server link-shortening service, like bit.ly or tinyURL. 

#### Phase 1:

* Your phase 1 deliverables should include a webserver listening on port 5000, and a datastore of your choosing to store the URLs
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

#### Phase 3 ALTERNATE:

* Deploy this on a live server! Your interviewer should have provided you with an Amazon EC2 Instance that you can use as a sandbox. Get the app working on the cloud!

### How to grade this kind of programming project

How do we determine what is a fair, but rigorous question to implement in 3 hours? Make sure all your mid-level and senior engineers can implement Phase 1 in the three hour time period. While the question above looks simple, there are a bunch of gotchas to work through, and doing the setup + project + tests + documentation is already pretty tough. If **everyone** on the team can't get reasonably close to passing Phase I in 3 hours, then your question is too hard. Phase 1 should encapsulate an entire functioning project, where Phase 2 and beyond test refactoring, design, or other aspects of software engineering like deployment and infrastructure. Phase 1 is the meat of what is being evaluated, where Phase 2 onwards are supplementary. Review the candidate's git history for the project to see how they break up the work. 

In one of the instances where I was given this kind of interview, I was only able to barely solve Phase 1 before my time was up. I thought I had failed it. During my one hour review with the interviewers, they had me implement the logic for phase 2 in front of them. Again, I thought I did poorly. At the end of the day, the recruiter told me that I did *really* well on the project. I found it so refreshing to be evaluated by the relative value of each phase. It wasn't a race to implement all the features -- but to pick and choose how to best solve the problem, how to structure your code in a way that would allow you to iterate, but overall, deliver the most important thing to your customer (a complete, demo-able software implementation).

## Final Thoughts

If there is one thing I'd like you to take away, its this: LeetCode interviews aren't inherently *bad,* but we've allowed it to become the end-all, be-all for software engineering interviews, even when it doesn't relate to the work that we are expected to perform as senior engineers. When you swing a hammer, everything looks a nail. As software engineers, we need to evaluate if there are better tools for the job.

- - -

If you got this far, hopefully you agree with some of these ideas I've presented in this article. Thanks for reading! If you have any questions, comments, or suggestions, feel free to tweet me: [@nudgemybody](https://twitter.com/nudgemybody)