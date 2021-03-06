---
title: "Backpropagating through Fréchet Inception Distance"
collection: publications
permalink: /publication/backpropagating-through-frechet-inception-distance
excerpt: 'The paper presents a fast algorithm, FastFID, for computing the Fréchet Inception Distance (FID) on a small bacth. The algorithm allows monitoring the FID of GANs during training and even training GANs with FID as a loss.'
date: 2021-02-04
paperurl: 'https://arxiv.org/abs/2009.14075'
venue: 'arXiv'
---

The Fréchet Inception Distance (FID) has been used to evaluate thousands of generative models. 
We present a novel algorithm, FastFID, which allows fast computation and backpropagation for FID. 
FastFID computes the true FID value but is faster than previous algorithms; in theory and practice. It is even fast enough to train GANs directly with FID as a loss. 

For a presentation on the paper, see [here]({{ site.baseurl }}{% link _talks/2021-05-05-Fast-FID.md %}).


