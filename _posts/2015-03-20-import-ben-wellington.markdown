---
layout: post
title: "Import: Safe Hallways, Successful Tests"
author: Ben Wellington
---

<i>Import is a new series of guest posts from friends, colleagues, and collaborators in the data science for social good community. This post is by <a href="https://about.me/benwellington">Ben Wellington</a>, who writes the open data blog <a href="http://iquantny.tumblr.com/">I Quant NYC</a></i>

Every year, New York City public schools conduct an in-depth survey of their parents, students and teachers. According to the Department of Education, the survey, one of the largest of any kind in the nation, “helps school leaders understand what key members of the school community say about the learning environment at each school.” 

People’s perceptions are inherently difficult to quantify, but the survey covers topics including Academic Expectations (e.g. asking if teachers “expect students to work hard”) and Safety and Respect (e.g. asking if students feel “safe in the hallways, bathrooms, locker rooms and cafeteria”). 

So are people’s perceptions related to other more common measures of academic success, such as test scores? With the help of <a href="https://nycopendata.socrata.com/">New York City’s Open Data platform</a>, I was able to have a look for myself.

<img src="/img/posts/nycschools1.png">

One might expect that Academic Expectation scores would be the most closely correlated to test scores. But what I found was rather surprising: Safety and Respect scores, are actually more highly correlated with test scores than Academic Expectations scores are. In other words, the more safe and respectful a school feels in New York City, the higher its test scores will be on average.   

This takeaway was revealing, since Safety and Respect might seem more attenuated from academic performance than Academic Expectations.  Yet for all three groups surveyed -- parents, students and teachers -- the correlation between test scores and safety was stronger than how “academic” a school feels. This relationship also held true both for elementary school state tests and high school SAT scores.    

At first, I wondered how much this had to do with income. It’s well known that schools in higher income neighborhoods tend to test better than their counterparts in less affluent areas -- our data shows that effect quite strongly in elementary school but less so for high schools. This lower high school correlation is likely due to the fact that while elementary school students typically go to their locally-zoned school, many high school students travel well outside of their neighborhood to get to school, so a high school’s population may be less representative of the surrounding neighborhood.  

So might the “safety” effect we see just be related to income? Surprisingly, no.  The data shows that the Safety and Respect scores are only weakly correlated with a neighborhood’s median income. This tells us that these safety scores are picking up on an important aspect of school performance that’s largely independent from income. 

Another interesting aspect of the Safety and Respect scores is that out of the three groups, parents’ perceptions of safety seem to be the least predictive of test scores.   This is true in elementary school and especially true in high school, where the perceptions of parents have almost no correlation with test results.  

This is not hard to imagine given my recollection of a typical teenager/parent relationship. High School students are much less communicative with their parents than elementary school students are, and so parents might have a harder time gauging high schools accurately. Teacher Safety and Respect responses seem to have the highest correlation with test scores among the three, which makes sense given they are the boots on the ground in our classrooms.  Lastly, students fall right in between the two.

Parents also seem to be biased by school size, perceiving larger high schools to be less safe (as measured by incoming class size or “Cohort Size”). But it turns out that larger schools actually have higher average SAT scores, so parents’ fears may not be well substantiated. Unfortunately, I couldn’t measure the rate of violence in schools directly as data on suspensions involving acts of violence in schools is not yet present on the NYC Open Data portal, so we’ll have to leave that for future work.

The numbers make it clear that perceptions of safety in our city’s public schools warrant special attention. By mapping student’s Safety and Respect scores at schools across New York City, it’s clear that school safety is an issue in all five boroughs (Darker colors indicate schools where students feel less Safety and Respect, and lighter colors indicate the opposite.)

<img src="/img/posts/nycschools2.png">

The map shows some hotspots, with one particularly low-scoring cluster in Springfield Gardens on the East Side of Queens. This neighborhood has median income rates in line with the Queens borough average, but the school Safety and Respect scores from students are stubbornly low, with many of the schools in that area falling below 6 on a 1-10 scale. The histogram below shows that these scores are quite low compared to the citywide median of 7.2.

<img src="/img/posts/nycschools3.png">

<img src="/img/posts/nycschools4.png">

Now before jumping to any conclusions on safety and its relationship to school performance, it’s important to note a few caveats. First, this analysis does not prove causation -- we don’t know if it is the perception of safety that is causing changes in test scores or some other related factor.   

Furthermore, due to limitations in the availability of open data, this analysis draws from data sets that are few years apart. These constraints are sure to decrease as our open data movement grows more robust. 

Lastly, and perhaps most importantly, measures of academic performance like the New York State test scores and SAT scores may not be a true reflection of a school’s success. Consider that for SAT scores, only a segment of the student population actually takes the SATs.  Moreover, there has been extensive analysis and discussion about the value of test scores in academic assessments -- a topic far larger than this blog post, but indeed worth mentioning 

So with those caveats in mind, what did NYC Open Data reveal?  Policy makers and the public alike should take a close look at perceptions of school safety.  Intuitively, the findings here make sense -- a student that feels comfortable walking down the hallways of his or her school is going to be better able to focus on learning. But I wouldn’t have expected that safety would be such a strong predictor of test score outcomes, relative to other, more academically-focused areas in the survey.   And that’s the beauty of Open Data -- helping us to learn about our city in new and exciting ways, one dataset at a time.

<b>Data Sources</b>
<ul>
	<li><a href="https://data.cityofnewyork.us/Education/NYC-School-Survey/kwk4-6u9e">Survey Data</a></li>
	<li><a href="https://data.cityofnewyork.us/Education/Graduation-Outcomes-Classes-Of-2005-2010-School-Le/vh2h-md7a">Graduation Rates</a></li>
	<li>New York State Test Scores (<a href="https://data.cityofnewyork.us/Education/Math-Test-Results-2006-2012-Citywide-SWD/ufu7-zp25">Math</a>) (<a href="https://data.cityofnewyork.us/Education/English-Language-Arts-ELA-Test-Results-2006-2012-S/phth-xf25">English</a>)</li>
	<li><a href="https://data.cityofnewyork.us/Education/SAT-Results/f9bf-2cp4">SAT Scores</a></li>
	<li><a href="https://data.cityofnewyork.us/Education/School-Point-Locations/jfju-ynrr">School Locations</a></li>
</ul>

