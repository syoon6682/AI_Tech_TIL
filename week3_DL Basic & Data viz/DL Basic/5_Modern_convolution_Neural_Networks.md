## 5. Modern Convolution Neural Networks

ILSVRC

: ImageNet Large-Scale Visual Recognition Challenge



AlexNet:

- 11x11 filter를 활용
- 5 convolutional layers, 3 dense layers
- ReLU 활용 - 이유는 잘 모르겠지만 잘 되는 activation function



### ReLU

- Linear model이 가지고 있는 좋은 성질을 잘 가지고 있음

  -> 경사하강이 용이함



VGGNet

- 3x3 convolution filter 활용

- 1x1 convolution for fully connected layers를 활용했지만 생각보다 중요하진 않음

  -> 이걸로 파라미터가 줄어든 것은 아님!



3x3, 5x5?

3 by 3 2개를 활용하는 것이 5 by 5 하나를 활용하는 것과 같다. 

그러나 파라미터 수에서는 3 by 3이 더 효율적!

-> 그래서 필터의 크기를 줄이고 layers를 늘리는 것이 훨씬 낫다!



GoogLeNet

: 1 by 1을 중간에 잘 활용해서 parameter 수를 줄이는 것! 

: network in network 구조 (NIN 구조)

: convolution filter 들어가기 전에 1 by 1 filter가 한번 들어감 

-> 파라미터를 줄이게 됨

-> 어떻게: 채널 방향으로 parameter를 줄일 수 있다!  (이거 교재 꼭 확인하기! 아이디어 참신하네..)



ResNet

: 그 kaiming이 작성한 논문..!

layer를 더 늘린다고 학습이 잘되진 않는 현상이 발생



- identity connection 추가
- 차이만 학습한다..? (residual 활용)
- projected shortcut은 활용이 많이 되진 않는다..!
- 이때 residual은 차원이 다르기 때문에 차원을 맞춰주기 위해 앞뒤로 1 by 1 convolution layer 활용



DenseNet

ResNet은 더하지만 얘는 concatenation함

what is concatenate? 



대부분 프젝은 resnet 구조 혹은 densenet 구조를 가지고 진행!

summary 꼭 보고 넘어가기 