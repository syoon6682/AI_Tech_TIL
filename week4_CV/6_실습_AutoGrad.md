## 6(실습)  AutoGrad



Autograd

: Automatic gradient calculating API

: Deep Learning library

-> deeplearning을 하는 것에 난이도를 확 낮춤!



```python
# y 미분 X gradients
x = torch.randn(2, requires_grad = True) # requires_grad = True -> x는 gradient를 가질 수 있는 변수!
y = x*3
gradients = torch.tensor([100,0.1], dtype=torch.float)
y.backward(gradients)
print(x.grad) # tensor([300.0000, 0.3000])



gradients = torch.tensor([100,0.1], dtype=torch.float)
y.backward(gradinets, retain_graph = True) # retain_graph => 원래 grad 계산값을 저장을 안하기 때문에 따로 저장을 원하면 해줘야함!
print(x.grad)
y.backward(gradinets)
print(x.grad)

# tensor([300.0000, 0.3000])
# tensor([600.0000, 0.6000]) # gradients are accumlated
```

![image-20221017145137247](6_%EC%8B%A4%EC%8A%B5_AutoGrad.assets/image-20221017145137247.png)





### Class activation mapping (CAM) 구현

hooking: forward_hook 

: function call을 했을 때, 중간에 있는 정보를 낚아채는것 -> 부덕이 과제와 유사



hook_grad -> gradient 변경은 이루어져서는 안됨 -> return에서 하기!

`handle.remove`를 활용하여 hook 지우기!



