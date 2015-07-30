---
layout: post
title: "Police Project: Lessons From Charlotte"
author: Kenny Joseph, Ayesha Mahmud & Joe Walsh
---

<img src="/img/posts/police-team.png">

Police departments around the country have been in the spotlight recently because of several [controversial, high-profile incidents](http://news.yahoo.com/high-profile-us-police-killings-black-suspects-184217237.html). Tragic events in Ferguson, New York City, Baltimore, and elsewhere have highlighted the need for police departments to better address the issue of adverse interactions between the police and the public. Many police departments are working hard to avoid these negative interactions with new [technologies](http://www.usatoday.com/story/news/nation/2014/10/11/police-body-cameras-ferguson-privacy-concerns/16587679/) and [tactics](https://www.bostonglobe.com/news/nation/2014/11/29/after-ferguson-some-push-for-more-escalation-police-training/HtXM7gUmKYT9Fx1Qwd8PxL/story.html), while others are leading new [data collection](http://www.claimsjournal.com/news/east/2015/07/16/264559.htm) efforts. 

This summer, as part of the White House [Police Data Initiative](https://www.whitehouse.gov/blog/2015/05/18/launching-police-data-initiative), fellows Sam Carton, Kenny Joseph, Ayesha Mahmud, and Youngsoo Park, technical mentor Joe Walsh, and project manager Lauren Haynes are working with the Charlotte-Mecklenburg Police Department (CMPD) on a novel approach: using data science to improve the department’s Early Intervention System (EIS)  for flagging officers who may be at a high risk for being involved in an adverse interaction. 

CMPD’s current system uses thresholds, such as 3 uses of force in 90 days, to flag officers for supervisor review. Our goal this summer is to increase the accuracy of CMPD’s EIS by using predictive models that take into account an officer’s past behavior pattern and other contextual factors. 

<img src="/img/partners/cmpd.jpg">

We visited CMPD a couple weeks ago to learn more about the department, their data collection efforts, and their EIS. In two whirlwind days, we met with department leadership, spoke with Internal Affairs, sat with a group of officers who volunteered to provide expert advice and feedback, and rode with patrol officers. Here are some of the things we learned:

*Context matters.* Almost everyone we talked to at CMPD pointed out that one of the major shortcomings of their Early Intervention System is that it fails to take into account contextual factors, such as where an officer works, the officer’s shift, the time of day or whether or not the officer is on a specialized unit. Our hope is that by taking these factors into account, our predictions will be more accurate than the current system. 

*Police are human beings and policing is an extremely difficult job.* Police officers routinely have to make split-second, life-altering decisions. Our data show that the vast majority of police-public interactions end peacefully and that adverse interactions are rare events. Yet, as in every profession, mistakes happen. 

During our meetings, police officers at CMPD shared anecdotes about factors that may cause officers to make mistakes on the job, such as problems in their personal lives, insufficient training, repeated exposure to stressful events, or burnout. We will attempt to incorporate this unobserved officer “stress” in our model by including data such as number of secondary employment hours or overtime worked and exposure to potentially stressful events such as domestic-violence cases. 

*Data can only tell part of the story, but it can definitely help.* During our ride-alongs, we saw firsthand how officers in the field enter data into the system. Every time an officer makes a traffic stop, responds to a 911 call, or interacts with the public, they are required to enter information about the event into CMPD’s database. 

It quickly became evident that it would be impossible to capture all the details and nuances of police-public interactions. The officers we rode with spent a large chunk of their time simply talking with, listening to, and helping out the people they encountered during the course of their daily work -- little of which is captured by the data. This is important to keep in mind not just to understand the limitations of our models but also to make recommendations to CMPD and potentially other police departments about what data to collect in the future.

<img src="/img/posts/charlotte-mecklenburg.png">

We’re using these insights as we enter the last stretch of the fellowship. In addition to new predictors, this visit helps us better interpret the models. 

While the problem we’re trying to solve differs substantively from other DSSG projects, the basic approach to solving it does not. In 2014, a DSSG team partnered with Montgomery County Public Schools to predict whether students would [drop out of school](http://dssg.uchicago.edu/2000/02/02/org-mcps.html); their tool uses administrative data to identify why individual students are at risk of dropping out before those students are off track. The same year, another team used historical blood tests, patient demographic information, building data from the City of Chicago, and neighborhood information from the U.S. Census to flag children for monitoring and their homes for inspection before they get [lead poisoning](http://dssg.uchicago.edu/2000/02/03/org-cdph.html). Similarly, the police team is using administrative and other data to build interpretable models that predict bad outcomes early enough that intervention can still work.  

Our visit to CMPD gave us an immense appreciation for the extremely difficult job that police officers face every day. Throughout our visit, we saw many examples of good policing, a job that includes aiding the mentally ill, protecting children from abuse, and making our communities a safe place to live. While there certainly exist events, officers, and even departments within which bad policing and bad practices are routine, there are also individuals, like those we met at CMPD, who are working hard to serve the public and proactively identify and remedy potential issues. We hope our efforts this summer can help CMPD increase the efficiency of resources and time used for supporting officers, with the ultimate goal of reducing adverse police-public interactions. 


