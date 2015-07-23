---
layout: post
title: "Sunlight Project: Text Re-Use in Scott Walker's Abortion Bill"
author: DSSG Sunlight Team
---

<img src="/img/posts/sunlight15-team.png">

On Monday, Wisconsin governor and 2016 presidential candidate Scott Walker signed into law a bill banning non-emergency abortions past the 19th week of pregnancy. Unsurprisingly, Walker's move garnered support from one side, derision from the other, and media attention from both. However, journalists face a big hurdle when trying to provide context for a story such as this: it is time-consuming to figure out how many states have introduced similar legislation and where it originated. 

Automated detection of copied legislation can help. Data Science for Social Good fellows Matt Burgess, Eugenia Giraudy, and Julian Katz-Samuels, technical mentor Joe Walsh, and project manager Lauren Haynes are working with the Sunlight Foundation to make it easier to find re-used text. Using Sunlight's corpus of state legislation, our computational tools uncover textual similarities. 

In its current state, our tool allows the user to enter the text of a bill and then returns documents that potentially match. The tool highlights similar sections in those documents, allowing the user to quickly evaluate the similarities. With the information about bill number, its state, and its legislative session, we analyzed which bills have passed, which ones have died, and which ones are still under consideration.

<img src="/img/posts/sunlight-reuse.png">

The above screenshot shows the tool's highest-rated match for Walker's bill. The left-hand side displays text from [Wisconsin Senate Bill 179](http://docs.legis.wisconsin.gov/2015/proposals/sb179) (2015), and the right-hand side displays text from [Louisiana Senate Bill 593](https://legiscan.com/LA/text/SB593/2012) (2012). The highlighting shows that these sections match almost perfectly. Where differences exist, they are usually numbers versus spelling (e.g. "16" versus "sixteen") or section identifiers (e.g. "(b)" versus "(9)"). 
 
The tool provides a list of documents that possibly match, as well as scores that show the strength of the match. We found the 100 best matches and further narrowed the list to 73 by only keeping the documents containing the word 'pain' (one of the distinguishing terms for this legislation). Here are several:

**Similar bills that passed:**
<ul>
	<li><a href="ftp://www.arkleg.state.ar.us/Bills/2013/Public/HB1037.pdf">Arkansas</a></li>
	<li><a href="http://www.legis.ga.gov/Legislation/en-US/display/20112012/HB/954">Georgia</a></li>
	<li><a href="http://legislature.idaho.gov/legislation/2011/S1165.pdf">Idaho</a></li>
	<li><a href="http://www.kslegislature.org/li_2012/b2011_12/measures/documents/hb2218_00_0000.pdf">Kansas</a></li>
	<li><a href="http://openstates.org/ok/bills/2011-2012/HB1888/">Oklahoma</a></li>
	<li><a href="ftp://ftp.legis.state.tx.us/bills/832/billtext/html/house_bills/HB00001_HB00099/HB00002H.htm">Texas</a></li>
	<li><a href="http://www.legis.state.wv.us/Bill_Status/bills_text.cfm?billdoc=hb2568%20intr.htm&yr=2015&sesstype=RS&i=2568">West Virginia</a></li>
</ul>

**Examples of similar bills under consideration:**
<ul>
	<li><a href="http://ilga.gov/legislation/fulltext.asp?DocName=09900HB3561&GA=99&SessionId=88&DocTypeId=HB&LegID=89750&DocNum=3561&GAID=13&Session=&print=true">Illinois</a></li>
	<li><a href="http://coolice.legis.iowa.gov/Legislation/86thGA/Bills/SenateFiles/Introduced/SF91.html">Iowa</a></li>
	<li><a href="http://openstates.org/ky/bills/2015RS/HB393/">Kentucky</a></li>
	<li><a href="http://mgaleg.maryland.gov/2015RS/bills/hb/hb0492f.pdf">Maryland</a></li>
	<li><a href="https://olis.leg.state.or.us/liz/2015R1/Downloads/MeasureDocument/HB2388/Introduced">Oregon</a></li>
	<li><a href="http://www.scstatehouse.gov/sess121_2015-2016/prever/130_20141203.htm">South Carolina</a></li>
	<li><a href="http://lis.virginia.gov/cgi-bin/legp604.exe?151+ful+HB2321">Virginia</a></li>
</ul>

**Examples of similar bills that have died:**
<ul>
	<li><a href="http://flsenate.gov/Session/Bill/2011/1948/BillText/Filed/HTML">Florida</a></li>
	<li><a href="http://www.legislature.mi.gov/documents/2011-2012/billintroduced/House/htm/2012-HIB-5343.htm">Michigan</a></li>
	<li><a href="https://www.revisor.mn.gov/bills/text.php?number=HF936&version=0&session=ls87">Minnesota</a></li>
	<li><a href="http://billstatus.ls.state.ms.us/documents/2014/html/SB/2400-2499/SB2427IN.htm">Mississippi</a></li>
	<li><a href="http://www.nmlegis.gov/Sessions/11%20Regular/bills/senate/SB0222.html">New Mexico</a></li>
</ul>

The map video below shows in red the bills that passed both the lower and upper chambers, and in purple the bills that were introduced but did not pass. The first bill was introduced in 2010 in South Carolina but failed to pass. In 2011, the bill was introduced in 14 states, with 3 of them passing it: Idaho, Kansas, and Oklahoma. In 2012, six states introduced the bill, but only Georgia approved it. In 2013, eight state legislatures introduced the bill, with Kansas, Texas, and Arkansas passing it. Last year, West Virginia passed the bill while five states rejected it. As of today, seven states have similar bills under consideration: Oregon, Montana, Iowa, Illinois, Kentucky, Virginia, and Maryland.

<iframe width="800" height="450" src="https://www.youtube.com/embed/SABKCC747AQ?rel=0" frameborder="0" allowfullscreen></iframe>
<br>

Many pieces of legislation begin on a lobbyist's desk. We are collecting pieces of model legislation so we can trace legislative text back to its source. We have collected more than 1,500 pieces of model legislation, but most of those come from only a handful of lobbying groups. We searched Google for some of the copied text and found the original at [Doctors on Fetal Pain](http://www.doctorsonfetalpain.com/), a website created to promote the view that fetuses can feel pain at 20 weeks. Although it contained significant text reuse with Scott Walker's abortion bill, it was not in our collection of model legislation.

The tool is not yet available for public use. We're still improving the performance of the algorithm, increasing its robustness to website traffic, incorporating model legislation into our corpus, and automating the legislative searches. However, as this analysis shows, the tool can already provide significant results. We believe this tool will be a valuable resource for journalists and scholars to shed light on state-level politics. 






