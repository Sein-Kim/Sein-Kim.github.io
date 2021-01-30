---
title: 추천시스템 Probabilistic Matrix Factorization
layout: single
use_math: true
---

Ruslan Salakhutdinov and Andriy Mnih. ['Probabilistic Matrix Factorization'](https://papers.nips.cc/paper/2007/file/d7322ed717dedf1eb4e6e52a37ea7bcd-Paper.pdf)

###### Abstract
많은 collaborative filtering에 대한 접근은 많은 datasets을 다룰 수 없을 뿐더러, sparse한 datasets을 다루는 데에도 어려움이 많다.
이 논문에서는 Probabilistic Matrix Factorization (PMF) 모델을 소개하고 있다.
PMF는 관측 횟수에 따라 선형적으로 스케일 되는 모델이며, large, sparse, imbalanced한 datasets에 대하여 좋은 성능을 보여준다.
우선 PMF에 관하여 설명하고, 그 후 adaptive prior을 사용한 PMF모델, 마지막으로 유저의 preferences를 모든 item에 대하여 적용한 constrained PMF에 관하여 살펴보겠다.

###### Codes
아래의 링크는 위 논문을 살펴보고 직접 구현해 본 코드이다.
['PMF codes - blog'](https://sein-kim.github.io/PMF/)
['Constrained PMF codes - blog'](https://sein-kim.github.io/CPMF/)
['PMF and Constrained PMF codes - github'](https://github.com/Sein-Kim/Recommender_Systems/tree/main/PMF)
