---
layout: post
title: 데이터 분석 리포트 작성 프레임워크(Data Analysis Reporting Framework)
date : 03 Feb 2022
category : DataAnalysis_Marketing
comments : true
---
: 데이터 분석을 하다보면, 연간/분기/특정기간내 서비스 전체 또는 주요 지표들에 대해서 리포팅을 해야하는 상황이 생겨난다. 이에 데이터 분석 리포팅 작성시, 절차 및 이슈들을 정리해보자.
 이때 각자의 문제 상황에 따라서 리포팅 작성 방식은 다를 수 밖에 없기에, 특정 문제를 해결하기 위한 FrameWork라고 보면 좋을 것 같다. 또한 본글은 개인적 경험과 일부 리서치에 기반하였기에, 지속적인 수정 & 보완이 필요하다.  


> 아래 작성한 개인 경헙에 기반한 분석 방법론 외, 체계화 되어있는 방법론들은 아래 링크를 참고하자

<center>

 <img src = '/assets/DataAnalysis_Marketing/data_analysis_process/data_analysis_process_1.png' width = '80%'>

 [데이터_분석계획_빅데이터_분석기획 by noti-note님 블로그](https://noti-note.tistory.com/12)

 </center>  


<br>
# 1. 문제정의 $\star\star\star$
## 1) Why : 리포팅을 왜 하는 것일까? $\star$
 : 리포트를 보는 대상에 따라서, 문제정의 작성 및 리포팅의 이유가 크게 달라진다.
  특정 문제에 국한된 리포트 또는 Daily리포트는 주로 실무자나 중간급에서 빠른 의사결정 및 진행상황을 체크하기 위함이기에 문제정의가 명확하다. <br>

  반면, 리포트 작성의 이유가, 전반적인 서비스 평가 및 서비스 지속 인사이트 추출이라는 모호한 경우가 있다. 주로 중장기간의 서비스 전체 또는 KPI 2,3개 이상의 리포트를 작성하여 상급자에게 리포트를 하는 경우이거나, 아직 데이터로 구체적인 KPI를 잡지 못하여 모니터링 조차 하지 못하는 팀에서 "전체적인 탐색적 분석을 하며 인사이트를 찾고 싶어요"라는 막연한 요청을 하는 경우가 주로 이러하다. <br>

  이런 막연함 속에도 "우리의 서비스가 얼마나 효율적으로 또는 어떤 방향으로 운영되고 있으며", "어떤 문제가 있는지", "분기별로 얼만큼의 성과를 이루었는지" 등의 목표가 존재한다. 추상적인 목표를 아래 분석 항목별로 나눠, 구체화 시키는 작업이 필요하다.


<br>
## 2) What : 무엇을 분석할 것인가? $\star$
 : 커머스 서비스 가정하에 탐색적 분석을 진행하기 위하여, 고객 여정별 분석 항목을 정리해보자.

<center>
<img src = '/assets/DataAnalysis_Marketing/report_1.png' width = '100%'>
</center>  

    (1) 유입 (Acqusition)
      - 앱설치자수 (total / daily)

    (2) 유입 채널 (Attribution)
      - 채널별 앱설치자수(유입자수) (total / daily)
      - 채널별 유입자 *KPI 전환율 (KPI : 회원가입 / 구매 / ETC)
      - 채널별 Fraud / Bounce 유저수 (total / daily)

    (3) 활성화 (Activation)
      - 회원가입자수 (total / monthly / weekly / daily)
      - 회원가입 전환율 (total / monthly / weekly / daily)

    (4) 유지 (Retention)
      - 접속 빈도 : DAU / WAU / MAU
      - 접속 빈도 : 평균 접속주기  
      - 사용 시간 : 세션당 평균 사용 시간 (집단별 / daily)
      - 퍼널 분석 : 설치 > 가입 > 상품 조회 > 상품 구매 > 재구매
                  (기간별 / 집단별 비교)

    (5) 참여 & 커머스 (Engagement & Commerce)
      - 참여 : 특정 이벤트 유입자 및 회원가입 등 KPI 지표
      - 참여 : 공유 조회 활성 유저수 (total / monthly / weekly / daily)  
      - 커머스 : 상세페이지 조회 & 조회자수  
      - 커머스 : 구매 & 구매자수 (total / monthly / weekly / daily)
      - 커머스 : 재구매 & 재구매율
      - 커머스 : 조회 & 구매 상품 Top 10
      - 커머스 : 구매 전환율 (사용자 그룹별 / 기간별 / 상품별)
      - 커머스 : 구매 금액 / 인당 평균 구매액
      - 커머스 : Pair 분석

    (6) 이탈 (Churn)
      - 최근 7/14/28일 이탈율 (동기간 대비 / 집단별 / 일별)
      - Bounce / Farud  유저수 / 비율

    (7) 도달 (Reachability)
      - 메시지 퍼널 : 발송자 > 오픈자수 > 오픈자 중 구매자
      - 메시지 성과 분석 : 시간대별 접속자수 / 구매자수 추이 + 메시지 발송 시간 표기

    + 인구통계 (Demographic)
      - 전체 유저 : 성별 / 연령 분포
      - 사용자 그룹별(일반 / VIP 등등) : 성별 & 연령 분포
      - 사용자 속성 정보(등급 / 설문 결과 등등)


 위 목록에서 필요한 항목을 골라, 1차 문제 정의를 작성하고 탐색적 리포팅을 작성한다. 이 과정에서 시간과 여유가 있다면, 탐색적 분석 과정에서 도출한 인사이트를 토대로 원인을 파악하기 위한 2차 문제 정의를 작성 할 수 있을 것이다.


<br>
## 3) How : 어떻게 분석할 것인가?
 : 위 에서 어떤 항목을 분석할지 선택하더라도, 단일 지표만을 가지고 해당 지표를 긍정적으로 해석해야할지 부정적으로 해석해야할지 판단하기 쉽지 않다. 때문에 타겟 지표를 비교 할 수 있는 비교 집단을 함께 설계하는 것이 중요하다.

    ex) 메시지 성과 분석
    - 분석 집단 : 메시지 발신 후 전환율
    - 비교 집단 : 메시지 발신 전 전환율

