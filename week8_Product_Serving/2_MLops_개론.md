## 2. MLops 개론

문제정의 - EDA - Feature Engineering - Train - Predict



모델의 결과값이 이상한 경우가 존재

- 원인 파악 필요
- Input 데이터가 이상한 경우가 존재
- Research 할 때, Outlier를 제외할 수 있지만, 실제 서비스에선 제외가 힘든 상황 



모델의 성능이 계속 변경

- 모델의 성능을 어떻게 확인할지
- 예측값과 실제 레이블을 알아야 함
- 정형(Tabular) 데이터에서는 정확히 알  수 있지만, 비정형 데이터(이미지 등)은 잘 모를 수 있음



새로운 모델이 더 안좋다면

- 이전 모델을 다시 사용하기 위한 작업이 필요 -> 이런 것들을 쉽게 할 수 있는 준비를 해둬야함



-> 머신러닝 모델링 코드는 머신러닝 시스템 중 일부에 불과함



MLOps = ML + Ops

: 머신러닝 모델을 운영하면서 반복적으로 필요한 업무를 자동화하는 과정



MLops 베스트 라이브러리는 아직 확립이 되지 않은 상태

-> 클라우드에서도 MLOps 시장 점유를 목표로 함



-> 그래서 MLOps의 각 Component에서 해결하고 싶은 문제는 무엇이고 그 문제를 해결하기 위한 방법으로 어떤 방식을 활용할 수 있는지를 학습하는 방식으로 학습하는 것을 추천!



### MLOps Component

: 처음엔 집에서 사용하던 재료, 소스를 활용할 수 있음

음식 = 모델

식재료, 소스, 밀가루 빵 = Data / Feature

요리하는 행위 = 모델 Train



#### Infra

클라우드: AWS, GCP, Azure, NCP 등

온 프레미스: 회사나 대학원의 전산실에 서버를 직접 설치



#### Serving



#### Experiment, Model Management

: 부산물 저장!

model artifact = pickle과 같이 모델을 저장하는 것

각 모델별 파라미터와 결과 저장 

대표적으로  MLFlow



#### Feature Store

: 중복되는 feature들을 저장하는 기능(우리 프젝에 augmentation 부분 같은거)

feature_store lib => FEAST

그러나 library보다는 직접 만들어서 많이 사용함



#### Data Validation

: 아직 명확한 library는 없다..



#### Continuous Training

: 신선한 재료로 다시 요리!

- 새로운 데이터가 도착한 경우
- Metric 기반으로 너무 줄어들면 다시 학습하는 방법

library가 특별히 존재하는 건 아니고 이런 개념을 구현한다고 생각하기 



#### AutoML

: 자동으로 음식을 만들수도 있음!

