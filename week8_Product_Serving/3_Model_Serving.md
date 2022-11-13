## 3. Model Serving

: 요리를 만들면 손님에게 서빙해야죠!

: Production(Real World) 환경에 모델을 사용할 수 있도록 배포

: 머신러닝 모델을 개발하고 현실 세계 (앱, 웹)에서 사용할 수 있게 만드는 행위



#### 방식

크게 2가지 방식

- Online Serving
- Batch Serving



#### 용어  정리

Serving: 모델을 웹/앱 서비스에 배포하는 과정, 모델을 활용하는 방식, 모델을 서비스화하는 관점

Inference: 모델에 데이터가 제공되어 예측하는 경우, 사용하는 관점

-> Serving - Inference 용어가 혼재되어 사용되는 경우도 존재



#### Web Server Basic

웹 서버: 요청한 내용을 반환하는 것

machine learnig server는 client의 다양한 역할을 처리해주는 역할

만들 마스크 예측 모델 프로토 타입: 임의의 이미지를 넣었을 때 판단하는 웹 서버



#### API

: 운영체제나 프로그래밍 언어가 제공하는 기능을 제어할 수 있게 만든 인터페이스

: pandas, tensorflow 등도 다 API라고 볼 수 있음



#### Online Serving을 구현하는 방식

1. 직접 API 웹 서버 개발: Flask, FastAPI 등을 사용해 서버 구축
2. 클라우드 서비스 활용: AWS의 SageMaker, GCP의 Vertex AI 등 -> 소수의 인원이 많은 업무를 해야하는 경우, 그러나 숙련도가 필요하다. 
3. Serving 라이브러리 활용: Tensorflow Serving, Torch Serve, MLFlow, BentoML 등 -> 완전 간단함



#### 다양한 Serving 방법을 선택하는 가이드

추천 방식

(만약 회사에서 클라우드 비용에 대해 괜찮을 경우)

1. 프로토타입 모델을 클라우드 서비스를 활용해 배포
2. 직접 FastAPI 등을 활용해 서버 개발
3. Serving 라이브러리를 활용해 개발



강의에선 다음과 같은 방식으로 진행

1. 프로토타입 개발
2. FastAPI로 서버 개발
3. Serving 라이브러리로 개발



#### Online Serving에서 고려할 부분

지연 시간을 최소화해야함 -> 추천 배달을 1분만에 받으면 서비스 쓸거니??

그래서 간단한 모델을 사용하는 경우도 존재



결과값에 보정이 필요한 경우

ex) 집 값을 예측하는데 집 값이 0보다 작을 경우 -> 이떄 0 이하의 모든 집 값은 0으로 후처리



#### Batch Serving

: 주기적으로 학습을 하거나 예측을 하는 경우

ex) 30분에 1번씩 최근 데이터를 가지고 예측, Batch 묶음(30분의 데이터)를 한번에 예측

: Batch Serving 관련한 라이브러리는 따로 존재하지 않음

-> 함수 단위를 "주기적"으로 실행함



#### Online Serving vs Batch Serving

기준은 Input을 기준으로!

하나씩 들어오면 Online, 한꺼번에 들어오면 Batch

즉각 결과를 반환해야하면 Online, 1시간에 한번만 해도 괜찮으면 Batch









 