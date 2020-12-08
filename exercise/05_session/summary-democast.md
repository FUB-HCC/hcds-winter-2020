# Summary Questions - Democast

1. Can we guarantee that the AI's like the Fairness AI 360 will stay as unbiased as possible in the future ?
1. Is AI the best possible way to solve this problem ?

***

1. I wondered why IBM decided to not commercialized parts of the AI fairness platform. I could imagine that there is a market for this form of application. But in the end its a good decision in terms of the open source community and the society.

***

1. Can reducing the bias for an unprivileged group increase/introduce bias for other groups? (Probably not, because we try to equalize the groups of a protected attribute.)
1. Can reducing the bias for a protected attribute increase/introduce bias for other protected attributes?
1. How do I know which attributes to choose as protected attributes when working with new data? I assume that gender, age, migrant background, etc. are quite obvious to check but there might be some other attributes that are less obvious.

***

1. We need to figure out which class/feature needs to be protected (or contain privileged and unprivileged values). How can we do this? In terms of gender or geographical background, as an example, one would suspect a certain bias, but if it is not that clear, it could be rather hard to determine this. 
1. Since he uses several metrics, does it make sense to use all of them at first and select the best one afterwards? 

***

1. In cases that aren't as obvious as gender, race, etc. how do you decide what features need to be protected? And how can you guarantee that focusing on reducing the bias for some group will not create bias against another one due to the actions taken?

***

1. Is it always the case that you can assume that a group is unpriviledged just because the data seems to indicate it, since for example men are unpriviledged regarding multible criminal offenses, but are actually statistically more aggressive than women ? 

2. If not, how would it be possible to still determine whether there is bias and a priviledged group?

***

1. Where has the framework been used in practice and how can success of its use be assessed?
1. How can we identify the protected feature if it is not obvious?

***

1. How do you know, what metrics is the most suitable for a problem? He said that different bias types can be discovered and then eliminated using different fairness metrics and algorithms, but what if you're dealing with multiple, emerging and complex types of bias, instead a single type? How do you know which fairness metric is capturing all aspects?
1. How can one be sure, that eliminating one bias for a group is not leading to the appearance of another bias? I feel like this whole topic is way more complex than I initially thought, and I think there might be a chance that when you're creating fairness for someone, this automatically implies disadvantages for others. This way, you'd be contradicting the actual purpose of creating fairness.

***

1. Many fairness metrics are mentioned in this demo video. Is there any preference between them? I remembered when the speaker shows the demo, 4 out 5 metrics displayed bias, do the different metrics have different "Aussagekräfte", oder how should we understand when some metrics detect bias whereas others not?
1. For the data processing, unpriviledged attributes are ignored (in the Jupyter example), for some cases we can say that in advance that some attributes arise biases (such as gender/religion/personal status). But in some other cases, there could be some hidden attributes which can also cause bias, how should we detect them since they are hard to be discovered in advance?

***

1. What are possible ways to rework existing models towards being unbiased?