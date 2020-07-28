---
title: "What if Neural Networks had SVDs?"
collection: publications
permalink: /publication/fast-orthogonal-parameterization-with-householder-matrices
excerpt: 'The paper presents a fast parallel algorithm suited for GPUs which works for a reparameterization of an SVD in a Houdsholder decomposition. We demonstrate high speed-ups in practice.'
date: 2020-12-01
venue: '[Under review] NeurIPS 2020'
---

Various Neural Networks employ time-consuming matrix operations like matrix inversion. 
Many such matrix operations are faster to compute given the Singular Value Decomposition (SVD). 
Techniques from recent work allow using the SVD in Neural Networks without computing it. 
In theory, the techniques can speed up matrix operations, however, in practice, they are not fast enough.  
We present an algorithm that is fast enough to speed up several matrix operations.
The algorithm increases the degree of parallelism of an underlying matrix multiplication $H\cdot X$ where $H$ is an orthogonal matrix represented by a product of Householder matrices.
