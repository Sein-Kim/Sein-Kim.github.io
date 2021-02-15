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

###### 1. Introduction
Probabilistic Matirx Factorization이라는 추전 기법을 설명하기에 앞서서, 우선 Recommendation Systems의 기본적인 개념에 관하여 알아본다.<br>

Recommendation Systems의 strategies는 크게, "Content-based filtering", "Collaborative filtering"으로 나누어져 있다.<br>

- **Content-based filtering**<br>
  사용자가 preference에 관한 explicit information을 제공한다면,
  이를 이용하여 새로운 prediction/suggestion을 하는 방식.<br>
  ex. user A가 어떤 음악(item) B를 들었다면, 그 음악 B의 작곡가인 C의 다른 음악들을 추천하는 것.<br>
- **Collaborative filtering**<br>

이 중, Collaborative filtering을 기반으로 하며, sparse하며 imbalanced한 datasets에서도 작동이 잘 되는 "probabilistic algorithms"을 만드는 것이 이 논문의 목표이다.<br>

###### 2. Probabilistic Matrix Factorization (PMF)
PMF model에서의 notation은 다음과 같다.<br>
- latent user feature matrix : $$ U \in R^{D \times N} $$
- latent item feature matrix : $$ V \in R^{D \times M} $$
- integer rating values : from 1 to $K^1$
- rating of user $i$ for movie $j$ : $R_{i,j}$<br>
- Gaussian distribution (normal distribution) : $$\mathcal{N}(x\mid\mu, \sigma^2)$$
- indicator function (=1 if user $i$ rated movie(item) $j$ and =0 in otherwise) : $$I_{i,j}$$ <br>

또한 PMF model은 **"root mean squared error (RMSE)"** 를 평가지표로 사용한다.<br>

<img src="https://user-images.githubusercontent.com/76777494/107918391-ec08f480-6fac-11eb-9562-11bd86457c77.png" width="40%"><br>
위의 그림은 본 논문에서 PMF model을 간략하게 표현한 것이다.<br>
latent user & item feature matrix의 column vectors $$U_i$$와 $$V_j$$는 표준편차 $$\sigma_U$$와 $$\sigma_V$$를 가지는 standard normal distribution으로 표현된다.<br>
$$U_i$$, $$V_j$$를 통하여, 평균: $$U^T V$$, 표준편차: $$\sigma$$인 $$\hat{R}$$을 형성하며, 이와 rating matrix R을 비교하여, RMSE를 최소화 시키는 방향으로 학습을 진행한다.<br>


우선적으로, 이 논문의 model들은 Bayesian inference를 바탕으로 형성되었다.<br>
$$p(\theta\mid\mathbf{X},\alpha) = \frac{p(\mathbf{X}\mid\theta,\alpha)p(\theta\mid\alpha)}{p(\mathbf{X})}$$
- posterior distribution = $$p(\theta\mid\mathbf{X},\alpha)$$
- likelihood = $$p(\mathbf{X}\mid\theta,\alpha)$$
- prior : $$p(\theta\mid\alpha)$$

위의 bayes rules에 따라, PMF model의 parameters는 bayes inference에서 다음과 같이 표현된다.<br>
- $$\theta$$ = U, V
- $$\mathbf{X}$$ = R
- $$\alpha$$ = $$\sigma^2$$


###### 3. Automatic Complexity Control for PMF Models

###### 4. Constrained PMF

###### 5. Results

###### 6. Codes
아래의 링크는 위 논문을 살펴보고 직접 구현해 본 코드이다.<br>
['PMF codes - blog'](https://sein-kim.github.io/PMF/) <br>
['Constrained PMF codes - blog'](https://sein-kim.github.io/CPMF/) <br>
['PMF and Constrained PMF codes - github'](https://github.com/Sein-Kim/Recommender_Systems/tree/main/PMF) <br>
