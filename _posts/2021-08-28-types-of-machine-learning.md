---
layout: post
title: 5 Main Types of Machine Learning Systems
permalink: /types-of-machine-learning/
---
![image](https://jeande.hashnode.dev/_next/image?url=https%3A%2F%2Fcdn.hashnode.com%2Fres%2Fhashnode%2Fimage%2Fupload%2Fv1635421775909%2FJF_J8XSd-.png%3Fw%3D1600%26h%3D840%26fit%3Dcrop%26crop%3Dentropy%26auto%3Dcompress%2Cformat%26format%3Dwebp&w=3840&q=75)[^1]

Machine learning, a science of teaching computers to perform tasks without programming them explicitly is classified into five main types that are:

* Supervised learning
* Unsupervised learning
* Semi-supervised learning
* Self-supervised learning
* Reinforcement learning

Let’s talk about them.

### 1. Supervised Learning

Supervised learning is the common most type of machine learning. Most ML problems that we encounter fall into this category.

As the name implies, a supervised learning algorithm is trained with input data along with some form of guidance that we can call labels.

In other words, a supervised learning algorithm maps the input data (or X in many textbooks) to output labels (y).

Labels are also known as targets and they act as a description of the input data.
In general, there are 2 main kinds of supervised learning problems that are:

* **Classification**: where the task is to identify a given category from numerous categories or simply make choice between a number of categories. Example of a classification problem: To identify if the incoming email is either spam or not based on the email contents.

* **Regression*: where the goal is to predict a continuous value of something. An example of this regression task is to predict the price of a used car given its features such as brand, number of doors, number of sits, safety level, maintenance cost, etc…

Example of supervised learning algorithms:
* Linear/logistic regression
* Decision trees
* Random forests
* K-Nearest Neighbors(KNN)
* Support vector machines(SVM) and
* Neural networks (which can also be unsupervised).

With that said, there are other advanced tasks that don’t directly fall into supervised learning, but they actually are.

Here are some:
* Image captioning where the goal is to predict the caption of a given image.
* Object detection where the goal is to recognize the object in an image and draw the bounding box around it.
* Image segmentation where the goal is to group the pixels that make up particular objects in the image.

Some of those tasks can involve both classification and regression. Take an example for object detection: it involves classification(recognizing the object among many other objects) and regression(predicting the coordinates of the objects in an image to make a bounding box).

### 2. Unsupervised learning
Supervised learning algorithms are trained with data and labels. Conversely, unsupervised learning algorithms are trained on unlabelled data.

Unsupervised learning algorithms are primarily used for clustering(such as K-Means), dimension reduction and data visualization(such as PCA, and t-SNE). PCA stands for Principal Component Analysis, and t-SNE is t-Distributed Stochastic Neighbor Embedding.

### 3. Semi-supervised learning

Semi-supervised learning falls between supervised and unsupervised learning.
In semi-supervised learning, a small portion of training data is labeled while the rest of the data points are not labeled.

Data labeling is one of the most challenging things in machine learning. It’s time-consuming and expensive. Semi-supervised learning reduced that bottleneck.

Semi-supervised learning is most notable in problems that involve working with massive datasets like internet image searches, image and audio recognition, and webpages classification.

### 4. Self-supervised learning
Self-supervised learning is one of the most exciting types of machine learning that is most applicable in computer vision and robotics.

While semi-supervised learning uses a small portion of labeled data, self-supervised learning uses entire unlabelled data and it does not require manual annotations, removing the need for humans in the process.

Quoting great self-supervised learning  [paper](https://arxiv.org/abs/2003.05199) :

>“Producing a dataset with good labels is expensive, while unlabeled data is being generated all the time. The motivation of self-supervised learning is to make use of a large amount of unlabeled data….The main idea of self-supervised learning is to generate the labels from unlabeled data, according to the structure or characteristics of the data itself, and then train on this unsupervised data in a supervised manner.”

And here is a great quote about self-supervised learning by Yann LeCun:

> "If intelligence is a cake, the bulk of the cake is self-supervised learning, the icing on the cake is supervised learning, and the cherry on the cake is reinforcement learning (RL).”

If you would like to learn more about self-supervised learning, check out this  [awesome repo](https://github.com/jason718/awesome-self-supervised-learning#survey)  or this survey  [paper](https://arxiv.org/abs/1902.06162#).

### 5. Reinforcement learning

Reinforcement learning is a special type of machine learning that is most applicable in games and robotics.

In reinforcement learning, a learning system called an agent can perceive the environment, perform some actions, and get rewarded or penalized depending on how it is performing.
The agent learns the best strategy (or policy) necessary for getting the most reward by itself.
For most of us, we may not get the most of reinforcement learning due to limited resources and applicability, but it’s a powerful thing for those who can afford it.

Reinforcement learning holds some of the most historical moments about AI. In 2016, [DeepMind AlphaGo](https://www.youtube.com/watch?v=WXuK6gekU1Y&list=PLqYmG7hTraZBy7J_4ynYPc0Ml1RUGcLmD&index=2&t=147s), a reinforcement learning system, won Lee Sedol in Google DeepMind Challenge Match.
Go is a complex board game that requires intuition, creative and strategic thinking. And Lee was one of the world-class Go players. Below is the movie between AlphaGo and Lee.


This is the end of the thread that was about the types of machine learning. The types are:

* Supervised learning
* Unsupervised learning
* Semi-supervised learning
* Self-supervised learning
* Reinforcement learning

*******

Thanks for reading!

Each week, with a probability of 80%, I write one article about machine learning techniques, ideas, or best practices.

If you found the article helpful, share it with anyone who you think would benefit from it, connect with me on  [Twitter](https://twitter.com/Jeande_d), or join my  [newsletter](https://www.getrevue.co/profile/deeprevision).

[^1]: **Cover image**: A child learning a bike under dad's supervision. Thanks to Vm/Canva for making the image freely available.