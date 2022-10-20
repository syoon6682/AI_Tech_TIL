## 8. Transformer

: 문장은 밀리거나, 비거나 하는 문제로 정보가 누락될 가능성이 크다.



tranformer 구조

: 재귀적인 구조가 아닌 attetion이라는 구조를 활용했다. -> attention 구조가 중요!!, NMT가 시초

: sequential한 데이터를 처리하고 그 데이터를 인코딩하는 방법

: 번역 ai와 가장 가깝다고 생각하면 됨



그러나 실습에서 다루는 attention 구조는 Jay Alammar가 제시한 구조와는 살짝 다르다..이건 추후 알랴줌



특징:

- 입력 시퀀스와 출력시퀀스는 다를 수 있음 (ex. 사랑해 -> I love you (1, 3))
- 입력시퀀스가 100개면 100번의 재귀가 아닌 한번에 encoder에 들어가서 decoder로 보내는 방식





Self-attention

1. 단어 하나하나를 벡터로 봄
2. self-attention을 활용하여 새로운 벡터로 만드는데 이때 다른 벡터도 같이 관여하여 생성



과정

1. embedding 벡터로부터 3개의 벡터, query, key, value
2. key, value벡터들을 기반으로 score 벡터를 생성, 그 후 인접한 단어 벡터와 내적을 하여 유사성? 판단



단점

1. length가 길어지면서 처리할 수 있는 한계가 있음



positional encoding 하는 이유

: ..?



교재 첨부되어 있는 블로그 참고하기!



요즘에는 self-attention이라는 구조를 이미지에서도 많이 활용한다. 