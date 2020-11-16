# Title of your post
> **Date:** 07.11.2020 - 15:37 PM *(Due: 17.11.2020 - 03:00 PM)*  
> **Name:** `albe` Ali B.  
> **Session:** [02 Exercise](https://github.com/FUB-HCC/hcds-winter-2020/wiki/02_exercise)   
----

## R2 - Reflection
> Book: The Practice of Reproducible Research (Chapter 2 and 3)

### Definitions
_Reproducibility and replicability_

_How does this relate to the definitions given in the lecture?_


### 🗨️&nbsp; "How does the reading inform your understanding of human centered data science?"  
_Describe in at least 2-3 full sentences._

### ❓&nbsp; Questions
_List at least 1 question (full sentence) that this reading raised in your mind, and say why._

1. ...
1. ...

***

## A2 - Reproducibility Workflow
_Briefly describe your experience using the reproducibility workflow._

I fist started this assingment with getting an understanding for the API and the parameters. 
Then I started with use these parameters to acuire the data from the API and to build the filenames 
with the specified convention. Then I started to build a directory structure and continued with 
following pre proccing steps which I know from the usual pre proccessing steps. 


### Final Wikipedia Page View Plot
_Add an image of your plot here and describe what you can see._ 🖼️ 

![final_vis.png](final_vis.png)

In the area where we have overlapping data from both APIs it is notable that for the desktop site (mobile site is the same) we have more views with the Pagecounts API. This coud be because the Pagecounts API includes also views from Bots. 

![comparison_apis.png](comparison_apis.png)

Also the trend is notable that over the time the views for the desktop side is decreasing while the views from mobile site is increasing. 
![trend_corr_dektop_mobile.png](trend_corr_dektop_mobile.png)

Unfortunatally I was not able change the format of the y-Axis label to display the values in billions. I spend a lot of time seaching a way ow this can be done in altair but could't find a solution now. I assume this is possible by passing a format to the y-Axis like '.1f' for 
float numbers with 1 digit after the comma which works well. 

### Challenges

For me a big challange was the big patience to spend the extra amount of efford for the data pre processing step. 
From other data sience projects I know that some amount of effort is required for the pre processing step but in this 
small project I had the feeling that I spend a bit more time on building an understandable structure for my project.

_What was surprising, what did you learn?_ 😮 

I knew that pre-processing is time comsuming but I was suprised that I still underestimated this efford >.<'

