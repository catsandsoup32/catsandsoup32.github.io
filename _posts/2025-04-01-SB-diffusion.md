---
layout: distill
title: Schrödinger Bridge Diffusion
description: KL divergence, diffusion, optimal transport [WIP]
tags: machine-learning 
giscus_comments: false
date: 2025-04-01
featured: true
mermaid:
  enabled: true
  zoomable: true
code_diff: true
map: true
chart:
  chartjs: true
  echarts: true
  vega_lite: true
tikzjax: true
typograms: true


toc:
  - name: KL divergence
  
---

## KL divergence

- The *Kullback-Leibler* divergence is a non-symmetrical quantification of the difference between two probability distributions
- The KL divergence of $q(x)$ from $p(x)$ (where $x$ is a discrete random variable) measures the information lost if $q(x)$ were 
  used to approximate $p(x)$ 
- Quantified as the expected extra bits required to code samples of $p(x)$ using a code based on $q(x)$ rather than $p(x)$:
    
  $$ D(p(x) || q(x)) = \sum_{x\in X} p(x) \log \frac{p(x)}{q(x)}$$


### Entropy 

- KL divergence is also termed relative entropy
- The relationship between Shannon entropy, cross-entropy, and relative entropy can be written as follows (for discrete random variable $x$):
  
  $$ D(p(x) || q(x)) = Q(p(x) || q(x)) - H(p(x)) $$

  <details>
    <summary>Proof (by definition)</summary>
    
    $$ 
    \begin{align*}
    D(p(x) || q(x)) &= \sum_{x\in X} p(x) [\log p(x) - \log q(x)] \\
    &= - \sum_{x\in X} p(x) \log q(x) + \sum_{x\in X} p(x) \log p(x)  \\ 
    &= Q(p(x) || q(x)) - H(p(x))  \quad \Box
    \end{align*}
    $$ 

  </details>

- In other words, the relative entropy (extra bits needed using predicted distribution) is the cross-entropy (total bits using predicted distribution) minus the Shannon entropy (inherent bits using true distribution)


## Diffusion 

(TODO)






## References
\[1\] https://www.stat.cmu.edu/~cshalizi/754/2006/notes/lecture-28.pdf

\[2\] https://hanj.cs.illinois.edu/cs412/bk3/KL-divergence.pdf