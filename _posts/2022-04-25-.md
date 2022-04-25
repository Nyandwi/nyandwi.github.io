---
layout: post
title: The Single Most Difficulty in Designing Deep Learning Systems
permalink: /neural-nets-design-difficulty/
---

[Read the earlier version of this article on [Twitter](https://twitter.com/Jeande_d/status/1506290793920835590)]

One of the biggest challenges in designing neural networks systems is determining the right size of the network.

Make the network small, it fails to capture the representation in the data. It underfits.

Make the network extremely large, it fools you it's working great on training data, but it fails to generalize on new data which is the ultimate test of a good learning algorithm! It overfits in other words.

How do you determine the right size of the network? Do you even have to build your network?(if you don't build a network from scratch, you have less to worry about the size!)

What does the size of the network even mean? In neural networks, the size of the network typically refers to the number of layers(depth) and a number of units in layers(width).

### Determining the size of the network by guess work

A naive way of determining the size of the network is to try different sizes(depths & widths) and see which works best or take depths and widths as hyperparameters to tune and use hyperparameter tuning techniques/tools to search their best values.

This can work but the problem is that the search space of hyperparameters is very large. You may have to spend lots of time and resources to get the optimal number of layers and units/neurons in layers.

### Reduce guess work by regularizing a large network 

A much better way perhaps is to make the network large and then regularize it. This will usually work well for most problems given the effectiveness of regularization and the conventional wisdom in modern deep learning that says that "large models are better".[^1]

So, rather than using a simple network that can't capture representation from the data, you can make the network (reasonably) big and regularize it with some of the following techniques: dropout, early stopping, data augmentation, Stochastic depth[^2], etc...

In case you are designing your own network, it's safe to make it big and then regularize as long as you can afford to train it and you have enough dataset.

### Don't build from scratch, use transfer learning

Regularing a large network(built from scratch) will likely work but maybe you shouldn't be designing your own architecture from scratch. Here is what I mean...

Some awesome people and organizations spend so much time and resources designing architectures, training, testing them, and open-sourcing the learned weights/trained models for free. Open-source tools like [Timm](https://github.com/rwightman/pytorch-image-models), [Keras](https://keras.io/api/applications/), [PyTorch](https://github.com/pytorch/vision), [OpenMMLab](https://openmmlab.com), etc...maintain models (of different tasks and data) that are ready to use with little fine-tuning based on your own problem.

Technically, I am talking about transfer learning, a technique that refers to reusing a pre-trained model in solving a new problem. Transfer learning is often the way especially if you're solving a common problem like image classification or object detection. Transfer learning [can also be applied in NLP as well](https://github.com/Nyandwi/machine_learning_complete/blob/main/9_nlp_with_tensorflow/5_using_pretrained_bert_for_text_classification.ipynb).

It works great, you don't have to design your own architecture, or worry about the size although you can modify the size of pre-trained model if you want.[^3]

This is the end of the article. Here is a bottom line:

Determining the size of the network in DL system design is one of the hardest things but it shouldn't be. Throw a pre-trained model in your data and there you have it. Don't build from scratch!



#### Footnotes
[^1]: [Deep Double Descent: Where Bigger Models and More Data Hurt](https://arxiv.org/abs/1912.02292), Sutskever et al.

[^2]: [Stochastic depth](https://arxiv.org/abs/1603.09382v3) is a regularization technique that is typically applied in deep networks with residual components. It shrinks the depth(number of layers) during training. It swaps a given subset of layers with identity connections during training.

[^3]: Some regularization techniques (such as data augmentation and dropout) can also be applied during transfer learning since the network can still be too big for the dataset especially if you are fine-tuning.