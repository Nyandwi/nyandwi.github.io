---
layout: post
title: Uncovering How Machine Learning Systems Learn
permalink: /how-machines-learn/
---

![image](https://jeande.hashnode.dev/_next/image?url=https%3A%2F%2Fcdn.hashnode.com%2Fres%2Fhashnode%2Fimage%2Fupload%2Fv1627550065636%2FAbrpFUwTpW.png%3Fw%3D1600%26h%3D840%26fit%3Dcrop%26crop%3Dentropy%26auto%3Dcompress%2Cformat%26format%3Dwebp&w=3840&q=75)

The whole goal of using machine learning is to learn the rules that can be used to automate a given task. Without the data and ability to learn the patterns hidden in the data(inexplicitly), machine learning would not be the headlines of the internet nowadays. 

In order for a machine to learn such patterns, we need three things: 

1. Input data
2. Actual output
3. Loss and optimization functions

Let's talk about each requirement. 

## 1. Input data

Data is the primary input for any machine learning algorithm. 

Data can be structured, or unstructured. Structured data are usually in spreadsheet(tabular) format. Unstructured data are images, video, sound, and text. 

The problem we are solving is what tells the type of data we need. If you want to predict if this [tweet]() is positive or negative, you will collect many positive and negative tweets. In this case, tweets are text data, so unstructured data. 

*Below is a summary of structured and unstructured data*


![Structured and Unstructured data.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627547096167/JsT7jUl1u.png)

## 2. Actual output

The actual output or what we also call a label is like the description of the input data. For the example of classifying tweets, the labels are `positive` and `negative`. Another example. If the task is image classification(say a car and truck), the labels are `car` and `truck`. 

For many machine learning blocks, you will see labels also referred to answers or results. 


![Screen Shot 2021-07-26 at 11.34.33.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627547115685/01BRn-MKy.png)

## 3. Loss and Optimization Functions

Loss and optimizer are the foundation of `learning` in [machine learning (a term coined by Arthur Samuel)](https://en.wikipedia.org/wiki/Machine_learning#History_and_relationships_to_other_fields). Without the ability of the system to measure the errors and correct them, learning would not be possible. 

In order to measure if a machine learning algorithm is doing well on mapping input data and output, we have to measure the difference/distance between the predicted output and actual output. 

During the model training, such difference is measured by a loss function and will be minimized by an optimization function.

Ideally, the loss will decrease gradually, or step by step, to the point where it is minimum. Or when it converges. This is what makes a learning curve. 

Take a look at the graph below, but pay attention to the decreasing variable or loss. 


![Screen Shot 2021-07-26 at 11.51.54.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627547186218/p3vI3oETJ.png)

In many (if not most) cases, the appropriate loss and optimization function depends on the task. There are regression losses, classification losses, and various optimizers. Choosing an appropriate loss is not a trivial task, but there are clear specifics. 

Choosing the right optimizer for a given problem can be hard. Stick to Adam. It is safe... and forgiving[(CC: Andrej)](http://karpathy.github.io/2019/04/25/recipe/). 

******
To summarize, machine learning systems are made of 3 main things: Input data, output label, and functions that measure and minimize loss(loss and optimizer). 

Below is your visual takeaway. 


![#Social Post.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627550943752/n4pTSL0Yd.png)

*******

Thanks for reading!

Each week, with a probability of 80%, I write one article about machine learning techniques, ideas, or best practices.

If you found the article helpful, share it with anyone who you think would benefit from it, connect with me on  [Twitter](https://twitter.com/Jeande_d), or join my  [newsletter](https://www.getrevue.co/profile/deeprevision).
