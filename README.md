# SKN011-EDA-7Team
- 이현민
- 정현욱
- 홍성욱

  <br>
  
📅미니프로젝트 기간: 2025.03.11 ~ 2025.03.14
---
# 📧스팸메일 구별을 위한 탐색적 데이터 분석 (EDA)
<br>

## 목차
1. 주제선정 이유 및 프로젝트 목표
2. 데이터 확인
    1) 데이터 도큐맨테이션
    2) 데이터 기본 구조
3. 데이터 분석
    1) 결측치 탐색
    2) 데이터 차원 축소를 위한 그룹핑
    3) 데이터 변환 및 피처 엔지니어링
    4) 데이터 스케일링
4. 결론
   
<br>

---
## 1. 🎯 주제선정 이유 및 프로젝트 목표
 * 일반적으로 경험하는 스팸메일의 데이터 전처리를 통해 청중의 관심도 증대.
 * 상호 관계가 깊은 언어 데이터의 전처리를 통해 데이터간 상관관계 처리에 대한 이해력 상승.
 * 본 부트캠프의 최종 목표인 대규모 언어모델 (LLM) 학습 전, 언어 데이터에 대한 이해력 향상.

<p align="center">
  <img src="./readme_image/언어의 연관성.jpg" height="500" width="500">
</p>

<div align="center">
  그림 1.1 언어 데이터가 가지는 단어간 상호관계 예시
</div>


## 2. 📜 데이터 확인
* 데이터 출처: https://archive.ics.uci.edu/dataset/94/spambase
  
### 1) 💡 데이터 도큐맨테이션

<p align="center">
  <img src="./readme_image/초기 데이터 프레임.png" height="120" width="1000">
</p>

<div align="center">
  그림 2.1 스팸메일 구별 데이터프레임 개요
</div>
<br>


 * 전기차는 에너지 효율이 높아 친환경 자동차 중 가장 보급 가능성이 높은 자동차로 평가되어, 정부는 전기차 구매 시 보조금을 적극적으로 지원하고 있음. 하지만, 소비자들은 전기차의 성능, 보조금 정책, 충전 인프라 등 핵심 정보에 대한 접근성이 부족하여 구매 결정에 어려움을 겪고 있는 실정임.
 * 소비자 설문조사 결과 전기차 구입을 망설이는 가장 큰 이유로 충전인프라, 가격, 주행거리 등 이 선정됨.
<p align="center">
  <img src="./readme_img/전기차구매이유.png" height="300" width="450">
</p>

<div align="center">
  그림 2. 전기차관련 설문조사 결과
</div>

<br>

 * 이에따라, 소비자들이 전기차 구매 시 가장 궁금해하는 정보를 직접적으로 비교할 수 있도록 대표적인 국내 전기차 모델들의 성능, 정부 보조금, 그리고 국내 충전 인프라 현황에 대한 종합적인 정보를 제공하고자 함.

### 2) 🎯 프로젝트 목표

 💿 국내 전기차 모델 성능, 국내 충전 인프라 현황 데이터베이스 구축
   - 국내 전기차 모델의 성능 정보 및 국내 충전 인프라 현황을 웹 크롤링하여 데이터를 수집하고, 이를 바탕으로 통합 데이터베이스를 구축함.

 📊 국내 전기차 모델 성능 비교 제시
   - 소비자가 관심있는 두 가지 전기차 모델을 선택하여 성능(배터리 용량, 연비 등)과 정부 보조금 정보를 직관적으로 비교할 수 있도록 데이터 시각화 플랫폼을 구축함.

 🗺️ 국내 충전 인프라 현황
   - 국내 전기차 충전 인프라 현황을 직관적으로 확인할 수 있도록 지도 기반 그래프 형태로 정보를 제시함.

 ❓ 전기차 구매 보조를 위한 통합 정보 FAQ
   - 전기차 구매 시 소비자들이 주로 궁금해하는 다양한 정보를 종합하여 FAQ 형태로 정리함.

<br>

---

## 2. 💻 프로젝트 내용

### 1) 🛠️ 사용 기술
 |<img src="https://img.shields.io/badge/streamlit-E31337?style=for-the-badge&logo=streamlit&logoColor=red"> |<img src="https://img.shields.io/badge/mysql-003791?style=for-the-badge&logo=mysql&logoColor=blue"> |<img src="https://img.shields.io/badge/python-49CC68?style=for-the-badge&logo=notion&logoColor=green"> |<img src="https://img.shields.io/badge/fast api-FF7900?style=for-the-badge&logo=fast api&logoColor=orange"> |<img src="https://img.shields.io/badge/selenium-7A1FA2?style=for-the-badge&logo=notion&logoColor=purple">|<img src="https://img.shields.io/badge/데이터 정제-000000?style=for-the-badge&logo=데이터 정제&logoColor=white">|

<br>

### 2) 🕸️ ERD
  <p align="center">
  <img src="./readme_img/ERD.png" height="600" width="800">
  </p>

### 3) 🎫 WBS

<center>

| 작업명              | 시작일 | 종료일 | 담당자   | 산출물               |
|:-------------------:|:------:|:------:|:--------:|:--------------------:|
| 프로젝트 주제선정   | 02-25  | 02-25  | ALL      | 없음                 |
| ERD작성            | 02-25  | 02-26  | ALL      | ERD모델              |
| DB연동             | 02-25  | 02-06  | 이현대   | 웹 크롤링, 데이터수집 |
| web crawling       | 02-25  | 02-26  | ALL      | 데이터수집           |
| Streamlit UI 구현   | 02-25  | 02-26  | ALL      | Streamlit            |
| 디버깅             | 02-26  | 02-26  | ALL      | 결과                 |

</center>

<br>

### 4) 🖼️ 데이터 시각화 플랫폼

 * 메인화면

  <p align="center">
  <img src="./readme_img/front_1.png" height="400" width="800">
  </p>

 * 전기차 모델 성능 비교

  <p align="center">
  <img src="./readme_img/front_2-1.png" height="435" width="800">
  </p>

<br>

  <p align="center">
  <img src="./readme_img/front_2-2.png" height="430" width="800">
  </p>

 * 국내 충전인프라 현황

  <p align="center">
  <img src="./readme_img/front_3-1.png" height="430" width="800">
  </p>

<br>

  <p align="center">
  <img src="./readme_img/front_3-2.png" height="320" width="800">
  </p>

<br>

  <p align="center">
  <img src="./readme_img/front_3-3.png" height="420" width="800">
  </p>

 * 통합 정보 FAQ

  <p align="center">
  <img src="./readme_img/front_4.png" height="440" width="800">
  </p>


<br>

---

## 3. 📜 한 줄 회고
