## 7. Instance/panoptic segmentation and landmark localization



semantic segmentation: 이미지에서 사람과 차만 추출하지만 각각의 instance 구별은 불가

instance segmetation: 이미지에서 사람과 차만 추출하는 것(각각의 사람과 차를 별개의 instance로 구별하는 것이 특징)

panoptic segmentation: 



### instance segmenters

Mask R-CNN

: RoIAlign



YOLACT (You Only Look At CoefficienTs)

: mask를 생성하는 다른 모델!

: video도 가능!



YolactEdge



### Panoptic segmentation

: 배경까지도 신경쓰면서 인스턴스 구분도 가능!



**UPSNet**

: semantic Head, Instance Head를 구별해서 layer 쌓음

-> 그 후 Panoptic Head로 합침



**VPSNet**

: for video! 



### 3. Landmark localization

: 얼굴, 포즈를 추정하는 기술, 키 포인트를 정하고 그것을 추정하는 것



Coordinate regression: 정확하지 않고 편차가 존재함

Heatmap classification: 좋은 성능을 보이지만 비용이 더 많이 듬



