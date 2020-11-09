Assignment 1
> **Date:** 02.11.2020 - 15:30 PM *(Due: 10.11.2020 - 03:00 PM)*  
> **Name:** `rowe` Robin W.  
> **Session:** [01 Exercise](01_exercise)   
----

## A1 - Warm up

Settings up the programming environment was very easy. Poetry installation went without problems. I am using Pycharm,
so i used the integrated git features to pull the project. From within pycharm i used the peotry commands to then start the notebook.

### Wikipedia Edits

I did look for an antricle and decided for "Predident of the United States" in english and german. Just like in the example before,
i queried the api for edit data for the german and english version of the article and for anon/user edits.

i then merged the german anon and user data first, renamed the columns. Then i merged the result with the english anon edits,
again renaming the column. At Last, i merged this with the english user edits.

For finishing up, i plotted all 4 columns with different colours in one plot. Result can be seen here:

![](plot.png)

#### Challenges
I am relatively new to data science, have used pandas briefly before and also matplotlib. As such, i had to refresh/learn
a lot of stuff about these, which took a little bit of time. I also had some problems with the csv task, as many opf the
govdata .csv datasets produced an error when importing it.

I was surprised by how powerful pandas and the other tools are for analyzing data and how easy it is to get good results
with them. I also was surprised about the kinds of data laying around on GovData :D

## R1 - Reflection
> Podcast: Human-centered Design in Data Science (with Peter Bull)


### 🗨️&nbsp; "How does the podcast inform your understanding of human centered data science?"  
The podcast confirms my idea of how a Human centered design process can be integrated into data science. In the podcast,
the exact steps of Human centered design we learned about in HCI 1 are applied to a data science project. It also confirms
my understanding that the outcome or what the people the data science project is done for need should be the focus,
not the technology or data used. The part about getting off from the computer and get to where the data is being produced
is very important from my point of view.

### ❓&nbsp; Questions 
1. I was asking myself it can really be that easy said that you always need to get to where your data originates from.
This is easier said than done as sometimes data can be generated where you are not permitted to be on site. The example
of the tanzania finance data is one of them. Not everyone or everywhere people are willing to let you observe money transactions.
