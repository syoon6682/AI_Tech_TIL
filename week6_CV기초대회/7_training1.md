## 7. Training

loss

optimizer 

metric



### loss

: 역전파

: error의 수치를 나타냄

loss 함수 = cost함수 = error함수

loss 함수 선택에 따라 parameter 업데이트도 달라짐

nn 패키지에 제공을 해줌 -> 모델을 상속한 하나의 클래스

criterion으로 사전에 loss함수 넣어줌



### Optimizer

: 어느 방향으로 얼마나 움직일지?



LR scheduler

: learning rate를 조절해주는 도구



StepLR

: 특정 Step마다 LR 감소



ReduceLROnPlateau

: 더 이상 성능 향상이 없을 때 LR 감소



### Metric

: 모델의 평가 (like f1-score)

: 학습된 모델을 객관적으로 평가하는 지표