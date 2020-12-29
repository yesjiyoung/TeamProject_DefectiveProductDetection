# Project 
### 반도체 제조공정 데이터 분석  : 반도체 제조 데이터를 기반으로 불량품 분류예측하기 


# Intro 
### 🗓️ Date 
Project term : 2020.10.28 ~ 2020.12.16 </br>
Presentation Date : 2020.12.16 </br>
### :man: Professor 
  한양대학교 ERICA 로봇공학과 윤종완 교수님 
### 👥 Team member 
  한양대학교 ERICA 산업경영공학과 2018042660 노지영  <br/>
  한양대학교 ERICA 로봇공학과 2015041730 여태수 
  
  
# Data Set 
### ✅ Source 
https://www.kaggle.com/paresh2047/uci-semcom <br/>
csv file : uci-secom.csv

### ✅ Characteristics of the dataset 
- Data Set Characteristics: Multivariate
- Number of Instances: 1567
- Area: Computer
- Attribute Characteristics: Real
- Number of Attributes: 591
- 타겟 변수의 클래스 불균형 : 양품 데이터와 불량 데이터의 비율 -> 97:3
- 레코드 수의 부족 : (행)1567 * (열)592 = 2.6 : 1 비율 : 열대비 레코드의 개수가 매우 부족
- 도메인 지식의 반영 불가 : 개방된 제조 데이터 특성 상, 피쳐이름이 모두 닫혀있음. 도메인 지식을 반영할 수 없는 구조이므로 데이터를 전처리시, 유의해야할 필요가 있음. 
  
# Contents 
- **1. 데이터 탐색**
  - &nbsp; 1.1 데이터 읽어오기
  - &nbsp; 1.2 기술통계량 확인
  
- **2. 데이터 전처리**
  - &nbsp; 2.1 피쳐 name 변경하기
  - &nbsp; 2.2 0에 가까운 분산을 가진 피쳐 제거
    - &nbsp;&nbsp; 2.2.1 std==0인 변수 제거
    - &nbsp;&nbsp; 2.2.2 std~0에 근사한 변수 제거
  - &nbsp; 2.3 다중공선성 문제 확인 및 상관성 분석을 통해 피쳐를 선별적으로 제거
  - &nbsp; 2.4 Null값 처리하기
    - &nbsp;&nbsp; 2.4.1 50% 이상 Null값을 가진 열 제거
    - &nbsp;&nbsp; 2.4.2나머지 null값을 다중대치법을 사용하여 예측값으로 채움
  - &nbsp; 2.5 Oultlier 확인
    - &nbsp;&nbsp; 2.5.1이상치 보정
  - &nbsp; 2.6스케일링
  - &nbsp; 2.7Recursive Feature Elimination(RFE)의 피쳐 Rank를 통해 피쳐중요도 확인
  - &nbsp; 2.8 oversampling + train_test 분리
  
- **3. 모델링**
  - &nbsp; 3.1 하이퍼파라미터튜닝+검증 -gridSerachCV()
  - &nbsp; 3.2 random_state from 1 to 100

# Result
### ✅ Source Code 
Colab -> https://colab.research.google.com/drive/1ibSSZ5al6CTNbzPseiDajEsx9ebIu8GI?usp=sharing
### ✅ AUC Score 
0.860809
### ✅ Final Evaluation
- Team Acitivity Score : 9팀 중 1등 
- Data Processing Creativity :  9팀 중 1등
- AUC Score Ranking : 9팀 중 3등 
