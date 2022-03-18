---
layout: post
title: Why Is It So Hard To Train Neural Networks?
---

Neural networks are hard to train. The more they go deep, the more they are likely to suffer from unstable gradients.

Gradients can either explode or vanish, and neither of those is a good thing for the training of our network.

The vanishing gradients problem results in the network taking too long to train(learning will be very slow or completely die), and the exploding gradients cause the gradients to be very large.

Although those problems are nearly inevitable, the choice of activation function can reduce their effects.

Using ReLU activation in the first layers can help avoid vanishing gradients. 

That is also the reason why we do not like to see sigmoid activation being used in the first layers of the network because it can cause the gradients to vanish quickly. 

Before researchers come to the conclusion that sigmoid kills the gradients when the weights are too big or small, people were using sigmoid as a cool activation function at the time. But in 2010, Xavier Glorot and Yoshua Bengio wrote a great [paper](http://proceedings.mlr.press/v9/glorot10a.html) showing that sigmoid doesn't scale well when the weights are randomly initialized. The same is true about hyperbolic tangent function(tanh). You should avoid using both of them. 

This post was only about the high-level understanding of the vanishing gradient problem. If you would like to learn more, you can read this [stats discussion](https://stats.stackexchange.com/questions/262750/why-is-it-hard-to-train-deep-neural-networks/369353#369353) Or read [chapter 5](http://neuralnetworksanddeeplearning.com/chap5.html#the_vanishing_gradient_problem) of the book Neural networks and Deep Learning by Michael Nielsen.

Key takeaways:
* It is hard to train deep neural networks due to unstable gradients problems.
* Using ReLU can avoid the gradients to vanish.
* Avoid using a sigmoid and hyperbolic tangent function(tanh) as they can cause the gradients to vanish.

******
Thanks for reading!

Each week, with a probability of 80%, I write one article about machine learning techniques, ideas, or best practices.
If you found the article helpful, share it with anyone who you think would benefit from it, connect with me on  [Twitter](https://twitter.com/Jeande_d), or join my  [newsletter](https://www.getrevue.co/profile/deeprevision).
