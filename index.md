---
layout: page
title: CVPR 2021 TUTORIALS
subtitle: Normalization Techniques in Deep Learning: Methods, Analyses, and Applications
---





## **Organizer and Presenter**



<img src=".\img\LeiHuang.jpg" style="zoom: 25%;" />
 	[Lei Huang](https://huangleibuaa.github.io/)																			

​									

## Description of the Tutorial

Normalization methods can improve the training stability, optimization efficiency and generalization ability of deep neural networks (DNNs), and have become basic components in most state-of-the-art DNN architectures. They also have successfully proliferated throughout various areas of deep learning, including but not limited to computer vision, natural language processing, and speech recognition. However, despite the abundance and ever more important roles of normalization techniques, we note that there is an absence of a unifying lens with which to describe, compare and analyze them. In addition, our understanding of theoretical foundations of these methods for their success remain elusive. This tutorial cover normalization methods, analyses and applications, and will address the following questions:

(1) What are the main motivations behind different normalization methods in DNNs, and how can we present a taxonomy for understanding the similarities and differences between a wide variety of approaches?

(2) How can we reduce the gap between the empirical success of normalization techniques and our theoretical understanding of them?

(3) What recent advances have been made in designing/tailoring normalization techniques for different tasks, and what are the main insights behind them?



## Tutorial Outline

This tutorial takes around 3~4 hours.  (The content may have minor variation, based on the continuing research progress until CVPR 2021).

#### (1)  **Introduction of the main motivations behind different normalization methods in DNNs** **(30 min).**  

We will illustrate that most normalization methods are essentially designed to satisfy nearly equal statistical distributions of layer input/output-gradients across different layers during training, in order to avoid the ill-conditioned landscape of optimization: 

a.  We borrow the results from conditioning analysis in optimization to illustrate how normalizing input improve the optimization efficiency theoretically. 

b.  How to extend the theoretical results in optimization from normalizing input towards normalizing activations? We provide an intuitive illustration by connecting to proximal gradients and an approximating theoretic result by analyzing the Fisher information matrix (FIM).

c.  We answer how normalizations relieve gradient explosion or vanishing problem during training. 

 

#### (2) **A comprehensive review of the normalization methods (60 min).**  

We show that one can obtain the desired conditions that lead to well-conditioned optimization landscape by either normalizing the activations or weights, or effectively relieve the negative effects of the ill-conditioned landscape by normalizing the gradients: 

a.  **Normalizing activations by population statistics**. We illustrate certain preliminary methods, prior to batch normalization (BN), that seeks to normalizing activation by using the population statistics. These methods pioneer the way of normalizing activations but suffer from several issues in practice. 

b.  **Normalizing activations as functions.** We decompose the most representative normalizing-activations-as-functions framework into three components: the normalization area partitioning (NAP), normalization operation (NOP) and normalization representation recovery (NRR). We unify most normalizing-activations-as-function methods into this framework and provide insights for designing new normalization methods.

c. **Normalizing weights** **with a constrained distribution**. We analyze what kinds of constraints on weights contribute to the training, and how to solve the optimization problem with constraints. 

d.  **Normalizing gradients.** We show how normalizing gradients in DNNs relieve the negative effects of an ill-conditioned landscape caused by the diversity in magnitude of gradients from different layers. 

 

#### (3) **Our theoretic understanding of normalization (30 min)**: 

We provide clear guidelines for understanding why BN stabilizes and accelerates training, and further improves generalization, through a scale-invariant analysis, condition analysis and stochasticity analysis, respectively.

a.  **Scale invariance in stabilizing training**. We illustrate how the scale-invariant property of normalization methods stabilize the training and affect the learning rate layer-wisely, and what’s the effects of weight decay, when combined with scale-invariant normalization methods.

b.  **Improved conditioning in optimization**. We show how BN improves the conditioning of the optimization problem, and what’s the recent progress in theoretical analyses on normalized networks, from the perspective of optimization.

c.  **Stochasticity for generalization**. How BN introduces the stochasticity, and how to mathematically model the stochasticity and empirically measure the stochasticity of BN. 

 

#### (4) **Normalization for applications (60 min)**: 

We show that the normalization methods can be used to ‘edit’ the statistical properties of layer activations. These statistical properties, when designed well, can represent the style information for a particular image or the domain-specific information for a distribution of a set of images. This characteristic of normalization methods has been thoroughly exploited in CV tasks and potentially beyond them:

a.  **Normalization for domain adaptation**. We illustrate how normalization can be used to align the distributions of activations for different domains in domain adaptation. We also illustrate how to exploit BN to learn the domain specific information, while other convolutional/linear parameters to learn domain invariant representation. These ideas can be further used to learn universal representation for multiple task learning.

b.  **Normalization for style transfer**. We provide how the statistical information of an internal layer can represent a style of an image, and how normalization can be used to disentangle the style from the content. This idea can be further used for more general image translation tasks.

c.  **Normalization for training generative adversarial networks (GANs)**. We show the recent theoretical and empirical progresses of normalization in training GANs. 

d.  **Normalization for efficient deep models**. We show how to exploit normalization for network slimming and how to effectively quantize networks with BN. 

 



## Presenter's Bio

Lei Huang is currently an associate professor at [State Key Laboratory of Software Development Environment](http://www.nlsde.buaa.edu.cn/), Institute of Artifical Intelligence, Beihang University, China. He received his BSc and PhD degrees, respectively in 2010 and 2018, at the School of Computer Science and Engineering, Beihang University, China. From 2015 to 2016, he visited the Vision and Learning Lab, University of Michigan, Ann Arbor. He was a research scientist in Inception Institute of Artifical Intelligence (IIAI), UAE. His current research mainly focuses on normalization techniques (involving methods, theories and applications) in training DNNs. He also has wide interests in deep learning theory (representation & optimization) and computers vision tasks. He serves as a reviewer for the top conferences and journals such as CVPR, ICCV, ECCV, NIPS, AAAI, IJCAI, JMLR, IJCV, TNNLS, etc.