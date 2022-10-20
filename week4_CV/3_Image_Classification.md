## 3. Image Classification

깊어진 network의 문제

1. Gradient vanishing / exploding
2. Computationally complex
3. Overfitting인 줄 알았으나 Degradation problem



### GoogLeNet

Inception module을 활용하여 여러개의 convolution layer를 거치게 함

이때 parameter수가 많이 늘어나게 되는데 이를 위해 1x1 convolution layer를 활용!

-> 이를 통해 계산에 이득을 가져옴 -> 이를 bottleneck layer라고 부름(자료 꼭 확인하기)

-> 층의 개수를 줄이는 역할



전체적인 구조

stem network, Stacked inception modules, Auxiliary classifiers











 



