---
layout: post
title: The Ultimate Guide on Choosing the Right Neural Network Architecture For the Right Data
permalink: /choosing-neural-nets-architecture/
---
![image](https://jeande.hashnode.dev/_next/image?url=https%3A%2F%2Fcdn.hashnode.com%2Fres%2Fhashnode%2Fimage%2Fupload%2Fv1631359206938%2FLHXDAR_nG.png%3Fw%3D1600%26h%3D840%26fit%3Dcrop%26crop%3Dentropy%26auto%3Dcompress%2Cformat%26format%3Dwebp&w=3840&q=75)

There are different kinds of data. Neural networks architectures are of different kinds too.

Some of the choices of network architecture can be obvious, but machine learning is an experimentation science. A network that was invented to process images can turn out to work well on texts too. 

As of today, neural networks are of 4 main architectures: Densely connected neural networks, Convolutional Neural Networks(Convnets), Recurrent Neural Networks (RNNs), and transformers. 

What are these networks and what kinds of data they are suited for? 

### Densely Connected Neural Networks

Densely connected networks are made of stacks of layers from the input to the output. 

The units (or neurons) of any layer in that type of network are connected to all other units of the next layer. This is why they are also called fully connected layers. 

Densely connected layers are generally used for tabular data. Tabular data are these kinds of data that are in a tabular fashion. An example of tabular data is customer records: you have a column of names, roles, data joined, etc...


![Densely connected.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1631359484854/ioMW08ea2.png)
*Image: Densely connected networks*

Dense layers are also used (in the combination of other architectures) as the last layer in either classification or regression problems. The right number of units in the last layer depends on the problem. Take an example: if you are classifying the news into 4 categories, then the last layer will have 4 units. If you are predicting the price of a house given its features, the last layer will have 1 unit. 

### Convolutional Neural Networks (CNNs)

CNN's, a.k.a Convnets are widely known as the go-to neural network architectures when it comes to processing images, but they can also be used in other data such as texts and time series.

Convnets are typically made of convolution, pooling layers, and fully connected layers at the end. Convolutional layers are used to extract the spatial features in images, and pooling layers are used to compress the resulted feature maps from convolution layers. And fully connected layers for classification purposes. 

![on-IOL-iG.png-2.webp](https://cdn.hashnode.com/res/hashnode/image/upload/v1630788206761/KF4gj3zPD.webp)
*Image: Convnets architecture*

Convnets are of 3 dimensions. The most popular one is Conv2D that is used in images and videos divided into frames. Conv1D is used in sequential data such as texts, time series, and sounds. A popular sound architecture called [WaveNet](https://deepmind.com/blog/article/wavenet-generative-model-raw-audio) is made of 10 stacked 1D Convnets.

Conv3D is used in videos and volumetric images such as CT scans.

### Recurrent Neural Networks(RNNs)

The standard feedforward network (or call them densely connected network) maps the input to output. RNNs go beyond that. They can maintain the recurrence of data at each time step. 


![TF RNN.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1630789332991/7kzTaiwxp.png)
*Image: Feed forward network vs recurrent neural networks*

Due to their ability to preserve the recurrence of information, RNNs are commonly used in sequential data such as texts and time series. 

The basic RNN cells are not efficient at handling large sequences due to a short memory problem. They also suffer from [vanishing gradients](https://www.youtube.com/watch?v=qhXZsFVxGKo). 

The variant of RNNs that are able to handle long sequences is called Long Short Term Memory(LSTM). LSTM has also the ability to handle the sequences of variable lengths.  

A special design difference about the LSTM cell is that it has a gate which is the basis of why it can control the flow of information over many time steps. 

In short, LSTM uses gates to control the flow of information from the current time step to the next time step in the following 4 ways: 

  * The input gate recognizes the input sequence.
  * Forget gate gets rid of all irrelevant information contained in the input sequence and store relevant information in long term memory.
  * LTSM cell updates update cell's state values.
  * Output gate controls the information that has to be sent to the next time step. 

![Screen Shot 2021-09-01 at 09.22.56.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1630789390006/avzF2LKrK.png)

*Image: LSTM architecture, [Intro to Deep Learning MIT](https://www.youtube.com/watch?v=BUNl0To1IVw&list=PLtBw6njQRU-rwp5__7C0oIVt26ZgjG9NI&index=5)*

The ability of LSTMs to handle long-term sequences makes it a suitable neural network architecture for various sequential tasks such as text classification, sentiment analysis, speech recognition, image caption generation, machine translation. 

Another recurrent neural network that you will see is [Gate Recurrent Unit(GRU)](https://arxiv.org/pdf/1412.3555.pdf). GRU is a simplified version of LSTMs, and it's cheaper to train. 

### Transformers

Although recurrent neural networks are still used for sequential modeling, they have short-term memory problems when used for long sequences, and they are computationally expensive. The RNN's inability to handle long sequences and expensiveness are the two most motivations of transformers. 

Transformers are one of the latest groundbreaking researches in the natural language community. They are sorely based on the attention mechanisms that learn the relationships between words of the sentence and pays attention to the relevant words. 

One of the most notable things about transformers is that they don't use any recurrent or convolutional layers. It's just only attention mechanisms and other standard layers like embedding layer, dense layer, and normalization layers. 

They are commonly used in language tasks such as text classification, question answering, and machine translation. 

There have been [researches](https://arxiv.org/pdf/2101.01169.pdf) that show that they can also be used for computer vision tasks, such as image classification, object detection, image segmentation, and image captioning with [visual attention](https://arxiv.org/pdf/1502.03044.pdf). 

To learn more about the transformer, check out its awesome [paper](https://arxiv.org/pdf/1706.03762.pdf). 


![Screen Shot 2021-09-04 at 23.16.48.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1630790223290/99Ltf-fAy.png)

*Image: Transformers architecture, [Attention Is All You Need](https://arxiv.org/pdf/1706.03762.pdf)*


*********

This is the end of the article. We can summarize the neural networks architectures we discussed by their suites of data: 

* Tabular data: Densely connected neural networks.
* Images: 2D Convolutional neural networks (a.k.a Convnets).
* Texts: Recurrent Neural Networks(RNNs), transformers, or 1D Convnets.
* Time-series: RNNs or 1D Convnets
* Videos and volumetric images: 3D Convnets, or 2D Convnets (with video divided into frames)
* Sound: 1D Convnets or RNNS. 

The machine learning community is so vibrant. It doesn't take long for a promised technique to fade away, or overlooked techniques to emerge unknowingly. Just take an example of recent research that used Multi-Layer Perceptions([MLP-Mixer: An all-MLP Architecture for Vision](https://arxiv.org/abs/2105.01601)) for computer vision claiming that Convnets and transformers are not necessary. 

All that speaks to is that this field will keep evolving, and my hope is that you and I can do all we can to stay up to date without affecting our essential needs as humans. 

*******

Thanks for reading!

Each week, with a probability of 80%, I write one article about machine learning techniques, ideas, or best practices.

If you found the article helpful, share it with anyone who you think would benefit from it, connect with me on  [Twitter](https://twitter.com/Jeande_d), or join my  [newsletter](https://www.getrevue.co/profile/deeprevision).



P.S. [PCA is...](https://twitter.com/Jeande_d/status/1417093660244594688?s=20)
