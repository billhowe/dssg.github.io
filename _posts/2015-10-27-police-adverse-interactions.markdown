---
layout: post
title: "Reducing Adverse Police Interactions"
author: Samuel Carton, Kenneth Joseph, Ayesha Mahmud, Youngsoo Park, Joe Walsh & Lauren Haynes
---

<img src="/img/posts/police-team.png">

Over the past year, the nation has faced a series of highly publicized adverse interactions between the police and the public, from Ferguson to Baltimore to New York. These incidents have had dire and occasionally deadly consequences for individuals and have eroded public trust in the police, making it more difficult for the majority of officers who are upstanding and professional to carry out their duties.

Early intervention can help prevent these kinds of interactions. By getting to officers early, police departments can address risky patterns of behavior such as an over-dependence on force, or risky situations, such as an emotionally compromised officer remaining on shift after a traumatic event, before they bloom into an adverse interaction with potentially catastrophic consequences. 

Over the summer, fellows Samuel Carton, Kenny Joseph, Ayesha Mahmud, and Youngsoo Park, technical mentor Joe Walsh, and project manager Lauren Haynes worked with the Charlotte-Mecklenburg Police Department (CMPD) to improve their existing Early Intervention System (EIS) for flagging officers who may be at high risk of involvement in an adverse interaction.

In [our previous post](http://dssg.uchicago.edu/2015/07/29/police-charlotte.html), we talked about the team’s visit to Charlotte and some of the lessons learned. After our visit, we delved into the data and focused on two main prediction problems:
<ul>
	<li>Which officers are likely to have an adverse interaction in the next two years?</li>
	<li>Which dispatches are likely to end up having an adverse interaction?</li>
</ul>

Our partner’s current system for predicting adverse events is heuristic -- when officers exceed thresholds on certain kinds of events within a prescribed time period, the system sends a warning message to the officers’ supervisors. These supervisors can then prescribe a variety of interventions at their discretion. This sort of threshold model underperforms because it fails to capture the complex nature of behavioral patterns and the context in which these events play out. 

To develop a model that could better address these complexities, we looked at a large amount of data from CMPD on their everyday operations, such as arrests and traffic stops made or dispatches responded to. We also utilized their personnel and Internal Affairs (IA) data. Our efforts included a thorough anonymization of the data to ensure that it retained no personal information about officers. The following timeline displays all the data that we incorporated into our models, along with the number of records and starting times for each type of data.

<img src="/img/posts/police1.png">

One of our major challenges this summer was determining what actually counts as an “adverse interaction.” We used IA investigations to determine which events should be considered adverse. The IA must investigate every time an officer uses force, is involved in a vehicle accident, takes part in a pursuit, violates a rule of conduct, sustains an injury, or faces a complaint from a citizen or another officer. 

Investigations result in different types of dispositions on these incidents: complaints can be deemed sustained; accidents and injuries can be deemed preventable; and all other incidents can be deemed unjustified. We defined an adverse interaction as any event deemed by IA investigators to be unjustified, preventable, or sustained. The only exceptions we made were for a number of internal complaints that we considered less egregious (such as violations of rules regarding sick leave) as well as traffic accidents (most of which were minor).

There are two important caveats to this definition of an adverse interaction. First, different types of adverse interactions may have different predictive features. This may end up “confusing” a predictive model. Second, and perhaps more importantly, the model we built relied on IA receiving reports for all incidents of note and that they make correct and unbiased judgements. While we believe the CMPD’s commitment to transparency allowed us to rely on their IA data, this reliance leaves the model open to the regurgitation of systemic biases if applied to data from other departments where such issues exist.

<img src="/img/posts/police2.png">

These complications aside, adverse interactions as we defined them are rare. Between 2005 and 2015, the CMPD had, on average, 1250 active officers. On average, fewer than one in four officers were involved in an adverse event. Further, contrary to what recent media reports might suggest, the majority of adverse incidents are preventable accidents or officer injuries. 

The goal of the officer-level prediction problem was to flag as many of the officers who go on to have adverse interactions while flagging as few officers who do not. Flagging officers unnecessarily wastes time and money and may harm morale. 

With this target defined, we generated a set of predictors from the available data. These included officer-level predictors such as recent arrest count, past IA violations, and years of experience, as well as neighborhood-level predictors such as mean income level. In total, we had about 300 predictors for our models.

Using relatively straightforward tools from the machine-learning toolkit, we achieved significant improvements both in flagging officers who have adverse interactions and not flagging the rest over the existing system.

<img src="/img/posts/police3.png">

Here we show a representation of CMPD, with red dots representing the portion of officers who will have some type of adverse interaction in a typical two-year period. Grey dots represent the fraction of officers who will not. Each dot represents about sixty officers. The “perfect” model, shown at the bottom of the figure, would flag only those officers who will go on to have these types of interactions. In reality, this is a difficult thing to do. The current EIS captures many more low-risk officers than high-risk ones. As the figure shows, our models can flag more high-risk officers (75 more than the current system) while flagging fewer low-risk officers (180 fewer than the current system).

Our event-level prediction problem has also given us insight into the types of situation where adverse events are most likely to occur. Preliminary results suggest that adverse incidents are most likely to occur in urgent, high-pressure situations. Factors such as dispatch priority, dispatch type, and travel time are by far the most predictive of whether a particular dispatch will end in an adverse event. CMPD, and potentially other police departments, could use this information to change dispatch procedures to minimize high-risk situations.

Although DSSG 2015 is over, this project continues. Our efforts this summer laid the groundwork for continued Early Intervention System improvements. DSSG’s parent organization, The [Center for Data Science and Public Policy](http://dsapp.org), has used our code and preliminary findings to search for new predictors, increase EIS accuracy, understand the models’ sensitivity to assumptions, incorporate data from other departments, and work toward implementing the system.

