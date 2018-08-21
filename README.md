# Overview
*Peer review* (or *code review*) is a technique where developers ask their peers to identify defects in their code before releasing it. There are different types of reviews ranging from very formal and heavyweight to less formal and lightweight. More formal reviews are a source of data that can be used to measure the effectiveness of a software organization.

Peer review relies on human judgement and experience to identify defects in code. It is a manual form of static analysis. In most variations of peer review, defects are identified and reported back to the author of the code. The peer review is not intended to be a venue for fixing defects. The author is expected to fix the work product based on the feedback from review.

Formal peer reviews, like Fagan Inspections, are considered somewhat expensive due to the coordination required and the number of face-to-face person-hours required to perform them. However, they are very effective with an average defect removal rate of 65% [Capers Jones]. 

There is an added educational benefit to these formal reviews. Less experienced developers get to hear how more experienced developers think about code and they are able to participate in discussions with them about it. 

Less formal reviews, sometimes called desk reviews, are ones where one or two peer developers read the code independently and then provide feedback to the author. These are typically less expensive but may also be less effective. 

The Agile development practice of pair programming is intended to be a ‘preemptive code review’. If having peers review the code after it is written is considered a good practice, the thinking goes, then why not have a peer next to the author as they are writing it?  

# Level
- Introductory

# Student Learning Outcomes
- After reading a peer's code, the student will be able to discover faults in it and communicate those faults to the team.
- Students will be able to communicate the faults in a way that is clear and concise. They will do so in a way that shows sensitivity and compassion.
- Students will be able to revise their code based on feedback from a review.


# Why Learn About Peer Review?
- The software produced by a team performing code reviews is of a markedly higher quality.
- Members of a team performing code reviews will become acquainted with more of the system. - The knowledge of each others work will grow as a result of being exposed to code written by other members of the team.
- Developers are often asked to write more code than they read. Being exposed to other people's code offers a valuable learning experience. 
- Developers learn how to critique a colleague's work.
- Developers learn how to take constructive criticism.

# Core Tenants of Code Review
Code review isn't like grading a programming assignment. The goal is not to *evaluate*, the goal is to *communicate* in both directions. The author is sharing, "this is the way I think this should be done." The author contributes a concrete implementation of a design, or a concrete solution to some problem. The reviewer is learning that approach.

The person whose code you are reviewing is your teammate, your peer, and very likely someone that will review your code someday soon. Code review is about communication, and ensuring that code that gets checked in is clear, correct, and understandable for the whole team - it's part of a process that leads to better team efficiency and long term velocity.

The reviewer is considering whether the big picture is clear. The author may not be part of the team in the future so the review has to answer whether the average person on the team be able to understand this design/feature/etc?

Simultaneously, the reviewer is usually also communicating about alternatives. Hopefully the team has already discussed and decided on the big picture design. The details, the way the code is written, the nuts and bolts, often represent a chance for the reviewer to learn new tricks AND to suggest clearer/more efficient/more common ways to do the same thing.

# Risks and Bias
The best way to kill team velocity? Fight about unimportant things, upset your teammates, be a jerk, let tempers flare.

It is critical that code reviewers remember that they are having a conversation, or at most providing a teaching lesson. Code review isn't a fight: if you are rude or abusive you can quickly do a lot of damage to team culture and morale.

Bias??
