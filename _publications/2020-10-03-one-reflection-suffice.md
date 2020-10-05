---
title: "One Reflection Suffice"
collection: publications
permalink: /publication/one-reflection-suffice
excerpt: 'We prove that compositions of many Householder reflections can be replaced with one "auxillary reflection." Such replacement yields higher GPU utilization and thus speeds up training and inference.'
date: 2020-10-03
paperurl: 'https://arxiv.org/abs/2009.14554'
venue: [Under review]
---

Orthogonal weight matrices are used in many areas of deep learning. Much previous work attempt to alleviate the additional computational resources it requires to constrain weight matrices to be orthogonal. One popular approach utilizes *many* Householder reflections. The only practical drawback is that many reflections cause low GPU utilization. We mitigate this final drawback by proving that *one* reflection is sufficient, if the reflection is computed by an auxiliary neural network.

