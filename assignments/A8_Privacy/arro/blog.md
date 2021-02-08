# A8 - Privacy
> **Name:** `arro` Arne Rolf
> **Session:** [11 Exercise - Explanations](https://github.com/FUB-HCC/hcds-winter-2020/wiki/11_exercise)   
----

## Summary
The talk was about privacy in machine learning, where at first she explained some basics of the differences between a white and black box model, and why the data is split up in training data, validation data, and test data. She showed the importance of privacy focus on a Netflix recommendation coding challenge example, where they hand out "anonymized" data which in the end could be cross linked by researchers with a Linkage Attack by matching the movie database (IMDB) with the netflix challenge data to deanonymize persons.

She then explained ways of privacy attacks on machine learning such as Model Inversion, Membership Inference, and Model Extraction.
She continued with ways to protect privacy with your machine learning model:
- Homomorphic encryption (encrypt the data before you send it to a cloud provider, decrypt it when it comes back)
- Federated learning (learning on client devices, only the weights get send back to the server)
- Secure Multi Party computing (Different institutions train a model together, by sharing partial knowledge about their data)

## Mind Map

* Add your png file here please.
* Please name your png file as `<alsc>_mind-map.png`.

## Question
In the tradeoff between accuracy and privacy, are there more numbers that state a range of how many accuracy percentage points you typically give up?

## Takeways

Key takeaways from the presentation:
- Any tool's effectiveness depends on the correct use (parameter tuning, even the noise parameters)
- Privacy leaks through "misconceptions"
- Privacy method exist, but they might cause overhead (lower accuracy on the model)
- Communicate! Exchange ideas! Encourage interdisciplinary!
