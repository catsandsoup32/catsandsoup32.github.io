---
layout: distill
title: Schrödinger Bridge Diffusion
description: KL divergence, diffusion, optimal transport [WIP]
tags: machine-learning 
giscus_comments: true
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
- Mathematically, 
  
  $$ D(p(x) || q(x)) = \sum_{x\in X} p(x) \ln \frac{p(x)}{q(x)}$$

### Smoothing:

- In a machine learning context, $q(x)$ is a prediction, and so can easily be a tiny number
- To avoid a divergence value towards infinity, a small constant $\epsilon$ can be added 

### Connection to Shannon entropy

https://www.stat.cmu.edu/~cshalizi/754/2006/notes/lecture-28.pdf
https://hanj.cs.illinois.edu/cs412/bk3/KL-divergence.pdf
