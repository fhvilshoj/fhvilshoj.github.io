---
title: "ECINN: Efficient Counterfactuals from Invertible Neural Networks"
collection: publications
permalink: /publication/ecinn-efficient-counterfactuals-from-invertible-neural-networks
excerpt: 'We present the first one-pass-algorithm for generating semantically meaningful counterfactual image examples.'
date: 2021-03-16
venue: 'Under review'
paperurl: ''
---

Counterfactual examples identify how inputs can be altered to change the predicted class of a classifier, thus opening up the black-box nature of, e.g., deep neural networks. We propose a method, ECINN, that utilizes the generative capacities of invertible neural networks for image classification to generate counterfactual examples efficiently. In contrast to competing methods that sometimes need a thousand evaluations or more of the classifier, ECINN has a closed-form expression and generates a counterfactual in the time of only two evaluations. Arguably, the main challenge of generating counterfactual examples is to alter only input features that affect the predicted outcome, i.e., class-dependent features. Our experiments demonstrate how ECINN alters class-dependent image regions to change the perceptual and predicted class of the counterfactuals. Additionally, we extend ECINN to also produce heatmaps (ECINNh) for easy inspection of, e.g., pairwise class-dependent changes in the generated counterfactual examples. Experimentally, we find that ECINNh outperforms established methods that generate heatmap-based explanations.

