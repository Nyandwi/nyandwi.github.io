---
layout: post
title: The Unavoidable Difficulties of Machine Learning Systems - Data and Model Drifts
permalink: /data-and-model-drifts/
---


![image](https://jeande.hashnode.dev/_next/image?url=https%3A%2F%2Fcdn.hashnode.com%2Fres%2Fhashnode%2Fimage%2Fupload%2Fv1626952308565%2FDuwG66z9W.png%3Fw%3D1600%26h%3D840%26fit%3Dcrop%26crop%3Dentropy%26auto%3Dcompress%2Cformat%26format%3Dwebp&w=3840&q=75)

Machine learning systems are complicated. And sometimes, it's not the fault of the engineers who build them. It's the nature of machine learning systems. 

Here is what I mean...

Let's say that you did a great job at finding good data, you prepared it reasonably well, and your model made great predictions. Everything is pretty cool at the moment! 

But there are times you won't be able to prevent the worse to happen. A model that is used to make good predictions can start to make misleading predictions. What can go wrong?

There are two reasons why that can happen, and they are all rooted in changes, either that is the change in data, model, or both.

### Change in Data: Data Drift

Let's say that you trained an image classifier with the images collected from the internet. The classifier did well on these images. 

But later you deployed the classifier on the mobile phone to recognize images taken from the mobile camera.

If such a mobile camera is not decent enough to take good images just like the high-resolution internet images that the classifier was trained on, it's very likely that it will fail to recognize the images taken by the mobile camera.

The data changed. This is *data drift*.

In data drift, the distribution of the data has changed and that resulted in the failure of the model. 

### Model Drift

There are times data will not change, but the model still performs worse. 

Let's take another example but in this case, I will use my [Twitter account](https://twitter.com/jeande_d) as an example. 

The data that is used to recommend to me the favorite content do not change. But if I pass a week or more without using Twitter in a mobile app, I will find news on top of the feeds (which I don't check often), but at the same time, the same account, if I use the web, I mostly get machine learning content on the top because I use the Twitter web often. What happened? 

The data that Twitter uses to recommend me good tweets didn't change on the mobile app, but my behavior towards the platform changed. 

You will see this too if you pass a week or more without using a given service, the model that recommends things to you will decay because you changed your behavior towards these services.

If you watch videos on Youtube or Netflix, you can notice this too, especially in the times you are using these services more frequently or less than normal. They will struggle to learn your new behavior or interests, they will fail to recommend your video or movie types.

All of the above examples describe *model drift*. Technically, model drift is caused by the change in the relationship between the input data(features) and output data (labels). 

### How to Handle Data and Model Drifts? 

One of the ways to handle data and model drifts is to retrain the model with both old and new data. And sometimes, scheduling retraining can be a good way to deal with that. 

How long you should wait to retrain a model depends on the type of your problem. For things that are used frequently (and winner take all) like online stores, streaming services, retraining should not wait too long. You do not want users to be overwhelmed with false recommendations.

Other times retraining can be weekly, monthly, or whatever time can suit the type of things you are dealing with.

### How to Spot Drifts? 

There are two ways to detect the decay of predictions caused by either model or data drift. The first option, which is common is to monitor the important metrics regularly via the dashboard and set up an alert if something goes wrong. 

Another technique that can be used is to train an anomaly detection model on the normal performance of a given system and let its goal be to spot if there is something unusual in the system's output. 

Also, after the drift is detected, there are can be an action in place (or automated), such as immediate retraining. 

#### To summarize this article: 

Machine learning systems are complicated. Data can change, models can change, and any of those affect the predictions. 

One of the ways to deal with these changes is to retrain the models with the old and new data and if retraining is frequent, it can be scheduled. 

*******

Thanks for reading!

Each week, with a probability of 80%, I write one article about machine learning techniques, ideas, or best practices.

If you found the article helpful, share it with anyone who you think would benefit from it, connect with me on  [Twitter](https://twitter.com/Jeande_d), or join my  [newsletter](https://www.getrevue.co/profile/deeprevision).
