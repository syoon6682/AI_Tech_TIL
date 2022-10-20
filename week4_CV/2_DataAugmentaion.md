## 2. Data augmentation



### 1. Data augmentation

neural network = data를 압축하는 것

하지만 카메라로 찍은 데이터와 실제 데이터는 차이가 있음 -> 버려지는 데이터가 상당히 많다. 

bias된 데이터가 많다. 

샘플된 데이터와 실제 데이터를 최대한 맞춰주기 위한 방법이 augmentation!



방법

1. 밝기를 다양하게 가져감 -> numpy로 일정한 숫자를 다 더해주면 됨
2. 회전을 줌 -> rotate 함수를 활용하여 진행
3. crop -> numpy indexing을 활용하여 진행
4. affine transform -> 대응쌍을 넣고 getAffineTransform 함수를 넣어서 변환
5. cut and mix

-> 이런 것들을 random하게 활용하는  RandAugment -> 성능이 쉽게 증가함



### 2. Leveraging pre-trained information

transfer learning: 미리 학습시켜놓은 데이터를 활용해서 연관된 새로운 task에 성능을 높이는 방법

한 데이터셋에서 배운 지식을 다른 데이터셋에서 활용하는 방법



knowledge distillation: 이미 학습된 모델에서 지식을 넘겨주는 방법 -> 모델 압축 방법이라고 볼 수 있다. 

먼저 학습된 모델에 output에 loss를 student model에 반영해줌



hard label vs soft label

hard label = one hot vector (0 1 0)

soft label = (0.14 0.8 0.06)



temperature

soft label의 값을 극단적으로 벌려주는 역할을 함 (교재 공식 참고)

semantic information을 고려하지 않는다. -> 내부 각각의 의미가 중요한 것은 아니다. 



Distillation loss

: KLdiv(Soft label, Soft prediction)



student loss

: CrossEntropy(Hard label, Soft prediction)



-> 둘 다 합쳐서 씀, 저 둘의 활용을 잘 알아보기 



### 3. Leveraging unlabeled dataset for training

: unlabeld data를 쓰는 방법 -> 대부분은 unlabeled data인데 적은 수의 labeled data와 많은 수의 unlabeled data를 활용하는 방법! -> semi-supervised 방법



label data로 먼저 모델링 -> unlabeled dataset으로 pseudo-label만들고 재학습 .....진짜 간단한데??



self-training 연구가 지평을 열었다..!

augmentation + Teacher-Student networks + semi-supervised