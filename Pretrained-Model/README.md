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