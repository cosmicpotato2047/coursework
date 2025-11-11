# AI Coursework Repository

이 저장소는 인공지능 관련 교과목에서 수행한 과제들을 정리한 공간입니다.  
각 과제는 독립적인 폴더로 구성되어 있으며, 코드와 결과, 분석 과정을 함께 포함합니다.

---

## 📂 과제 목록

### 🔹 [AI Assignment 1: Cars93 데이터 분석](./AI_Assignment1_Cars93)
- **내용**: Cars93 데이터셋을 활용하여 기술통계, 왜도 분석, 상관관계, 가설 검정, 전처리 과정을 수행.
- **핵심 포인트**:
  - 왜도(skewness) 계산 및 해석
  - Type별 평균 비교를 통한 t-test 수행
  - 이상치 제거 및 정규화, 결측치 보정
- **결과 요약**: 주요 속성 간 상관관계 파악, 데이터 전처리의 중요성 확인

---

### 🔹 [AI Assignment 2: Wine Classification](./AI_Assignment2_WineClassification)
- **내용**: sklearn의 Wine 데이터셋을 활용한 분류(Classification) 모델 실습
- **핵심 포인트**:
  - Logistic Regression을 활용해 와인 종류 분류
  - StandardScaler로 정규화 후 학습
  - 정확도(Accuracy) 평가 및 모델 비교
- **결과 요약**: Logistic Regression 기반 모델 정확도 약 98%, 데이터 스케일링의 효과 확인

---

###🔹 [AI Assignment 3: Mall Customer Clustering](./AI_Assignment3_MallCustomerClustering)
- **내용**: 쇼핑몰 고객 데이터를 이용해 K-Means 및 계층적 군집화를 수행하고, 고객의 소비 성향을 분석.
- **핵심 포인트**:
  - Annual Income(연간 소득)과 Spending Score(소비 점수) 변수 선택
  - StandardScaler를 이용한 Z-score 정규화
  - Elbow Method로 최적의 클러스터 수 탐색
  - K-Means 학습 및 Silhouette Score로 군집 품질 평가
- **결과 요약**: 3개의 주요 고객 그룹(고소득·고소비 / 중간소득·중간소비 / 저소득·저소비) 도출, 시각화를 통해 소비 패턴과 고객 세분화 가능성 확인

---

## ⚙️ 환경 정보
- Python 3.12  
- Jupyter Notebook  
- 주요 라이브러리: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`

---

## 🧠 학습 목표
- 데이터 분석 및 시각화 능력 향상  
- 전처리(결측치, 이상치, 스케일링)의 중요성 이해  
- 머신러닝 모델 학습 및 평가 경험 축적
