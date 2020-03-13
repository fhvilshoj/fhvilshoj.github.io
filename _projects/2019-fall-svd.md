---
title: "What if Neural Networks had SVDs?"
type: "In Review"
permalink: /projects/2019-fall-what-if-neural-networks-had-svds
date: 2019-10-15
venue: ICML 2020
tags:
  - Invertible Neural Networks
  - Linear Algebra
  - Machine Learning
---
Various Neural Networks employ time-consuming matrix operations like matrix inversion. 
Many such matrix operations are faster to compute given the Singular Value Decomposition (SVD). 
Techniques from [1, 2] allow using the SVD in Neural Networks without computing it. 
In theory, the techniques can speed up matrix operations, however, in practice, they are not fast enough.  
We present an algorithm which is up to $27 \times $ faster than a previous approach, fast enough to speed up several matrix operations. 

The full article will soon be available on ArXiv.

[1] Zhang, J., Lei, Q., and Dhillon, I. Stabilizing Gradients forDeep Neural Networks via Efficient SVD Parameteriza-tion. In ICML, 2018.
[2] Mhammedi, Z., Hellicar, A., Rahman, A., and Bailey, J.Efficient Orthogonal Parametrisation of Recurrent Neu-ral Networks Using Householder Reflections. In ICML,2017.
