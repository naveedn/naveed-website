---
template: post
title: A sane and fair process for conducting Senior Software Engineering interviews
slug: alternative-senior-engineer-interview-process
draft: false
date: 2020-03-10T22:15:40.358Z
description: >-
  Despite the numerous problems, we still use LeetCode style interviews almost
  exclusively in our hiring process. Is there a better way? Read on to find
  out. 
category: interviews
tags:
  - interviewing
  - technical
---
_For those reading, the first half of this essay can be found here: [Part 1: Interviews for Senior Software Engineers are F*cking Broken](https://www.naveed.dev/posts/senior-engineer-interviews-broken)_

# Introducing a new style of Engineering Interviews

From my experiences interviewing, there were a few companies that stand out as having a novel and great interview process. They were short and efficient, thorough and challenging for the senior engineering role. Whats more interesting was that the interviews were structurally very similar to each other, albeit some details are different. Essentially, you try to take the best aspects of both styles of interviewing while minimizing each solutions downfalls. I've adapted some of the common ideas into the format below.

They are only 2 interviews periods. One is an initial phone screen with the recruiter or hiring manager. These conversations would be anywhere from 30-60 minutes, where the company gets a feel for you and whether or not they are interested. This isn't different from most interviews currently, so I'll move on. 

The second interview is where things get interesting: It's a full day on-site assessment, broken out into a few parts. It goes something like this:

1. The candidate arrives, and is brought to a conference room. The recruiter provides the candidate with a written spec for a programming project. After 15 minutes, an engineer steps into the room, and provides any clarifications and answers any question the candidate has.
2. The candidate is then left alone and given 3 hours to implement the spec as best as they can. The test is open-book, open everything. They can use whatever IDE, language, or framework they want. The programming project is composed of multiple logical phases, with the goal being to complete the requirements for one phase before moving onto the next one. Each phase tests a different aspect of the project or becomes more difficult than the previous. *I will provide an example below.*
3. At the 3 hour mark, the candidate zips up their project, and sends it to a predetermined destination.
4. The candidate is given a 30-60 minute lunch break / informal interview, where they can talk to an engineer that currently works at the company and get answers to any questions they may have, while getting some food.  
5. After lunch, 2 interviewers come into the room for a 1 hour interview where the candidate will demo their project, walk through their code solution, and field any questions from the stakeholders. The interviewers can ask questions regarding architecture or design decisions, ask the candidate to implement a later phase, and/or modify some of their code due to a changing scaling requirement.

   **NOTE: Every company that performed this kind of interview did it with *every* candidate, including the interviewers themselves. As such, they often were familiar the details, and it was easy to swap interviewers on short notice.** 
6. The candidate is given a 15 minutes break, where the interviewers confer and decide whether to keep going. This is probably the most contentious part: If the candidate did not perform well satisfactorily on the programming project or the project review, then the interview would end there and the candidate leaves. If the candidate passes, then we jump into the final rounds of the interview.
7. The next round(s) is either a system design or a technical communication interview. System design interviews are par for the course in terms of senior software engineering interviews -- not to mention that this is something that a candidate should be familiar with in the course of their everyday work. Technical Communication Interviews are a flavor of System Design Interviews where the candidate is asked to describe a past project they built in technical detail, discussing the trade-offs, the constraints, the solution, and their involvement with the project. 
8. The day would end with a behavioral interview, where a candidate's culture fit aligns with company values. Pretty standard.

Could one swap out the later interviews with another coding question? Sure. But one thing I've noticed is that doing a 3 hour project is *tiring.* Keeping yourself focused, efficient, and calm for that duration is pretty draining. You have to recognize that your candidates are humans too -- so expect that their interview performance will degrade over time. If you plan on doing coding questions in addition to the project, perhaps do those questions in the morning, saving the afternoon for the project, and making the project slightly easier or smaller in scope. 

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