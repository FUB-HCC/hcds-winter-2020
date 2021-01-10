# Title of your post
> **Date:** 16.11.2020 - 18:35 PM *(Due: 11.01.2020 - 03:00 PM)*
> **Name:** `alsc` Alexa S.
> **Session:** [07 Exercise - Explanations](https://github.com/FUB-HCC/hcds-winter-2020/wiki/07_exercise)   
----

## A5 - Explanations

### Task 1: Different Explanation Needs

#### ORES Scenario

** Please describe the roles and the different explanation needs in the context of ORES by writing your own scenario. Tool to detect incomplete and unsufficiently proven articles

*Description:* Machine learning systems are being used in photo gallery applications inside of phones and computers to categorize photos. On use case is to enable extended photo search functionality, for example, the user can search for the keyword "car" and the app will return all gallery pictures containing objects that have been identified as a car. Additionally they are being used to detect persons in pictures to match them with a specific contact from the users contact list. In the latter case, the application already cathegorizes detected persons, but the user has to link the person collection to a specific contact. The user can also decide, wether a detected person matches with its assigned group or if the application has made a mismatch.

* Creators: the software company and its employees that developed the gallery app

* Operators: the users of the application

* Executors: the user of the application

* Decision-subject: the user of the application

* Data-subject: the user of the application and every person and object that has been photographed. Also all objects and people which have been photographed to train the ML System before releasing the app

* Examiners: mostly the quality assurance department of the software company, but also the user that decides wether a photo was cathegorized correctly

**Explanation needs**
* The creators need to explain the idea of the ML system to the developers, that implement the application
* Operators need to know, how to use the ML feature in the gallery application
* Data-subjects need to know how to cathegorize photos properly to make the best out of the application function
* Data-subjects should get an explanation how their data is being used
* Examiners need an explanation on the expected application behavior

#### Reflection
_your TEXT here_

_your IMAGE here_

### Task 2: Explanation method: LIME

_LINK to your annotated notebook here_

### 81
![](81.png)
### 82
![](82.png)
### 84
![](84.png)

#### Reflection

1. Which documents did you choose?
  
    documents with the ids: 81, 82 and 84

2. What did you learn about the model?
  
    Even with the features listed it is quite hard to understand how the model classifies the data, since most features seem to be quite random, Such as names or the 'Re:' in the subject line being used to predict atheism. Some features make a lot of sense though, like 'God', 'Jesus' or 'murder'. When looking at the positions of the used words it becomes very apparent that the classifier uses the header and its structure for most of its atheism classification, which is why the words used don't really make a lot of sense in some cases.
3. How well do you think the classifier works? Why?
  
    Since the classifier a high F score of 0.924 as shown in the example notebook, the classifier seems to work very well. Since the classifier uses the header for most of its atheism classification, this may be very different when working with data with a different structure, though
4. For what role(s) (from task 1) are LIME explanations useful? Why?
5. How useful is LIME for a non-data-scientist (e.g. non-ml-experts or designer)? Why?
    
    I would say it is quite useful, since it is very easy to use with a little guidance and can provide valuable insights for non-data-scientist as well.
6. What question types is LIME able to answer? Why?
  
    LIME is able to explain the inner workings of a model after it was used on data by answering how a classifier got to a specific chosen result and display the feature weights used.
