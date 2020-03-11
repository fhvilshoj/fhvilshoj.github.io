---
title: "K-Means Clutering"
date: 2019-03-09
author: frederik
permalink: /ml-notes/2019-03-16-k-means
tags:
  - ML Notes
  - K-Means
---
The K-Means problem is an unsupervised problem, where the task is to group
elements into clusters such that elements in the same cluster are similar (for
some measure of similarity) and points from different clusters are dissimilar.

## Dissimilarity:
Dissimilarities $D(x, x')$ must have the following properties:  
1. $D(x, x') \geq 0, \quad \forall x, x'$  
2. $D(x, x) = 0$  
3. $D(x, x') = D(x', x)$  

The third property is assuring that $D$ is symmetric. This is e.g., not the case for
the KL-divergence.

## K-means clustering derivation
Consider the following setup:

 - **Data:** $\{x_1, \dots, x_N \} \in \mathbb{R}^p$   

 - **Encoder:** $C: \{ 1, 2, \dots, N\} \rightarrow \{1, \dots, K\}$, $K \ll N$.  

Here, the encoder is the function that maps each datapoint to a 
particular cluster. The, we would like to find the cluster representatives,
that minimizes the in cluster distance. More formally, this can be formulated
by a cost function $\mathcal{J}$. (I think that this cost function is called
the distortion). 

$$
\mathcal{J} = \sum_{k=1}^K \sum_{C(x_i) = k} ||x_i - \mu_k||^2
$$

where $\mu_1, \dots, \mu_K \in \mathbb{R}^p$

So the objective is the following:

$$
\min_{\mu_1, \dots, \mu_K} \mathcal{J}
$$

To minimize $\mathcal{J}$, we can diferentiate it and set it to $0$. (because $\mathcal{J}$
is convex in $\mu_k$).

$$
\frac{\partial \mathcal{J}}{\partial\mu_k} = \sum_{C(x_i)=k} \frac{\partial \mathcal{J}}{\partial \mu_k} ||x_i - \mu_k||^2 = \sum_{C(x_i)=k} \left(x_i^\intercal x_i - 2x_i^\intercal \mu_k + \mu_k^\intercal \mu_k\right)
  = \sum_{C(x_i)} \left(-2x_i + 2 \mu_k \right)
$$

Now, set to zero

$$
\sum_{C(x_i) = k} \left(-2x_i + 2 \mu_k \right) = 0 \Rightarrow \sum_{C(x_i) = k} \mu_k = N_k \mu_k \Rightarrow \hat{\mu}_k = \frac{1}{N_k} \sum_{C(x_i) = k} x_i
$$

Where $N_k = \|\\{x_i \| C(x_i) = k\\}\|$. So now we know that we must set $\hat\mu_k = \frac{1}{N_k} \sum_{C(x_i) = k} x_i$.


# K-means and Gaussian mixtures (the relation)

K-means turns out to be a special case of GM:
We consider the model, where we assume that the covariance matrices are
basicaly identities $\Sigma = \Sigma_k = \epsilon I_p$. (Plug it into 
the multivariate normal and reduce to get the formula from slides.

Next step, consider what happens, when $\epsilon$ goes to zero.
In that case, the $\mu_k$ that has the smallest descrepancy norm
with the point will become the dominant.

for small $\epsilon > 0$

$$
a_i = \frac{1}{2}||x_n - \mu_i||^2
$$

$$
\exists j_0 : a_{j_0} < a_k \Rightarrow -a_{j_0} > - a_k \Rightarrow - \frac{1}{\epsilon} a_{j_0} \gg - \frac{1}{\epsilon} a_k \Rightarrow e^{- \frac{1}{\epsilon} a_{j_0}} \gg e^{-\frac{1}{\epsilon}a_k}
$$

$$
\not\exists j_0 : a_k < a_{j_0} \Rightarrow 0 < a_j - a_k
$$

In the case where $k$ is the smallest value, we have that 

$$
\begin{align}
\ast &= \frac{\hat \pi_k e^{-\frac{1}{\epsilon}a_n}}{\sum_{j=1}^K \hat \pi_j e^{- \frac{1}{\epsilon} a_j}}\\
&= \frac{\hat \pi_k e^{-\frac{1}{\epsilon}a_n}}{\hat \pi_k e^{--\frac{1}{\epsilon}a_n} + \sum_{j\neq k}^K \hat\pi_k e^{-\frac{1}{\epsilon}a_j}} \\
&= \frac{1}{1+\sum_{j \neq k} \frac{\hat\pi_j}{\hat\pi_k} e^{-\frac{1}{\epsilon}(a_j - a_k)}}
\end{align}
$$

Note how the sum in the denumerator is approximately $0$, which means that we will get 

$$
\ast = \left\{
\begin{matrix}
0 & \text{if } a_k \text{ is not smallest}\\
1 & \text{if } a_k \text{ is smallest}
\end{matrix}
\right.
$$

It turns out, that both the E-step, the M-step, and the log-likelihood are generalizations og the cluster update step, reassignment step, 
and the distortion, respectively. 

# Practical Issues with K-means
(Choice of initial clusters)

In the K-means algorithm, we initially select $K$ clusters at random. The solution we will end up finding
will be a local minima. For this reason, we might end up at a bad solution, if we are unlucky and initialize
choose a bad assignment of clusters. 

In this section, we will see how we can try to fight this problem.
An obvious solution would to just run the algorithm multiple times
for different initial assignments of the mean values. Then selecting
the clustering that gives the smallest distortion.

## K-means ++
In [Arthur and Vassilvitskii, 2007], they present an algorithm for 
selecting initial clusters. The algorithm goes as follows:

```
initialize choose c1 at random the xi's and set C = {c1}
For k = 1 : K
Compute D(xi) = min c\in C ||xi - c|| for i = 1, ... , N
Choose ck with probability pi prop. D(xi)^2
Let C = C \cup {ck}
```

This algorithm has a bound on the initial distortion $\phi$ as compared
to the optimal distortion $\phi_{OPT}$: 

$$
\mathbb{E}[\phi] \leq 8(\log K + 2 ) \phi_{OPT}
$$

The proof can be found in the article.