---
<br>  
# 2. 데이터 수집
 : 분석에 필요한 데이터를 수집하는 과정으로, 사전에 협의된 분석 기간의 데이터를 추출한다. 이 단계에서는 데이터의 수집 뿐아니라, 적합성, 커스텀 변수등을 확인한다.

    (1) 데이터 퀄리티
      - 데이터 누락 확인

    (2) 데이터 기간
      - 분석 데이터 기간 확인

    (3) 분석 기준
      - 사용자 기준 데이터
      - 기기 기준 데이터

    (4) Key, Value, Param 정의
      - 매출, 카테고리 KPI 변수명 등을 사전에 정의

---
<br>
# 3. 데이터 전처리
 : 수집된 데이터의 결측치, 중복값, 타입오류 등의 이슈를 사전에 체크해준다. 다만 로그데이터를 분석하는 경우, 이상치 제거는 평균의 왜곡 등을 방지하기 위해서 필요하지만, 경우에 따라서 DB값과 차이를 생성하므로, 제거 여부 논의 후 판단해야하는 상황이 생긴다. 주요 전처리 이슈들은 아래와 같다.

    (1) 데이터셋 확인 단일
      - 상품의 중복 카테고리 이슈 [ex. 상품 1개, 카테고리 2개]
      - 데이터 타입 이슈 [ex. 금액 Value : str type으로 수집됨]
    (2) 결측값 처리
      - 삭제
      - 대체 (평균, 최빈값, 중간값)
      - 예측값 대체 (Regression, Logistic)
    (3) 이상치 처리
      - 단순 삭제
        : 리포트 경우 삭제가 어렵기에, Scaling으로 편향된 이상치를 조정
      - 평균, 중위값 등으로
    (4) Feature Engineering
      - Scaling
        : 변수의 단위가 너무 크거나 편향 될 경우, 변수간 관계가 잘 드러나지 않기에, Log 또는 SqureRoot등을 취해 스케일 조정
      - Binning
        : 연령, 금액 등 연속형 변수를 범주형 변수로 변경
      - Transfrom
        : 자주 사용하는 예로, 단순 weekday를 주중과 주말로 변환하는 것 처럼, 분석 목표에 맞는 변수생성

  * [데이터 전처리에 대한 모든 것 - DODOMIRA](http://www.dodomira.com/2016/10/20/how_to_eda/)
  * [데이터 전처리 필요성 및 - 나는야 데이터사이언티스트](https://rk1993.tistory.com/entry/%EB%8D%B0%EC%9D%B4%ED%84%B0-%EC%A0%84%EC%B2%98%EB%A6%AC)


---
<br>
# 4. 데이터 분석 or 모델링
 : ML/DL 모델을 구축하는 과정은 이단계에서 정제된 데이터를 모델에 넣어 최적화 작업을 진행한다.
 반면 리포트를 위한 분석에서는 데이터를 토대로, 인사이틀 발굴하기 위한 차이점과 원인을 찾는 실험설계의 과정이 반복된다.

       1. 가설 설정
       2. 실험군 비교군 설정
       3. 분석 지표 생성
       4. 결과 해석
리포트를 쓰다보면, 수많은 가설들을 세우고, 이에 따른 실험군과 비교군의 사용자집단들이 무수히 많아지기도 한다. 때문에 아래 2가지 모듈을 사전에 생성하고 작업한다면 비교적 정리된 상태로 분석을 진행할 수 있다.

       1. Module_1 : 사용자 그룹 생성
       2. Module_2 : 지표 분석


---
<br>
# 5. 데이터 분석 시각화
 : 시각화는 앞선 분석항목들을 최종적인 형태로 만들어 분석 결과를 해석하거나, 또는 리포트를 받는 사람입장에서 직관적으로 결과를 인지하기 위해 필요하다.
 때로는 너무 많은 변수들을 하나의 차트에 담으려고 하다보면, 시각화된 자료를 보고 해석하는데 많은 시간이 소요될 수 있으니, 시각화도 결국 어떤 분석 결과를 보여주기 위함인지 목적에 맞추어 필요한 정보만을 비교하는 것이 좋을 것 같다.

 - 적절한 시각화 방법 활용
   - 항목간 비교시 파이 그래프(비율)는 지양하고 막대(양) 그래프 위주
   - 시계열은 라인으로(실선)
   - 분포는 히스토그램이나 박스플롯
   - 변수간 관계는 산점도


---
<br>
# 6. 리포팅 및 피드백 반영
: 열심히 '기획 정의'를 작성하고 코드를 짜며 '분석'을 완료하고, '시각화'까지 마쳤다면, 이제 자료를 리포팅 형식으로 정리고 결과를 해석하기 위한 글을 작성하는 마지막 단계가 남아있다. 여기까지 오느라 이미 많이 지쳤겠지만, 이단계가 잘 이뤄지지 않으면 그동안의 노력이 물거품이 되어버릴 수 있을 만큼 중요한 단계이다.

## 1) 리포팅 포맷
 : 최종 리포트 작성을 위해 먼저 고민하는 것은 리포트의 포맷이다. 가장 쉽게는 '엑셀' 또는 'PPT'가 있을 것이며, 'GA Data Studio', 'Tableau'와 같은 툴을 사용하고 있다면 해당 분석툴의 기능을 사용하는 것도 좋을 것 같다.
 'Excel'과 'PPT'도 물론 사용자의 능력에 따라 다르겠지만, 개인적인 경험에 따르면 아래와 같은 상황에서 각각의 툴을 선택하는 것이 좋은 것 같다.

    - Excel
      : 탐색적 데이터 분석 과정에서 획득한 데이터들을 보며 실무진에게 리포팅하는 경우
    - PPT
      : 탐색적 분석을 마치고, 인사이트를 정리하여, 최종 의사결정자에게 중요한 분석 결과만 전달하는 경우


## 2) 리포팅 정리시 주안점

### (1) 독자 중심 정리
  - 상대가 이해할 수 있는 언어 사용
  - <b>목적을 수시로 상기</b>하고 재확인
  - 분석 과정 보다는 <b>'결과'</b>중심 전달

### (2) 간결 & 명확
  - 짧은 문장
  - Bullet point 방식
  - 선 핵심내용, 후 근거

### (3) 피드백 & 수정
  - 피드백 후 수정 & 보완은 당연한 과정
  - 분석입장에서 공을 들인 결과물도, 고객사 입장에서 중요도가 낮을 수 있음을 명시.

---
여기까지 분석 리포트를 작성하기 위한 각 단계별 작업들을 정리해보았다. 개인적으로 리포트라는 업무가 주어지면, 가이드라인 없이 망망대해에서 작업하던 경험이 많았기에, 그동안 작업했던 경험과 자료들을 취합하여 내가 사용하기 위한 글을 정리해보았다.
더불어 개인적으로 향상된 리포트 작성을 위해선, 복잡하고 각기 다른 형태의 산출물 데이터를 시각화 시키는 능력이 더 필요할 것 같다.




#### Reference
[1] [데이터 분석 절차 - @osk3856](https://velog.io/@osk3856/data-analysis)  
[2] [데이터 분석을 위한 5단계 절차 - 마경근](https://brunch.co.kr/@data/10)   
[3] [분석 프로세스 - 위키독스](https://wikidocs.net/16561)  
[4] [데이터 분석 계획](https://noti-note.tistory.com/12)  