---
layout: post
title: "World Bank Integrity Vice Presidency Project: Kickstarting Data Science"
author: Emily Grace, Ankit Rai, Elissa Redmiles
---

<img src="/img/posts/worldbank15.png">

Are you hearing a lot of data-themed buzzwords lately? Are you wondering whether the use of data science can help a project on which you are working?

Using data makes it easy to prove the efficacy of a project and inform your decisions. More simply, data science is the process of taking all the data you have lying around and turning it into actions. 

**Who are we?** We're a team of three Eric and Wendy Schmidt Data Science for Social Good fellows at the University of Chicago. This summer, we're spending 14 weeks helping the [World Bank Integrity Vice Presidency (INT)](http://web.worldbank.org/WBSITE/EXTERNAL/EXTABOUTUS/ORGANIZATION/ORGUNITS/EXTDOII/0,,contentMDK:20542001~pagePK:64168427~piPK:64168435~theSitePK:588921,00.html) use data to detect collusion, corruption and fraud in development projects. We’ll use examples from our work so far with INT to demonstrate the important steps needed to assemble an effective data science project.

Even if you are not a data scientist, you are probably wondering about the tools and approaches needed to start using data science. Below, we outline four steps (and how-tos) for getting started with data science. 

####Step 1: Set A Goal

Like any other project, setting a goal is key for data science projects. 

Your goals may vary. As a project manager, what are you hoping to accomplish by looking at your data? Do you want to showcase the impact of your project to funding partners? Do you need to decide what to do next? Do you want to improve existing practices?

The World Bank Group provides loans to developing countries so that they can finance investments in infrastructure, health, and environment sectors while boosting economic and social opportunity for the poor. While managing these loans, client countries post RFPs (requests for proposals), to solicit and receive bids from contractors. 

Occasionally, during the bidding and billing process, companies may engage in corrupt behavior. Misconduct is revealed via whistleblowers’ complaints and/or the proactive work of contract supervisors and investigators that identify red flags. With the help of the Eric & Wendy Schmidt Data Science for Social Good Summer Fellows, the Group would like to take a more data-driven approach to achieve two goals:
<ul>
	<li>Develop a methodology to prioritize complaints filed by whistleblowers based on data science applied to historical records of past World Bank-financed contracts and investigation outcomes.</li>
	<li>Support the proactive work by World Bank staff in identifying red flags in high risk projects</li>
</ul>

In order to begin working towards these kinds of goals, a data science team will first examine the current processes and get a clear picture of the data landscape. For example, how many contracts are typically awarded, or how are the contract amounts are distributed (that is, how many contracts are awarded for $100,000, how many for $200,000, etc.)? Further, do the amounts and numbers of contracts vary based on geographic location? What are the salient data features of successful investigations? 

<img src="/img/posts/wbint1.png">
*Image 1: Number of Contracts in Each Amount Range ($0-$50,000; $50,001-$100,000, etc.)
[Created with Tableau]. Source: World Bank Group Open Finances Data*

<img src="/img/posts/wbint2.png">
*Image 2: Heat Map of Contracts Awarded To A Given Country. [Created with Python (Pandas and MatplotLib)] Source: World Bank Group Open Finances Data*

####Step 2: Compile Your Resources

To start a data science project, take a look at what resources you already have available. What data do you have? Do you have access to spreadsheets, databases, case management or Sales Force systems? All of these are good sources of data!

Do you know an IT-professional or computer scientist? Someone with programming or technical skills can be a great resource as you start looking at your data. Keep in mind that you just need a few resources to get started with data science.

Here are some examples of resources that you might be able to find:

**Open Data**
<ul>
<li>An Excel file or API with information about your project</li>
<ul>
	<li>Example: A list of all the contracts awarded by the World Bank since 2000</li>
</ul>
</ul>

**Corporate or proprietary data**
<ul>
<li>A case management system with data relevant to your project</li>
<ul>
	<li>Example: A file exported from the case management system which contains a list of all the World Bank investigations since 2000</li>
</ul>
</ul>

**People**<br>
(You only need one person - yourself - to start your project, but this list suggests folks who might be good teammates or helpful resources)
<ul>
	<li>Someone who is familiar with the data and the subject matter</li>
	<ul>
		<li>Example: A World Bank investigator and anti-corruption specialist</li>
	</ul>
	<li>Someone who knows programming or is tech-savvy</li>
	<ul>
		<li>Example: A Data Science for Social Good fellow who studies computer science or physics</li>
	</ul>
	<li>Someone who knows statistics</li>
	<ul>
		<li>Example: Someone who studied psychology, epidemiology, business or statistics in college</li>
	</ul>
</ul>

**Software**
<ul>
	<li>You can use Tableau (www.tableau.com) to visualize and analyze your data without any programming!</li>
	<ul>
		<li>Are you a member of an educational organization or still in school? You may <a href="http://www.tableau.com/academic">qualify for a free Tableau license</a></li>
		<li>Otherwise, you can try Tableau for free and then consider purchasing</li>
	</ul>
	<li>The Eric and Wendy Schmidt Data Science for Social Good Fellowship provides a repository of Python (a programming languages) files that can help you process and analyze your data</li>
	<ul>
		<li>See <a href="https://github.com/dssg">here</a> to learn more</li>
		<li>To get started with Python, check out iPython Notebooks (an easy interactive interface for programming via the web):</li>
		<ol>
			<li>Install Python and libraries that are crucial for data science by installing the Anaconda distribution here: <a href="http://continuum.io/downloads">download and install Anaconda</a>.</li>
			<li><a href="http://opentechschool.github.io/python-data-intro/core/notebook.html">Tutorial</a> for setting up and opening IPython Notebook</li>
			<li><a href="http://nbviewer.ipython.org/github/jvns/talks/blob/master/pydatanyc2013/PyData NYC 2013 tutorial.ipynb">Example</a> of how IPython notebooks can be used in data science</li>
			<li><a href="https://github.com/ipython/ipython/wiki/A-gallery-of-interesting-IPython-Notebooks">Amazing examples</a> of IPython Notebooks</li>
		</ol>
	</ul>
	<li>You can also use Microsoft Excel to analyze and visualize your data</li>
	<ul>
		<li><a href="https://books.google.com/books?id=Jx_JBgAAQBAJ&pg=PA267&lpg=PA267&dq=data+science+how+to+with+microsoft+excel&source=bl&ots=BgRpN5Tb44&sig=X8mX2cvBBNAHIVtRlKQvCtgfAUQ&hl=en&sa=X&ved=0CFUQ6AEwCGoVChMIlvzYlIHoxgIVBJmACh2FDgTL#v=onepage&q=data%20science%20how%20to%20with%20microsoft%20excel&f=false">See this book</a> for more information on getting started with Data Science activities in Microsoft Excel</li>
	</ul>
</ul>

####Step 3: Explore Your Data

Exploring the data is a very crucial step in any data science project. Often, the data for a real world problem is messy and does not immediately reveal insights about specific hidden attributes pertaining to the data science problem. Data exploration helps data scientists dig deeper into data by visualizing it in different ways (tables, charts, etc.). It also helps with understanding domain-specific patterns that a data scientist may or may not be aware of.

For example, in the World Bank DSSG project, we looked at the contract data set, which contains approximately 200,000 records spanning from years 2000 to 2014. The figure below shows the development projects for which work was contracted occurred in 168 countries around the world. These contracts were awarded to suppliers from 198 different countries. 

In 76% of cases, the contract was awarded to a supplier local to the borrower country. This proportion varied across the different borrower countries in the data set. The large majority of contracts awarded in South American countries went to a domestic supplier, while the proportion is lower in African countries.

<img src="/img/posts/wbint3.png">
*Image 3: Percent of contracts awarded to a supplier from the same country. The darker coloring of South America indicates that many local suppliers are awarded contracts in this region. In Africa, the lighter coloring indicates that many foreign suppliers are awarded contracts by African countries. [Created with Python (Pandas and Matplotlib)] Source: World Bank Open Finances Data*

####Step 4: Get More Out of Your Data

Once you know what information your data contains, you can start digging deeper. While the raw data points that are recorded in your data sets may be useful on their own, there are often interesting ways to combine different data points to develop additional insight. 

For example, data lists may include the dates on which each contract was awarded to a particular company at the conclusion of the bidding process, as well as the date on which the contract was officially signed by that company. We wondered whether a significant delay between these two events might indicate suspicious activity. To investigate this, we calculated the difference between these two data fields, and discovered that a long delay between the date a contract was awarded and the date the contract was signed was a feature of some substantiated investigations and therefore a *possible indicator* of corruption.

As another example, we compared the available data about contract values with data about the total budget of each development project. Considering whether a contract made up a significant portion of its parent development project provided a scale for the relative monetary importance of that contract.

We also wanted to learn more about the companies that were participating in development projects. The raw data set didn't provide any link between contracts awarded to the same company over time. By searching the data for all of the contracts involving a given company, we could discover trends in the historical behavior of that company. Did it work primarily in the agricultural sector or the financial sector? Did it work in multiple countries?

As you look to expand the power of your own data sets consider the ways that you could combine different aspects of the data. Can you draw on data from two or more different sources? Can you learn something about the historical trends in your project?  

After you have explored your data and generated some calculated fields, like those aforementioned, you can move on to using this data to make models which will allow you to make your existing processes more data-driven and streamlined. 

For example, in our project with the World Bank Group, we built data models that could use data about contracts and previous investigation outcomes to prioritize whistleblower complaints about potential fraud, corruption and collusion. We developed a methodology that could not only prioritize complaints, but also provide justifications for the prioritization. 

This methodology will help the World Bank Group more efficiently pinpoint fraud and collusion in their contracts -- allowing them to devote more of their resources to supporting the developing world, rather than searching for wrongdoing.

Though our project is part of a formal relationship with the World Bank Group (now in [its 2nd year](http://dssg.uchicago.edu/2014/07/11/world-bank-corruption.html)!), similar steps, tools, and approaches can be used by other aspiring data scientists, whether an independent individual curious about a particular social issue or an employee looking for new ways to improve their company's work. With plenty of free resources, software, and data available, now is a great time to find out what data science can do for you.













