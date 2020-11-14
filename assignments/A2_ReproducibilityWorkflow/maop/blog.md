# Assignment 2
> **Date:** 14.11.2020 - 22:31 PM *(Due: 17.11.2020 - 03:00 PM)*  
> **Name:** `maop` Marc O.  
> **Session:** [02 Exercise](https://github.com/FUB-HCC/hcds-winter-2020/wiki/02_exercise)   
----

## R2 - Reflection
> Book: The Practice of Reproducible Research (Chapter 2 and 3)

### Definitions

_Reproducibility and replicability:_

The authors provide multiple definitions from different sources. Their prefered definition is the one from Goodman et. al.:
* \[Reproducibility is\] the ability of a researcher to duplicate the results of a prior study using the same materials as were used by the original investigator. That is, a second researcher might use the same raw data to build the same analysis files and implement the same statistical analysis in an attempt to yield the same results. 

* \[Replicability\] \[...\] refers to the ability of a researcher to duplicate the results of a prior study if the same procedures are followed but new data are collected.


_How does this relate to the definitions given in the lecture?:_ 

The definitions from the lecture are are pretty similar to the ones mentioned above and are based on the same fundamental ideas. While our definition is "including key quantitative findings, tables, and figures \[when providing\] only a set of files and written instructions", Goodman et. al. simply bundles these aspects to results, without specifying more precisely what the result needs to contain. Goodman's definition focusses more on making sure that the "same analysis files and \[...\] same statistical analysis" is being used to receive the same result.  

Compairing the definitions of replicability one finds major differences in terms of the actual purpose of replication. The definition presented in the lecture motivates the reason for replicating a project with "achieving a commensurate, confirming, or contradictory result". Furthermore purpose of replication is "to strengthen the foundation of a theory so that it too will become a part of our general knowledge system." These were aspects that were neglected in the books definitions.


### 🗨️&nbsp; "How does the reading inform your understanding of human centered data science?"  
_Describe in at least 2-3 full sentences._

Human Centered Data Science is also about providing code which has been produced during research projects and making sure your research projects are fully reproducible. Providing a project that is not reproducible or replicable is therefore almost worthless for other developers, or people that try to understand and verify the used methods. Publishing such projects comes with a high responsibility towards everyone to whom these results are being provided.

### ❓&nbsp; Questions
_List at least 1 question (full sentence) that this reading raised in your mind, and say why._

1. There are many degrees of reproducibility. What degree is used for what purpose? I can image that developing software for a bigger company requires a very high degree of reproducility. But on the other side making sure a project is perfectly reproducible can be very time consuming and best believe that companys do not have the budget or the will to secure reproducible workflow. Therefore: what is considered a "minimum" reproducible project, that satisfies the criteria for reproducibility but also digs not too deep.

***

## A2 - Reproducibility Workflow
_Briefly describe your experience using the reproducibility workflow._

* **Step 1:** I started this assignment by setting parameters for the queries through the APIs. I then proceeded to create a directory structure which was presented in Chapter 2. All the queried data was then saved in the `raw` directories.

* **Step 2:** Afterwards, I processed the data by cleaning, extracting, and reassigning, and combining dataframes to create the `clean` data in the required format. I decided to compute the average views for the ~ 1 year of overlapping data. I figured out that adding the data in this overlapping time period is senseless, since parts of the data were counting the same things (e.g. views for mobile access type).

* **Step 3:** I adjusted the data set and plotted the time series which seriously gave me headaches labeling, resizing and trying to adjust the axis.

### Final Wikipedia Page View Plot
_Add an image of your plot here and describe what you can see._ 🖼️ 

![result graph.png](result/result graph.png)

The gray line is showing all traffic (desktop+mobile)

The green line is showing mobile traffic only

The blue line is showing desktop traffic only

**Note that the blue line is actually underlapped by the gray line. The reason for this is that date on mobile traffic is only available starting from 2014/10. Therefore all traffic (which is being computed as the sum of mobile+desktop traffic is the same as the desktop traffic until 09/2014**

### Challenges
_Describe what tasks were challenging to you._
* It was challenging to me to merge the data and not always work with the dataframes as variable, but to ensure a reproducible workflow. I must admit that sometimes I just wanted to call a prior created variable containing the needed dataframe. But for this task it was crucial to make sure to follow best practices for reproducible research, which meant putting more effort in exporting the acquired data and parsing it again.

_What was surprising, what did you learn?_ 😮 
* It was definitely surprising to see how much work it actually is to deliver a fully reproducible project. There's much more behind it than I thought it would be
