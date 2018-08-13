# Formal Inspections

*Fagan Inspections* are a formal peer review process created in the mid 1970's  (https://en.wikipedia.org/wiki/Fagan_inspection, http://www.mfagan.com/pdfs/aisi1986.pdf). These types of inspections were promoted by the Software Engineering Institute's (SEI) Capability Maturity Model (CMM) as a key process area that demonstrated maturity at SEI Level 3 (a minimum threshold for many software contracts). 

A good description of the practice can be found here  "Key Practices of the Capability Maturity Model", peer review pages L3-97 - L3-104
[https://resources.sei.cmu.edu/asset_files/TechnicalReport/1993_005_001_16214.pdf](https://resources.sei.cmu.edu/asset_files/TechnicalReport/1993_005_001_16214.pdf)
[http://people.cs.ksu.edu/~dwyer/courses/748/resources/cmm-tr25/tr25_l3g.html](http://people.cs.ksu.edu/~dwyer/courses/748/resources/cmm-tr25/tr25_l3g.html) (web)

Some of the highlights from the SEI CMM peer review recommendations are:
- Adequate resources and funding are provided for performing peer reviews on each software work product to be reviewed.
- Peer review leaders receive required training in how to lead peer reviews.
- Reviewers who participate in peer reviews receive required training in the objectives, principles, and methods of peer reviews.
- Peer reviews are planned, and the plans are documented.
- Peer reviews are performed according to a documented procedure.
- Data on the conduct and results of the peer reviews are recorded.
- Measurements are made and used determine the status of the peer review activities.
- The software quality assurance group reviews and/or audits the activities and work products for peer reviews and reports the results.

There are different roles for the participants of a Fagan Inspection. Below is a summary of each:
Author 
The author is responsible for creating the work product to be reviewed. The author attends the inspection to answer questions and to clarify their work. 

## Moderator
The moderator organizes and manages the entire review process. Participants in a review should not be evaluated by members of the review team who happen to be managers.

## Reader
The reader reads the work product aloud during an inspection

## Recorder
The recorder communicates the defects discovered during the inspection to the author with a review log. This information is provided to the author after the inspection so that they can revise their work. The recorder records information like the filename(s) where a defect is found, the line number(s), the severity of the defect, and a concise summary of the defect so that the author will know what to address. 

In addition, the recorder records data about the reviewers preparation time, the size of the work product, and the length of the inspection. All of this data can be analyzed by the organization to evaluate the effectiveness of the review and the team. Some data that can be collected and monitored over time are:
- Average time spent by reviewers to prepare for the inspection
- Average number of lines of code inspected per hour
- Average number of defects per line of code
- Average number defects found per hour

## Reviewer
A reviewer is responsible for understanding the work product and identifying defects in it. Reviewers bring these issues up during the inspection and a discussion typically ensues about whether the issue is really a defect and what is its severity. 

All of the previously mentioned roles are also reviewers. For example, the author may discover faults in their own code during the inspection. They are permitted to identify them since they are a reviewer also.


There are different phases in a Fagan Inspection. Below is a summary of each:

## Planning and Overview
In this phase the author and moderator must coordinate to find an acceptable meeting place and time to have the inspection. Potential peer reviewers are recruited based on their availability. After the review group has been identified the author shares the work product being reviewed. The inspection must be scheduled far enough in the future so that all of the reviewers have enough time to review and markup their copies of the work product.

## Preparation
In this phase, the reviewers read the code and identify defects in it. This is likely the most important phase in a review. Typically, reviewers will mark up a copy of the work product and bring the copy to the inspection. 

The reviewers are making judgements about the quality of the work product. In addition to code, other work products can be reviewed (requirements and design documents, for example). If the work product in the inspection is code then the reviewers have to make judgements about it. Boehm [Characteristics of Software Quality (TRW series of software technology) June, 1978 Barry W. Boehm] has identified several attributes for describing quality in a software product. Reviewer comments typically address one of these issues:
- Intrinsic code quality
- Freedom from problems in operation
- Usability
- Installability
- Documentation for intended users
- Portability
- Maintainability and extendibility
- Fitness for use (implicit conventional user needs are satisfied)

This phase is where developers get to use their judgement and experience to identify potential issues with the code.

Reviewers are asked to track the amount of time spent reviewing the code. This metric can be used to evaluate the effectiveness of the review and the software development team. 

## Inspection
In the inspection, the reviewers meet synchronously face-to-face (or using some virtual meeting technology) to go over the work product. The reader reads each line of code aloud. If a reviewer has identified a potential issue they will interrupt the reader after the line is read. 

When this happens the reviewer may pose a question to the author or author may clarify a misconception that the reviewer has. It is not uncommon for the group to have a discussion about the issue. A great deal of knowledge can be spread among the team members as a result of these discussions. Ultimately, though, it is the moderator who decides whether the issue should be marked as a defect and at what severity level. The recorder must record the relevant information in the review log.

It is important to note that the inspection is not the place to fix defects. Defects are identified and recorded during the inspection and it is expected that the author will revise the work product to address them.  It is not uncommon, however, to have a group discussion about potential ways to fix the problem. This is one of the advantages to committing so many resources (experienced developers) to a review. Having said that, often the moderator will suggest that the author meets with one or more reviewers offline to have a more in depth discussion.

Inspection meetings should be limited to a maximum of two hours per day. The quality of review comments drops the longer the inspection meeting. If a work product can't be reviewed in two hours then additional meetings need to be scheduled to complete it. 

## Rework
In this phase the author is given the review log with the defect information in it and they must address each recorded defect. The author may consult with one or more of the reviewers to get some follow up information and suggestions. After the author completes the revisions they will hand the work back to the moderator for the follow up phase.

## Follow Up
In this phase, the moderator ensures that the author adequately addressed every recorded defect. If the author makes major changes to the work product the moderator might request another review of the new work product. Otherwise, the moderator will give the go ahead to release the work product if they feel that the defects were addressed adequately by the author.
