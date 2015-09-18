---
layout: post
title: "An Ethical Checklist for Data Science"
author: Alan Fritzler
---

As data scientists, we often get lost in the techniques and methods of our trade. In doing so, we can forget to ask important questions: who will be affected by our work? How we are ensuring that by doing ‘good’ for one group, we are not inadvertently harming another?

Ethical controversies have dominated recent data science headlines (think <a href="http://www.wired.com/2014/06/everything-you-need-to-know-about-facebooks-manipulative-experiment/">Facebook’s emotion manipulation studies</a>, or the <a href="http://www.technologyreview.com/view/519281/cryptographers-have-an-ethics-problem/">NSA surveillance program</a>). Even though these ethical issues are in the news, we often don’t give enough attention to them when they’re in our own work. 

At DSSG, some of our most interesting discussions this past summer centered on the ethical dimensions that underpin the work of data scientists. What emerged from these discussions were a number of key questions that data scientists should ask as they pursue their projects. I’ve summarized these below with the hope that you consider them in your next project.

####Project Selection & Scoping####

<ul>
	<li>Is the problem we are solving the symptom of a greater issue? Sometimes we think we’ve identified a problem only to learn that it cannot be addressed without solving a greater systemic issue. For example, differences in educational attainment across demographic groups in America are driven by many factors, from parenting to poverty to healthcare access.</li>

	<li>Is data science the right tool for the job? Pursuing a data science project can mean pulling resources away from other initiatives that could have a greater impact. Data science can be incredibly powerful, but it requires a lot of pieces to be in place to be successful. It’s important to recognize when this is not the case and resources are better directed elsewhere.</li>
</ul>

####Building the Team####

<img src="/img/posts/ethics1.jpeg">

<ul>
	<li>Does the team include and/or consider individuals and institutions who will ultimately be affected by the tool? A team of graduate students or PhDs is not always representative of the population being studied. For this reason, they should engage members of their target communities and find ways to give them a voice throughout their project, while at the same time familiarizing themselves with their culture and realities.</li>

	<li>Are our team members in it for the right reasons? Are members joining the team to pad their resume or because they truly care about the issue? It’s OK to care about both, but people that are motivated by a greater cause are generally better team players. </li>
</ul>

####Data Collection####

<ul>
	<li>Does collecting data impede on anyone’s privacy? Did the people we are studying give consent to the way their data is being used? Were they given the option to opt out? If such steps were not possible, was the data anonymized and cleansed of personally identifiable information?</li>

	<li>Were the systems and processes used to collect the data biased against any groups? Surveys are a common venue for introducing bias. For example, a question about gender that is limited to male or female responses may inadvertently alienate transgender people. Similarly, a survey sent to non-English speakers may return unreliable responses. </li>
</ul>

####Analysis####

<img src="/img/posts/ethics2.jpeg">

<ul>
	<li>What bias is the team introducing? The variables that are considered for an analysis are subject to selection bias. An experiment is limited by the knowledge of its authors. For this reason, it is critical that the team recognize the limitations of their backgrounds and engage outside experts when possible. </li>

	<li>Should the team include features that could be discriminatory? Features such as race, gender, or income can be highly predictive for certain problems. When this happens, it’s important to think through about why this is happening and what data is missing. Some good examples of this can be seen in the banking industry, where features such as zip code and race have historically had a disproportionate effect on loan access and interest rates for minorities.</li>

	<li>Is the analysis sufficiently transparent? Machine learning models can be opaque, particularly around what variables are driving predictions. This can hinder important discussions within a team or with stakeholders about targeting and intervention strategies. Think back to the last financial crisis. Would things had gotten as bad as they did if the average person knew how mortgage-backed securities and collateralized debt obligations worked? It’s easier to critique a process when you know how the sausage is made.</li>
</ul>

####Implementation####

<ul>
	<li>Are the people using our models aware of its shortcomings? Many people trust models as if they are fact. In reality, all models have some degree of uncertainty. It’s important for end users to be aware and educated of this as they implement these tools.</li>

	<li>What are the consequences of not acting on false negatives (and acting on false positives)? End users have to choose what tradeoffs they are willing to make when implementing a predictive model. They should assess the costs and benefits of various courses of actions. A situation you may have experienced is your bank calling you about abnormal credit card activity, when everything was OK. Your bank likely tuned its fraud detection models to return more false positives than false negatives because the cost of making a few extra calls outweighs the cost of not catching a real instance of fraud.</li>
</ul>

Ethical considerations often get kicked to the sidelines in data science projects. However, if they are not properly incorporated at every stage, it’s possible that the project is not implemented or, even worse, implemented with adverse consequences. By considering some of the questions above, we can improve our chances at delivering projects with truly positive social impact.