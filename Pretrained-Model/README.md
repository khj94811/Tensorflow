# Pretrained Model

- Deep Learning이 발전하며 다양한 네트워크가 개발되었으며, 좋은 성능을 보이는 네트워크들의 레이어가 늘어남에 따라서 네트워크를 훈련시키는데 걸리는 시간 또한 증가하였다.

- ResNet-50은 8개의 P-100을 사용해 ImageNet Classification을 위한 학습에 29시간이 필요했다.

- 최근 더 좋은 결과를 내고있는 NasNet은 AutoML 기법을 이용하여 최적의 네트워크 구조를 스스로 학습하기 때문에 훨씬 더 많은 Training 시간이 필요하다.

- Deep Learning은 개방적인 환경에서 빠르게 발전하고 있기 때문에, 연구자들은 자신이 만든 Pre-trained Model을 인터넷에 올려놓아 다른 사람들이 쉽게 받을 수 있도록 하였다.

- 이런 모델을 그대로 사용할 수도 있지만, Transfer Learning이나 Neural Style Transfer를 통해 재가공 하는 것이 가능하다.

## Tensorflow Hub

- 재사용 가능한 Model을 쉽게 이용할 수 있는 라이브러리

- https://tfhub.dev

- Tensorflow 2.x를 사용하면, Tensorflow Hub 설치는 따로 필요 없고 바로 Library를 불러올 수 있다.

## Transfer Learning

- Transfer Learning은 미리 훈련된 모델을 다른 작업에 사용하기 위해서 추가적인 학습을 시키는 것을 말한다.

- 이때 훈련된 모델은 데이터에서 유의미한 Feature를 뽑아내기 위한 Feature Extractor로 쓰이거나, Model의 일부를 재학습시키기도 한다.

- CNN 전이학습을 예로 들어보자

![CNN Transfer Learning](https://miro.medium.com/max/1400/1*qfQ3hmHLwApXZBN-A85r8g.png)

- 미리 훈련된 CNN을 불러오고, 가장 마지막의 Dense Layer를 제외한다.

- 다음으로 새로운 분류 작업을 위한 레이어를 추가해야한다.

    - 이 때, 잘린 부분에서의 Dense Layer 하나만 추가할 수도 있지만, 조금 더 복잡한 분류 작업을 위해서 여러 개의 Dense Layer와 Dropout Layer를 추가하기도 한다.

- 새롭게 추가된 Layer만 훈련시킬 수도 있고, 훈련된 모델의 일부 레이어를 훈련하는 것도 가능하다.

    - 훈련하지 않은 Layer를 'freeze' 라고 표현한다.

- Google Colab을 이용하여 Training을 해보려고 하였으나,

    - 내 PC에 설정해서 쓰려고 했는데, AMD CPU / GPU 셋트에서 설정하는걸 미루다보니..

        - 왜 Docker Toolkit 쓰려고 하는데 에러가 나는걸까!

        - VM은 쓰기 싫으니, Ubuntu Dualboot 시간날때 꼭 해놓자..
