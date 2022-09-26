## 2. PyTorch Basics



### PyTorch Operations

: numpy + AutoGrad



### Tensor

: 다차원 Arrays를 표현하는 PyTorch 클래스

: 사실상 numpy의 ndarray와 동일 (그러므로 TensorFlow의 Tensor와도 동일)

: Tensor를 생성하는 함수도 거의 동일

-> 하지만 대부분의 tensor를 생성을 직접해서 구현하는 일은 별로 없다..!

:reshape 대신에 view를 써줘야한다..! contiguity(메모리 보장) 차이

:  squeeze, unsqueeze -> 차원이 1인 차원을 삭제하거나 추가

: numpy와 같이 array 간 연산을 지원해줌



