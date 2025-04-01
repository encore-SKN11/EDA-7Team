**📅개발 기간: 2025.03.31 ~ 2025.04.01**
# 🎓 대학교 수강 이탈 예측 모델링

## 🏃‍♂️ 팀원 소개
- **SK 네트웍스 Family AI 캠프 11기**

- **팀명:** **6조**
---

|[@백미송](https://github.com/misong-hub)|[@김성지](https://github.com/kimseoungji0801)|[@이채은](https://github.com/chaeeunlee05)|[@이혜성](https://github.com/comet39)|[@홍성욱](https://github.com/Sung-WookHong)|
|------|------|------|------|------|
| <img src="https://github.com/user-attachments/assets/108ea96c-cb56-42fc-90cb-0d2c833c0fd2" width="200"/> | <img src="https://github.com/user-attachments/assets/108ea96c-cb56-42fc-90cb-0d2c833c0fd2" width="200"/> | <img src="https://github.com/user-attachments/assets/2dc83746-b3a4-45a8-96d3-36a458222cc1" width="200"/> | <img src="https://github.com/user-attachments/assets/14e4c4f8-80b6-41d9-befb-9e0c59b96443" width="200"/> | <img src="https://github.com/user-attachments/assets/da607129-b42f-4275-84cc-5e1379a6f749" width="200"/> |

<br>

## 목차   
1. 프로젝트 개요   
    1) 프로젝트 목표   
    2) 데이터셋 
2. 탐색적 데이터 분석 (EDA)   
    1)    
3. 학생 이탈 예측 모델 학습   
    1)   
4. 학생 정보 기반 맞춤형 교육과정 설계
5. Appendix
   
<br>

---

## 1. 🔍 프로젝트 개요
### 1) 📌 프로젝트 목표
 * Open University의 실제 데이터셋을 활용하여 수강 철회 결정에 영향을 미치는 주요 요인 분석
 * 수업 난이도, 학생의 기본 정보, 과제 제출 패턴 등을 종합적으로 분석해 수강 철회 확률 예측
 * 신규 수강생의 데이터를 기반으로 수강 철회 가능성을 조기에 예측하고, 맞춤형 교육과정 설계방안 제시

### 2) 📂 데이터셋    
 * 데이터 개요   
   영국 Open University에서 공개한 대표적인 공개 데이터: [Open University Learning Analytics Dataset (OULAD)](https://analyse.kmi.open.ac.uk/#open-dataset)
 * 데이터 구성
    1. `assessments.csv` : 각 강의에서 제공되는 과제 및 평가 관련 세부 정보 <br/>
    2. `courses.csv`: 개설된 각 강의의 식별자, 강의명 등 강의 기본 정보 <br/>
    3. `studentAssessment.csv`: 학생들의 과제 제출 이력과 성적 데이터를 포함한 학습 성과 정보 <br/>
    4. `studentInfo.csv` : 각 학생의 인구통계학적 특성(성별, 연령, 최종 학력 등) <br/>
    5. `studentRegistration.csv`: 학생들의 수강 신청 내역과 각 강의에 대한 철회 여부 <br/>
 * 5개의 csv 파일을 `학생 ID(id_student)`, `과목 코드(code_module)`, `학기(code_presentation)`를 기준으로 병합
 * 최종 병합된 데이터에 포함된 컬럼  cf.) [제거된 컬럼 명 확인](#불필요한-컬럼-제거)    
표 1.1 원본 데이터에 포함된 주요 컬럼 항목

| 컬럼명                     | 설명                                                               |
|----------------------------|--------------------------------------------------------------------|
| gender                     | 학생의 성별 (남성, 여성)                                          |
| highest_education          | 학생의 최고 학력 수준 (고등학교, 학사, 석사)                       |
| imd_band                   | 학생이 속한 지역의 사회경제적 지위                                 |
| age_band                   | 학생의 연령대                                                     |
| disability                 | 학생의 장애 여부                                                  |
| studied_credits            | 학생이 현재까지 이수한 학점 수                                    |
| num_of_prev_attempts       | 해당 과목의 과거 수강 이력 횟수                                   |
| final_result               | 최종 결과 (Pass, Fail, Withdrawn)                                |
| date_registration          | 학생이 등록한 날짜                                               |
| module_presentation_length | 강의의 전체 길이                                                 |
| assessment_weight          | 각 평가 항목이 성적에 미치는 비중                                 |

<br>
<br>

표 1.2 초기 데이터 컬럼을 기반으로 계산된 신규 컬럼 항목    
| 컬럼명                     | 설명                                                                 |
|----------------------------|----------------------------------------------------------------------|
| my_average_score           | 특정 학생의 평균 점수                                               |
| my_score_std               | 특정 학생의 점수 표준편차                                           |
| my_score_trend             | 특정 학생 점수의 변화 추이 (상승, 하락)                             |
| weighted_score             | 평가 가중치를 반영한 환산 점수                                      |
| course_avg_score           | 특정 과목 수강생들의 평균 점수                                      |
| course_max_score           | 특정 과목 수강생 중 최고 점수                                       |
| course_std_score           | 특정 과목 수강생들의 점수 표준편차                                  |
| course_late_rate           | 해당 과목에서 전체 학생의 지각 제출 비율                            |
| days_early_submission      | 마감일 기준으로 과제를 조기 제출한 일 수                            |
| my_late_rate               | 해당 학생의 전체 과제 중 지각 제출한 과제 비율                       |


## 2. 📊 탐색적 데이터 분석 (EDA)


## 5. Appendix

#### 불필요한 컬럼 제거   
   - 분석에 불필요하거나 중복되는 정보를 가진 열 제거   
![image](https://github.com/user-attachments/assets/6bfea0d2-d3ab-43d1-ae69-88ef89b54229)







<p align="center">
  <img src="./readme_image/언어의 연관성.jpg" height="450" width="450">
</p>

<div align="center">
  그림 1.1 언어 데이터가 가지는 단어간 상호관계 예시
</div>
<br>
  
* 단어 빈도 속성: K-means 클러스터링<sup>*</sup>을 활용하여 48개의 속성을 5개의 그룹으로 구분
* 군집화된 단어들을 시각화하기 위해 주성분 분석 (PCA)<sup>**</sup>으로 데이터 속성을 2개로 축소 후 산점도(scatter) 그래프 작성
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>*</sup>K-means 클러스터링: 데이터를 K개의 군집으로 나누어 중심점을 기준으로 반복적으로 최적화  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>**</sup>주성분 분석 (PCA): 고차원 데이터를 저차원으로 변환하여 주요 정보만 보존
