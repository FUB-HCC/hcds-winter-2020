
# Blog A1
> **Date:** 07.11.202 - 13:30 PM *(Due: 10.11.202 - 03:00 PM)*  
> **Name:** `ansa` Anil Sahintürk.  
> **Session:** [01 Exercise](01_exercise)   
----

## A1 - Warm up

I first tried to setup the environment in Windows 10. But that caused me some trouble so I decided to setup everything in Linux Ubuntu. From there on I just had some little trouble with opening jupyter notebook as a non-root user it would give me the error _500 Internal Server Error_. Changing ownership rights did not fix the problem so I removed jupyter and found the solution in reinstalling with the command _conda install jupyter._

### Wikipedia Edits
I decided to first fetch the user edits data from the article 'Donald Trump' in German and English. So I had 2 JSON files from user data for each language. Than I merged them together.

I did the same for the anonymous edits data. Then I merged both the user edits data frame and the anonymous data frame together. After that I plotted the graph u see below.

![](https://gblobscdn.gitbook.com/assets%2F-MLXUNAbLGVqvn6dZBCx%2F-MLXWu0aoWJ_IQ7n32OJ%2F-MLXarUl1IowsDkiVdaK%2FBildschirmfoto%20von%202020-11-07%2013-07-52.png?alt=media&token=ffd10075-a80c-4ca0-beec-d4056fbf5bf9)
*Edits for the Wikipedia article 'Donald Trump' from 01.01.2020 - 31.10.2020*

We can see some spikes in the beginning which probably are caused by some political events (Iran, corona, etc.). The biggest spike happened recently and this may be because of the current election in the USA.


#### Challenges

The most challenging for me was to fetch the data from the API. But after a while I got the hang on it. I do not have a real expertise in data science but I have worked with pandas, matplotlab, numpy etc. before because I want to teach myself a basic understanding of data science. That means the other tasks were not really challenging but I had to read the documentation to follow along.

I learned how to use an API and how to merge data frames together. The mentioning of GovData was a surprise to me because I did not know that the government was sharing data like that.

## R1 - Reflection
> Podcast: Human-centered Design in Data Science (with Peter Bull)


### 🗨️&nbsp; "How does the podcast inform your understanding of human centered data science?"  
Surprisingly data science needs a lot more communication in the process as I thought in the beginning. Like Peter Bull mentioned in the podcast I thought of data more like a treasure that contains all the information we need to solve problems. But it seems like the data itself is not enough. And that is also true from a business perspective because it is easy to create a product that has no value for its clients if there is no clear communication about their shared goals.

### ❓&nbsp; Questions 
1. Is it possible to create machine models completely free from bias?
2. If so how?
3. If not how can we deal with it?
4. How does data ethics influence the data science process?

