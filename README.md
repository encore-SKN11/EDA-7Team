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
2. 데이터 기본 구조 확인
    1) 데이터 도큐맨테이션
    2) 스팸 데이터 특성 파악
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
  <img src="./readme_image/언어의 연관성.jpg" height="450" width="450">
</p>

<div align="center">
  그림 1.1 언어 데이터가 가지는 단어간 상호관계 예시
</div>


## 2. 📜 데이터 확인
* 데이터 출처: https://archive.ics.uci.edu/dataset/94/spambase
  
### 1) 💡 데이터 도큐맨테이션

**① 단어 빈도 (word frequency) 속성 (48개)**
   * 특정 단어가 이메일에서 차지하는 비율 (0~1 사이의 float 타입)

**② 문자 빈도 (character frequency) 속성 (6개)**
   * 특정 특수문자가 이메일에서 차지하는 비율 (0~1 사이의 float 타입)

**③ 대문자 연속 속성 (3개)**
   * 연속된 대문자 시퀀스의 평균 길이 (1 이상의 float 타입)
   * 가장 긴 연속된 대문자 시퀀스 길이 (1 이상의 int 타입)
   * 이메일 내 대문자 개수의 총합 (1 이상의 int 타입)

**④ 클래스 속성 (1개)**
   * 이메일의 스팸 여부를 나타내는 속성 (0, 1)
   * 0: 일반 이메일
   * 1: 스팸 이메일

<p align="center">
  <img src="./readme_image/초기 데이터 프레임.png" height="120" width="1000">
</p>

<div align="center">
  그림 2.1 스팸메일 구별 데이터프레임 개요
</div>
<br>

### 2) 🚫 스팸 데이터 특성 파악
 
<p align="center">
  <img src="./readme_image/스팸타입1.jpg" height="300" width="320">
</p>

<div align="center">
  그림 2.2 초기 스팸 데이터 형식
</div>
<br>

<p align="center">
  <img src="./readme_image/스팸타입2.jpg" height="280" width="1000">
</p>

<div align="center">
  그림 2.2 광고 유형별 변칙 표기 사례
</div>
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
