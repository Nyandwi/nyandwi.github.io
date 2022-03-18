---
layout: post
title: How to Think About Precision And Recall!
permalink: /precision-recall/
---

Precision and recall are classification metrics that are used when the dataset is not balanced or skewed. 

It can be challenging to understand the difference between those metrics. And even when you understand it, it doesn't take long to forget it. Unlike my former articles, this article is organized into a series of questions to give concise explanations. 

### 1. What is the question that each of these metrics answers? 

* *Precision: What is the percentage of positive predictions that are actually positive?*

* *Recall: What is the percentage of actual positives that were predicted correctly?*

$$
Precision = \frac{True Positives}{(True Positives + False Positives)}
$$

$$
Recall = \frac{True Positives}{(True Positives + False Negatives)}
$$

The fewer false positives, the higher the precision. Vice-versa. The fewer false negatives, the higher the recall. Vice-versa.

### 2. How do you increase precision and recall? 

To increase precision, reduce false positives. 

It can depend on the problem, but generally, that might mean fixing the labels of those negative samples(being predicted as positives) or adding more of them in the training data.

To reduce recall, reduce false negatives. 

Fix the labels of positives samples that are being classified as negatives when they are not, or add more samples to the training data.

### 3. What happens when you increase precision or recall?

If you increase precision, you risk hurting the recall. There is a tradeoff between them. Increasing one can reduce the other.

### 4. What does it mean when the precision/recall of your classifier is 1? 

When precision is 1, it simply means that the false positives are 0. 

Your classifier is smart about not classifying negative samples as positives.

What's about recall being 1? False negatives are 0. 

Your classifier is smart about not classifying positive samples as negatives. 

What if the precision and recall are both 1? You have a totally perfect classifier. This is ideal!

### 5. What is a better way to know the performance of the classifier without playing a battle of balancing precision and recall?

Combine them. Find their harmonic mean. If either precision or recall is low, the resulting mean will be low too.

Such harmonic mean is called the F1 Score and it is a reliable metric to use when we are dealing with imbalanced datasets.

$$
F1 Score = \frac{2(Precision * Recall)} { (Precision + Recall)}
$$

If your dataset is balanced(positive samples are equal to negative samples in the training set), ordinary accuracy is enough. 


*********

**Thanks for reading!**

Each week, I write one article about machine learning techniques, ideas, or best practices. 

If you found the article helpful, share it with anyone who you think would benefit from it, connect with me on [Twitter](https://twitter.com/jeande_d), or join my [newsletter](https://www.getrevue.co/profile/deepyearning). 
