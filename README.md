# Kickstarting the Theatre of Excel

## Overview of Project

### Purpose
Assignment 1

   The scenario of this assignment is that we received a hypothetical set of data describing
  the results of a variety of Kickstarter campaigns from Louise: an up-and coming playwright who intends to fund her own campaign.
Through our analysis of the data, we intend to help her decide on a set of details for
her own campaign in order to increase the likelyhood of it's success. This we achieve through the analysis of graphs
and tables obtained by filtering the data to fit her specific needs.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date


In order to perform an analysis on outcomes based off of launch date, we first had to edit the data itself.
The raw data provided included the dates in unix timecodes. In order to make them readable, I took the codes from
column J, then converted them to readable dates in a new column via the excel formula `=(((J2/60/60/24)+DATE(1970,1,1)'
	Next, with functionable dates, I created a pivot table counting outcomes into rows designating the dates,
filtering them down to show the months specifically. Adding filters for Years and Categories, the following chart
was produced:

![Chart of Outcomes vs Launch Date](https://github.com/Jelsik/kickstarter-analysis/blob/main/Theater_Outcomes_vs_launch.png)

### Analysis of Outcomes Based on Goals


To proceed through this analysis, conditional data needed to be collceted from the main kickstarter Worksheet
Specifically we are looking for outcomes of projects within a given series of dollar amounts. The formula 'COUNTIFS()'
would be employed to collect results on another a new page from the original one. For the dollar categories the conditionals
to search for were: Category:Plays, the Number of projects succesful/failed/canceled in that range, and then the final
count of the total number of projects was collected.
	This data allowed us to find the percentage of the results for each category, then use them to plot the following
line graph:

![Chart of Outcomes vs Goals](https://github.com/Jelsik/kickstarter-analysis/blob/main/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered


The challenges that were and could be encountered doing these analyses mostly centered around data in the
parent kickstarter worksheet. The data needed to be organized to have additonal conditions; so that we could 
properly locate and define the data categories. This would ensure that the pivotcharts produced
from this dataset could be accurately filtered to provide the results asked for.

## Results

###Chart 1: Outcomes based on Launch Date


Based on the first chart embedded in this report, you can conclude that the greatest portion of successful
theatre campaigns were launched in May, making this the most logical launch month. Secondly, one can see from the data that,
successful or not, the groups who proceed to launch a kickstarter campaign are dedicated. Very few of the kickstarters
launched overall are canceled; most notably is that not a single campaign launched in october was canceled.
	My reccomendation to Louise would be to make sure that this was the direction she wished to take for certain,
and then suggest a launch date in May, and continuing into the summer.

###Chart 2: Outcomes based on Goals


Based off of the outcomes defined in this chart, linked earlier in the report, a definite trend forms.
Generally speaking, the lower financial goal a theatre campaign has, the more likely it is to succeed. There is a recovery
period flattening off in the mid 60% for theatre campaigns from 35000 to 44999, but no theater campaign in the range
of 45000 to 49999 was succesful.

###Dataset Limitations:


We do not have data based on the traffic to these kickstarter pages, or web analytics of the companies/indiviuals
in charge of these campaigns. Many of these successes could be based off of previous popularity of the campaign's source.
In addition, this data gives us access to the total number of backers, but not the total number of visitors to these campaign's pages.
We can assume from the data that projects that were "staff picks" got more traffic than normal, but real numbers would be good to 
more accurately see how many or how few visitors chose to take the additonal plunge and become a backer.

###Additonal Charts or Graphs

There are a few additional charts and graphs that could be generated in order to provide Louise with a more
informed reccomendation. A chart plotting Campaign Length vs. Success would be useful. This could be combined with the info 
 regarding launch date, in order to see if there was an additional connection. Also helpful could be a table comparing the number
 of campaigns of defined lengths compared to start date. Perhaps the success in May and summer is because of lightning-quick campaigns,
 or perhaps they run the whole season to accumulate enough funds for their goal.
