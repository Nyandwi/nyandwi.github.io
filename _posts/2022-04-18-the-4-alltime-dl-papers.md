---
layout: post
title: The 4 All Time Papers that Revolutionalized Deep Learning, Computer Vision, and NLP in 2010s
permalink: /deep-learning-alltime-papers/
---

[This post was orginally posted on [Twitter](https://twitter.com/Jeande_d/status/1514936993603469316?s=20&t=Lozlx5yaqvpbg6b823IB2Q)]

The decade 2010s is inarguably the host of some of the most important breakthroughs in deep learning algorithms and applications. I think we can all agree on that!

What made those breakthroughs possible are the other good works that were invented many years before. Take a few examples:
- In 1958, Frank Rosenblatt invented a [perceptron](https://en.wikipedia.org/wiki/Perceptron) algorithm that were later implemented in a machine dubbed Mark I Perceptron.
- In 1986, Rumelhart et.al invented [a backpropagation algorithm](https://www.nature.com/articles/323533a0)(backprop) which is the core part of training machine learning systems.
- In 1989, Yann LeCun et.al [applied backpropagation to handwritten zip code recognition](http://yann.lecun.com/exdb/publis/pdf/lecun-89e.pdf) which was *"the earliest real-world application of a neural net trained end-to-end with backpropagation"* as Karpathy also [mentioned](http://karpathy.github.io/2022/03/14/lecun1989/).
- In 1998, Yann LeCun et.al designed [LeNet-5](http://vision.stanford.edu/cs598_spring07/papers/Lecun98.pdf), one of the earliest convolutional neural network and applied it to document recognition - backpropagation algorithm that was introduced 10+ years before also played a key here!

Something that is well-known in science is that *good works always take inspiration from other good works(or even better)*. So, the works listed above are not meant to be exhaustive. That said, let's see 4 papers that I consider to be some of the most important papers that were ever published.

## 1. AlexNet, ImageNet Classification with Deep CNNs, 2012

[AlexNet](https://proceedings.neurips.cc/paper/2012/file/c399862d3b9d6b76c8436e924a68c45b-Paper.pdf
) is inarguably one of the most important papers that were ever published in deep learning and computer vision. It gave a practical proof that convolutional neural networks(ConvNets) work better for large scale image recognition. To day, AlexNet is not a state-of-the-art architecture, but it inspired efficient ConvNet architectures.

>For a bit overview, AlexNet achieved the top-5 error rate of 15.3% on ImageNet Challenge. It had only 8 layers with learnable weights that are convolution and fully connected layers(Some convolution layers were followed by max-pooling layers but max-pooling layers are often omitted from layer count since they don't have learnable parameters).
![AlexNet](/images/alexnet.png)

## 2. R-CNN, Rich Feature Hierarchies for Accurate Object Detection and Semantic Segmentation, 2013

[R-CNN or Region Based-CNN](https://arxiv.org/abs/1311.2524) is one of the early object detectors. Just like how AlexNet introduced deep learning for image classification, R-CNN introduced deep learning for object detection. Before R-CNN, object detectors relied on region propal networks such as [selective search](http://www.huppelen.nl/publications/selectiveSearchDraft.pdf) with some classical ensemble systems.

R-CNN was super slow and it's no longer a state-of-the-art detector but it inspired later efficient detectors such as [Fast R-CNN](https://arxiv.org/abs/1504.08083), [Faster R-CNN](https://arxiv.org/abs/1506.01497v3), [Mask R-CNN](https://arxiv.org/abs/1703.06870), [Cascade R-CNN](https://arxiv.org/abs/1712.00726), [RetinaNet](https://arxiv.org/abs/1708.02002v2), [EfficientDet](https://arxiv.org/abs/1911.09070v7), etc...

And guess what? What differentiated R-CNN from other traditional detectors is using pretrained AlexNet to extract features from region proposals. I think that again speaks to the influence of AlexNet that we discussed previously.

>For a bit overview, R-CNN is two stage detector but in broad, it has has 3 main parts. The first part in R-CNN is selective search network that generate all possible regions that contain objects. The second part is a convolutional neural network(CNN) that extracts features(of fixed length) from each region. The CNN used in R-CNN was pre-trained AlexNet. Using a pretrained backbone network in object detection is a common and recommended thing but today. AlexNet is not used as backbone anymore. You will find most backbones being ResNet, ResNeXT and other better CNNs architectures. The third part is SVM classifier that runs on top of features extracted by CNN to identify the class of the regions and a bounding box linear regressor that predicts bounding boxes of the regions.
![R-CNN](/images/r-cnn.png)

Subsequent detectors improved performance and speed by replacing traditional regional proposal networks(such as selective search) and SVM classifier and linear regressor with a single unified CNN.

## 3. ResNet - Deep Residual Learning for Image Recognition, 2015

[ResNet](https://arxiv.org/abs/1512.03385
) is inarguably one of the most influential architectures in the vision community and even beyond.

Before ResNet, it was hard to train extremely large networks(over 100 and 1000 layers), and almost nobody understood why. People thought that large networks overfit, but it was not actually the case.

ResNet influenced the design of neural network architectures, and not just only for vision but also for [language architectures](https://arxiv.org/abs/2203.00555). After ResNet introduced and proved that residual connections help the large network to converge faster, most new ConvNet architectures had some residual components. Everything became ResNet++![^1].

ResNet explored and answered a very important problem: ***is learning better networks as easy as stacking more layers?***. I wrote more about that problem [here](https://twitter.com/Jeande_d/status/1501188533897216003?s=20&t=SzR9og0teCX5-COmPDKbZw).


## 4. Attention is All you Need - Transformer, 2017

It's not even been longer than 5 years since Transformer was introduced, but it completely transformed NLP and no doubt it will also transform vision and make it easier to do tasks that involve both vision and language(multi-models).

To day, pretty much all large-scale NLP tasks are modelled by Transformer. Currently, Vision Transformers(most notably [ViT](https://arxiv.org/abs/2010.11929)) are also showing great results across different visual recognition tasks.

> For a bit overview,  a Transformer is a class of neural network algorithms that is purely based on attention mechanisms. Transformer doesn’t use recurrent networks nor convolution. It is rather made of multi-head attentions, residual connections, layer normalization, fully connected layers, and positional encodings for preserving the order of sequence in data.
![Attention](/images/attention.png)
Attention image shown above was taken from [ML-Visuals](https://github.com/dair-ai/ml-visuals)


As we are getting to the end of the post, let's make an important note: those 4 papers are not obviously the only important papers that were published in the 2010s. What they did is starting/shaping the league. They inspired nearly all later efficient deep learning algorithms that are used today. Also, as some people replied on the [post](https://twitter.com/Jeande_d/status/1514936993603469316?s=20&t=nXFPFW9E2l59nO3BI2s_3g), we can't dismiss other biggest inventions such as [GANS](https://twitter.com/G_RiveraAlf/status/1515185051683926016?s=20&t=nXFPFW9E2l59nO3BI2s_3g), [word2vec in NLP](https://twitter.com/sujoyrc/status/1515033816821559303?s=20&t=nXFPFW9E2l59nO3BI2s_3g), etc...

For further learning, you can read the paper we discussed:

- [AlexNet, ImageNet Classification with Deep CNNs](https://proceedings.neurips.cc/paper/2012/file/c399862d3b9d6b76c8436e924a68c45b-Paper.pdf
) 
- [R-CNN, Rich Feature Hierarchies for Accurate Object Detection and Semantic Segmentation](https://arxiv.org/abs/1311.2524)
- [ResNet, Deep Residual Learning for Image Recognition](https://arxiv.org/abs/1512.03385
)
- [Transformer, Attention is All you Need](https://arxiv.org/abs/1706.03762)


#### Footnotes

[^1]: Hat tip to Saining He for the term ResNet++ in his [presentation about ConvNeXt](https://rosanneliu.com/dlctfs/dlct_220225.pdf)