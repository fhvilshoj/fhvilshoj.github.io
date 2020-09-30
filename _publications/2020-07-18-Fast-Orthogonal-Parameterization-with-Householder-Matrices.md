---
title: "Faster Orthogonal Parameterization with Householder Matrices"
collection: publications
permalink: /publication/fast-orthogonal-parameterization-with-householder-matrices
excerpt: 'The paper presents a fast parallel algorithm for multiplying an orthogonal matrix, parameterized by a sequence of Householder matrices, with an input vector'
date: 2020-07-18
venue: 'ICML Workshop on Invertyible Neural Networks, Normalizing Flows, and Explicit Likelihood Models'
paperurl: 'https://invertibleworkshop.github.io/accepted_papers/pdfs/10.pdf'
---

Orthogonal matrices have been used in several Normalizing Flows .
 Orthogonal matrices are attractive since they are easy to invert and have Jacobian determinant one. 
Their main downside is the additional computational resources required to perform gradient descent. 
We identify a computational bottleneck for previous work on Householder matrices, and introduce a novel algorithm, FastH, which 
circumvents the bottleneck and is up to $29\times$ faster than a previous method. 

BibTeX:
```
@inproceedings{fasth,
    title={\{F}aster {O}rthogonal {P}arameterization with {H}ouseholder {M}atrices},
    author={Mathiasen, Alexander and Hvilsh{\o}j, Frederik and J{\o}rgensen, Jakob R{\o}dsgaard 
    and Nasery, Anshul and Mottin, Davide},
    booktitle={\{ICML} Workshop on Invertible Neural Networks and Normalizing Flows},
    year={2020}
}
```
