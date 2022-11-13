## 6. Streamlit

voila의 장점 -> 쉽게 프로토타입을 만들 수 있음

그러나 레이아웃을 잡기 어려움



### 웹 서비스를 만드는 과정

프론트 + 백



### Streamlit의 대안

1. R의 Shiny
2. Flask, Fast API: 백엔드 직접 구성 + 프론트엔드 작업도 진행
3. Dash: 제일 기능이 풍부한 Python 대시보드 라이브러리
4. Voila: Jupyter Notebook을 바로 시각화 가능



### Streamlit 소개

- python 베이스
- 백엔드 개발이나 HTTP 요청을 구현하지 않아도 됨
- 쉬운 배포 가능
- 화면 녹화기능



localhost 8085로 접속



### Streamlit 작성

Text는 교재 참고

button도 참고

pandas dataframe을 지원

활용은 그냥 전체적으로 교재를 참고하면서 진행해보기

sidebar에는 파라미터를 지정하거나 암호를 설정할 수 있음

form을 통해 input을 받음 -> html과 많이 유사

session state를 활용하여 counter 등을 구현