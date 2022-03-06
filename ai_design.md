---
layout: page
title: Blogs
---

## AI Design: Testing Vision Transformers on Design Images
This blog article is written by [Sun-Young HA](https://medium.com/@sunyoungha) & Stefan PASCH
![design_transformers](assets/img/ai_design/design_transformers2.jpg)

In recent years, advancements in artificial intelligence have been omnipresent. AI is applied in various fields and for various applications, such as *language translation, customer segmentation*, or *fraud detection*. An obvious form of AI that could support and complement the work of designers are algorithms that are able to detect images and understand various features of images with potential applications in design: For example, an AI that can classify fashion in different categories, can detect furniture in images of interior design, or classify the design style in images.


While initial forms of AI could only conduct very narrow image tasks, e.g. distinguish the image of a dog from a cat image, in recent years, AI shows increasingly general abilities to detect and analyze images. In this article, we will focus on a particular kind of AI, so-called **transformer-based models** that simultaneously provide visual and language understanding. As we will see, these models inherit, on the one hand, a remarkable general understanding of images and, on the other hand, can be applied fairly flexible for different purposes.

We find that vision transformers, in fact, show a solid performance in various tasks, on a dataset of IKEA interior design images, suggesting that such tools could become increasingly important for designers.

### A Very Short History of ‘Image Recognition’

20 to 30 years ago, most computer-assistant programs relied on **rule-based approaches**, that is, computers are given well-defined rules on how to behave in certain situations. For example, a bank may use the algorithm to decline all loan requests when the client’s balance is below -1000$ and grant all loans for higher balances. As images are extremely complex, however, these simple if-then conditions fall short when trying to analyze images. Say, for example, you would like to develop an algorithm that is able to distinguish between images of cats and dogs. When considering the image of a cat, one realizes how difficult it is to put into words what actually makes it a picture of a cat. A cat has two eyes, two ears, and a nose, but so have dogs and humans. So, simple **if-then-conditions** won’t help us much here.

That’s where **neural networks** jumped in. Roughly speaking, neural networks reflect a complex relationship between input variables (the color shades of an image) and an output variable (cat or dog) by using thousands, often millions, of neurons/parameters. By doing so, neural networks, can detect nuanced differences between images, for example, distinguish the shape of ears or eyes, or learn what kind of postures cats and dogs tend to have. This resulted in remarkable performances in image classification, like distinguishing a dog from a cat image. However, a huge downside remained: An AI could be only applied to the narrow task it had been trained on. For instance, an AI trained to distinguish cats from dogs could not detect a human. Hence, each specific application needs a particular dataset and training.

### Vision Transformers

The basis for the **visual-language model** we discuss, actually, stems from the field of **text-based AI (NLP — Natural Language Processing)**. Here, in recent years there has been a shift away from keyword- and rule-based approaches, towards large neural networks that contain a general understanding of language. Most notably, in 2018, Google introduced there **BERT (Bidirectional Encoder Representations from Transformers)** that could set new high scores in various NLP tasks, such as *question answering* and *text classification*. For example, BERT understands that the search phrase “2019 brazil traveller to USA need a visa” wants to know about a Brazilian applying for VISA in the U.S. and about a U.S. citizen in brazil.

The basic idea behind this technology is that large neural networks are trained on different language tasks, such as predicting which word belongs to a particular sentence, allowing the model to learn a general understanding of language. This “*general language understanding*” can then be applied and fine-tuned on particular problems, such as text classification.

