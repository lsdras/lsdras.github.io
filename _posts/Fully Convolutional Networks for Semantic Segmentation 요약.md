---
title: "Fully Convolutional Networks for Semantic Segmentation 논문 요약"
date: 2018-10-01
categories: CNN, ML, Semantic Segmentation, 논문
---
# Fully Convolutional Networks for Semantic Segmentation

위 논문:(https://people.eecs.berkeley.edu/~jonlong/long_shelhamer_fcn.pdf)을 읽고 제가 이해하는 한 최대한 요약해 설명해보고자 합니다.

# Abstract

Convolutional networks는 계층적 피쳐를 얻을 수 있는 강력한 시각적 모델이고, sementic segmentation 분야에서 계속 발전하고 있다는 말로 문장을 시작하고 있습니다.
이 논문의 주제인 Fully Convolutional Network에 대한 간략한 소개로 남은 abstract를 채우고 있는데, "임의의 사이즈를 가진 image를 input으로 넣었을 때, 효과적인 추론과 학습 과정을 동반한 output을 만드는 법" 정도로 이 논문이 쓰인 basic한 목적을 파악할 수 있을 것 같네요.

전체적인 논문의 구조는 Fully Convolutional Network를 정의하고 
