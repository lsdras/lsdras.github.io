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

전체적인 논문의 구조는 Fully Convolutional Network를 정의하고 그 영역을 구체화하며, 공간적으로 밀집된 predict과정에서의 적용에 대하 설명하고, 이전의 모델들과의 연관성을 설명하는 파트로 나뉠 것 같네요.

AlexNet, VGG net, GoogLeNet 등 최근의 분류 네트워크들을 FCN으로 적용,개조시키고, fine tuning을 통해 학습된 표현(출력)들을 분할과정으로 전환시킬 것이고요.
깊고 거친 층에 있는 의미론적인 정보와 얕고 fine한 층에 있는 appearance(형태론적인?)정보들을 합친 skip architecture을 정의했습니다.

마지막으론 실험 결과에 대한 설명이 들어있는데, 요약하자면 짧은 추론시간만으로도, 기존 방법들에 비해 각종 데이터셋에서 20% 이상의 성능 개선을 보여줬다고 합니다.

# Intro

Convnet(컨볼루션 네트워크를 이렇게 줄여 쓰네요)의 발전을 얘기하면서, 전체 이미지 분류 뿐만 아니라, 구조화된 output을 내는 과정에서 국소적인 작업까지도 발전했다 하면서, 예시로 bounding box detection, part&keypoint detection, local correspondence를 들고 있습니다.

