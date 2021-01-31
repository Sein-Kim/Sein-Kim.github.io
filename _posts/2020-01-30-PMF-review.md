---
title: "[추천시스템] Probabilistic Matrix Factorization"
layout: single
use_math: true
---

Ruslan Salakhutdinov and Andriy Mnih. ['Probabilistic Matrix Factorization'](https://papers.nips.cc/paper/2007/file/d7322ed717dedf1eb4e6e52a37ea7bcd-Paper.pdf)
<br>
###### Abstract
collaborative filtering에서 나아가 large, sparse한 datasets를 다루기 위하여,<br>
이 논문에서는 Probabilistic Matrix Factorization (PMF) 모델을 소개하고 있다.<br>
우선 PMF에 관하여 설명하고, 그 후 adaptive prior을 사용한 PMF모델, 마지막으로 유저의 preferences를 모든 item에 대하여 적용한 constrained PMF에 관하여 살펴보겠다.<br>

###### Introduction

###### Probabilistic Matrix Factorization (PMF)
  - latent user feature matrix $$ U \in R^(D \times N) $$
###### Automatic Complexity Control for PMF Models

###### Constrained PMF

###### Results

###### Codes
아래의 링크는 위 논문을 살펴보고 직접 구현해 본 코드이다.<br>
['PMF codes - blog'](https://sein-kim.github.io/PMF/) <br>
['Constrained PMF codes - blog'](https://sein-kim.github.io/CPMF/) <br>
['PMF and Constrained PMF codes - github'](https://github.com/Sein-Kim/Recommender_Systems/tree/main/PMF) <br>
