---
title: "MeLIME: Meaningful Local Explanation for Machine Learning Models"
collection: publications
permalink: /publication/melime-meaningful-local-explanations-for-machine-learning-models
excerpt: 'We present ideas on how to improve the highly popular explanation method LIME.'
date: 2020-09-12
paperurl: 'https://arxiv.org/abs/2009.05818'
venue: arXiv
---

In this work, we introduce ideas on how to improve the popular explanation method LIME.
In particular, we introduce density estimators, such as Kernel Density Estimation and VAEs, to improve the local sampling process of LIME. 
In turn, we obtain local samples that are more likely to be situated on the manifold, which the original training data was sampled from.
This yields more trustworthy local interpretable models.

To further improve the trustworthyness of the local interpretable models, we also introduce a stopping criteria which helps stop fitting the local model only when the model no longer changes significantly. 
Such improvement results in more robust local explanations.
