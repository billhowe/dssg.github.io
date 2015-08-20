---
layout: post
title: "Blight Prevention: Building Strong and Healthy Neighborhoods in Cincinnati"
author: Jennifer Helsby, Talia Kaufmann, Katharina Rasch
---

<img src="/img/posts/cincinnati.png">

Many cities are working to prevent the negative impacts of vacant buildings caused by population loss.  Cincinnati is one such city, with a more than 40% reduction in population since 1950 and a large stock of historic buildings. This effect coupled with the housing crisis of 2008 has produced new challenges in Cincinnati and many other cities across the country. Homes that are foreclosed and/or neglected tend to fall into disrepair and cause property values to decline, and can eventually result in home abandonment and vacancy. This effect is like a disease: if left untreated, it spreads from one home to others in the neighborhood. 

Currently, the City of Cincinnati’s Department of Buildings & Inspections attempts to address this problem via building inspections and code enforcement. Building inspectors respond to citizen complaints and then work with property owners to bring their building(s) into compliance with regulations. However, under the current process, for homes that will one day become vacated, the Department of Buildings & Inspection only receives a complaint in approximately 25% of cases. 

During the Eric and Wendy Schmidt Data Science for Social Good Fellowship 2015, fellows Jennifer Helsby, Talia Kaufmann and Katharina Rasch, technical mentor Eric Rozier, and project manager Paul van der Boor are working with the City of Cincinnati's Chief Performance Officer and building inspections department to develop an early detection process to identify buildings at risk of decline using data science tools. This will enable the City to attend to at-risk properties before the phenomena spreads to nearby homes and adversely affects the quality of life in some neighborhoods.

Considering that 2,300 of the 150,000 properties in Cincinnati are vacated, a system for early intervention could have a significant impact, enabling inspectors to become aware of troubled buildings earlier in the process. When we visited the City of Cincinnati, we found that the main role of the building inspectors in Cincinnati is to educate property owners about the responsibilities of homeownership and work with them to bring homes into compliance with the building codes. For example, an inspector may provide the owner with information about programs that help low income people receive assistance with home repairs. Early intervention systems will allow building inspectors to start working with property owners earlier, thus preventing abandonment. 

<img src="/img/posts/cincy-figure1.png">

Since the City has no systematic way of identifying troubled homes before they fall into serious disrepair and become vacated, we are developing a series of predictive models that will help the City in their building enforcement process. Using data about home values, fire, crime, tax, census and water shutoff information together with historical inspections data, we can learn which aspects of the data are predictive of property decline. We can use those early signs to reprioritize the list of inspections for homes in Cincinnati, allowing the City to focus their attention on the properties that are most at risk of falling into disrepair.

Our inspection priority is constructed from three predictive models: a risk model, "P(violation)," describing the likelihood that a building inspector will find a problem with a home; a cost model, "Effort," predicting the number of inspector visits it will take before a home can be brought into compliance, and a compliance model, "P(compliance)," that will predict the probability that a home can actually be brought into compliance.

Currently, property inspections are triggered by citizen complaints and inspectors find a violation in 53% of cases. Based on initial results from our risk model, we are able to triage complaints and increase the chance of finding a building code violation to 78%.

<img src="/img/posts/cincy-figure2.png">

These models, along with a prototype dashboard, will be delivered to the City at the end of the summer. This tool is intended to be used by inspectors to guide their work to areas of the city predicted to be most at risk of building code violations. Through the use of predictive tools, the enforcement response process becomes proactive instead of reactive. 

All of our tools and code will be made available on Github. We anticipate that similar approaches could be useful for other cities struggling with the decline of urban buildings and hope that what we build this summer can be adopted by other local governments. With data science methods, cities can optimize the use of their resources to build and maintain safe, strong, and healthy neighborhoods.



