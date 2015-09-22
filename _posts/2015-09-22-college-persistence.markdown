---
layout: post
title: "College Persistence: Helping Students Beyond High School Graduation"
author: Benedict Kuester, Michael Stepner, Masha Westerlund
---

<img src="/img/posts/college-team.png">

A college education is one of the keys to economic security and prosperity in the United States.  Bachelor’s degree holders earn nearly twice as much as high school graduates, enjoy better health and hold jobs that offer a greater sense of accomplishment, independence, creativity, and social interaction (Oreopoulos and Petronijevic 2013).  But there are large gaps in college completion: fewer than 15% of students in the lowest quartile of socioeconomic status earn a bachelor’s degree, compared to 60% of students in the highest quartile. There are wider disparities in college completion than college enrollment; too many students begin a college degree but never complete it (NCES 2015).

<img src="/img/posts/persistence-graph.png">
*Source: Mortenson, Tom. “Bachelor’s Degree Attainment by Age 24 by Family Income Quartiles, 1970 to 2011.” http://www.postsecondary.org.*

Though dropping out of college is a life-changing decision, it often starts with small, preventable events: missing the deadline to request financial aid, or failing to register for the right courses on time. We spent the summer working with four charter networks, the [Noble Network of Charter Schools](http://noblenetwork.org/), [KIPP Chicago](http://www.kippchicago.org/), [KIPP New Jersey](http://kippnj.org/), and [Perspectives Charter Schools](http://www.pcsedu.org/), who are well aware of the challenges facing their alumni as they progress through college. 

Many charter schools support their students through alumni counselors who keep in touch with students, giving them support and practical advice to help them succeed in college. But all schools have limited resources, and counselors cannot be in touch with all students at all times. 

To have the largest possible impact, counselors need to identify and reach out to the alumni who need the most assistance in persisting through their college degree program. Alumni counselors currently rely on instinct and their personal knowledge of alumni to determine who to call when. With only a handful of students this approach may be manageable, but as cohort sizes increase, it quickly becomes difficult to efficiently prioritize resources. As a result, struggling students may fall through the cracks.

We spent the summer working with our partners to help them identify which of their alumni are most at risk of not completing college, to make sure that their counselors have the information they need to reach out to struggling students. We used students’ high school records and alumni contact records to build statistical models that predict which students are at risk of not completing college. These anonymized records provided us with demographic information on students, various measures of students’ academic performance in high school, such as GPA, courses taken, and standardized test scores, and behavioral performance such as attendance records and disciplinary events.

Because alumni counselors need to know who to call in the next days and weeks, we generated a series of models that each predict persistence for the upcoming semester. That is, each model predicts the odds of persisting N+1 semesters at a college, conditional on having persisted N semesters at that college. This provides counselors with timely, up-to-date information about students at all stages of their college degrees. 

<img src="/img/posts/persistence-stairs.png">
*Multiple models predict persistence at every step of a student’s progression through college, from enrollment to graduation.*

We built a data analysis pipeline that combined the diverse data provided to us by our partners into a common database schema. From the data, we generated features that characterize each student’s individual high school experience, such as the number of days they were absent every year, their scores on standardized tests, and the colleges they applied to and enrolled in. We used these features to fit models on data from earlier years, and we then evaluated the predictions of these models on later years. This temporal cross-validation procedure allows us to estimate how successfully our models will perform in the future.

<img src="/img/posts/persistence-pipeline.png">
*Overview of our pipeline*

Our work this summer taught us that simple models, such as a model using high school GPA features alone, or a model that only takes into account features of the college a student is attending, are relatively successful at predicting college persistence. Among the 10% of students predicted to be *least* likely to persist by these models, 60% do in fact not persist for their third semester -- double the base rate among all students, which is 30%. Various models with larger sets of features perform similarly, indicating that including more aspects of a student’s high school experience does not add significant predictive power. The lack of added predictive power is in part because many features are correlated -- for example, a student who misses many high school classes will tend to also have a lower GPA (though we don’t know whether the two are causally linked). 

<img src="/img/posts/persistence-models.png">
*Area under the receiver operating characteristic curve (AUC) for models with different subsets of features. This metric is useful because it accounts for class imbalance and gives a good overall sense of the predictive performance of a model. Error bars represent bootstrapped 95% confidence intervals.*

These results show us that using high school records alone, a simple benchmark such as high school GPA can provide counselors with informative risk scores. But we know that there’s a lot more to a student’s college experience than their high school grades or the college they choose to go to. Fortunately, alumni counselors, who take care to talk to every student regularly, know much more about a student’s academic performance and their social integration in college. 

This information could be an invaluable resource towards building better predictive models. For example, an alumni counselor who learns that a student is feeling overwhelmed by their course load could record that information, which might then prioritize that student more highly at the beginning of the next semester, when course registration is beginning. We believe that by working with alumni counselors to keep track of every student’s college experience, we could build models that are more successful at identifying at-risk students. This in turn will allow counselors to provide timely and effective support. Improving these outreach efforts is a crucial first step in ensuring that every student in the United States has the tools that they need to graduate college. 



