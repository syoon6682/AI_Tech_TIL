## 4. AutoGrad & Optimizer

: layer를 쌓고 backpropagation을 통해 돌아가서 weight를 업데이트! 

: block = layer



### nn.parameter

: Tensor 객체의 상속 객체

: nn.Module 내에 attribute가 될 때는 required_grad=True로 지정되어 학습 대상이 되는 Tensor

: 우리가 직접 지정할 일은 잘 없음

-> 대부분의 layer에는 weights값들이 저장되어 있음



forward = 해당하는 parameter와 bias값을 계산하여 다음 layer로 보냄

backward = 미분하는 작업까지 포함시킴! 정말 대단해! 