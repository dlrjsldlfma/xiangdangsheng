---
layout: post
title: Tableau_Study_1
date : 06 Dec 2021
category : Tableau
comments : true
---

# Tableau
## 주요 전처리 기능 정리


#### 1) 데이터 전처리
##### (1) 피벗 (long-form)
 : wide-form -> long-form데이터 형태여야 시각화 가능
```
Step_1) 전환해야하는 축 범위 선택
Step_2) 전환해야하는 축 마지막 컬럼에서 화살표 클릭
Step_3) 피벗 클릭
```


##### (2) 데이터 원본 필터링
```
Step_1) 데이터 원본 시트 우측 상단 '필터' '추가' 클릭
Step_2) 기준이 될 필드 선택
Step_3) 필터 기준 선택
```
<center>
<img src = '/assets/tableau/tableau_study_preprocess_2-1.png' width = '80%'>

<img src = '/assets/tableau/tableau_study_preprocess_2-2.png' width = '80%'>

<img src = '/assets/tableau/tableau_study_preprocess_2-3.png' width = '80%'>
</center>


##### (3) 새로운 필드 생성하기 (계산된 필드 생성하기)
```
Step_1) 계산 대상 필드 마우스 우측 클릭
Step_2) 계산된 필드 생성
Step_3) 계산식 입력
```
<center>
<img src = '/assets/tableau/tableau_study_preprocess_3.png' width = '80%'>
</center>


##### (+) 사용자그룹별 분석시 데이터의 형태
 : 다수 사용자그룹을 생성하여, 특정항목에 대한 분석을 진행해야 하는 경우, 아래 두가지 테이블을 생성한 후 분석하는 방향으로 진행.
 이후 두 테이블을 서로 merge할시, Tabeau에서 쉽게 filter를 줄 수 있음.
  - 분석 테이블
  - 유저별 사용자 그룹 테이블
|||  <---- 예시 테이블 만들 차례! 
