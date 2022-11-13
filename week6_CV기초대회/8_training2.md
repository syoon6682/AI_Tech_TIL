## 8. Training & Inference

 

### Training Process

model.train() : train mode



optimizer.zero_grad()

: epoch은 전체 단위의 for loop

: zero_grad의 의미 - 각각의 parameter들의 수치를 초기화하면서 현재 batch만 반영



loss

: criteriion을 넣어주고 작성

: loss를 마지막으로 chain 작성



loss.backward()



optimizer.step()

: 꼭 매 step 마다 진행할 필요는 없음 -> 3~4번째 step마다 하는 걸 gradient accumulate라고 함

: optimizere도 step 진행 후 zero_grad 해주기



### Inference Process

model.eval() : eval mode



: 추론 과정에 validation set이 들어가면 그것이 검증

fit이라는 함수 하나로 train을 lightining하게 가능 -> 그러나 pytorch를 먼저 숙달하기