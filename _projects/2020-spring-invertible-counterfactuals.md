---
title: "Counterfactuals from Invertible Neural Networks"
type: "Ongoing"
permalink: /projects/2020-spring-invertible-counterfactuals
date: 2020-03-01
tags:
  - Invertible Neural Networks
  - Counterfactuals
  - Explainability
---
"How can I make a _minimal_ and _realistic_ change to an input such that the predicted outcome change?"
This is the answer which I am aiming to answer using invertible Neural Networks.
The idea relates a lot to pre-imaging from, e.g., kernel-methods.

The idea is the followig. Learn a non-linear and invertible transform $f$ on your data. 
Compose this transform with a linear binary classifier to get a predictive model.
From this construction, you can train the composition using, e.g., binary cross-entropy.
So produce a counterfactual example, one can then take an embedded feature vector and 
shift it onto the decision-boundary of the linear classifier before inverting the shifted
embedding. The idea is illustrated below.

<div style="text-align: center">
	<img src="/images/content/counterfactual.svg" style="width:80%;"/>
	<p><strong>Figure 1.</strong> Illustration of the construction of counterfactual examples. First a point $x$ is mapped 
	by $f$ into the $Z$-domain. Then the embedding is shifted to the decision boundary, before being mapped back into the $X$-domain.</P> 
</div>

Preliminary experiments on the GLOW network from [1] shows promissing results.

[1] Kingma, D.P. and Dhariwal, P., 2018. Glow: Generative flow with invertible 1x1 convolutions. In Advances in Neural Information Processing Systems (pp. 10215-10224).
