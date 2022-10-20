## 4. Semantic Segmentation

: 해당 픽셀이 어느 카테고리에 속하는지 분류하는 것

: 만약에 사람이 두명이 겹쳐있다면 같은 클레스지만 다른 물체로 구별함



활용범위

- Medical images
- Autonomous driving
- Computational photography
- etc...



### 2. Semantic segmentation architectures

: Fully convolutional networks (FCN)



Fully connected layer

: classification의 마지막 단에 가장 많이 활용

: 공간 정보를 고려하지 않음



 Fully convolutional layer: 

: 입력이 activation함

: 1 by 1 convolution으로 구성이 되어 있음

7:46