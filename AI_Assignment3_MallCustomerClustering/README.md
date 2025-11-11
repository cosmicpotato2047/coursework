# AI Assignment 3: Mall Customer Clustering

이 프로젝트는 쇼핑몰 고객 데이터를 기반으로 K-Means 및 계층적 군집화를 수행하여 고객 그룹을 식별하는 과제입니다.
연간 소득(`Annual Income`)과 소비 점수(`Spending Score`)를 기준으로 고객의 소비 패턴을 분석했습니다.

---

## 📌 과제 목표

* `Mall_Customers.csv` 데이터셋을 불러와 전처리
* 상관관계 분석 (`sns.heatmap`)
* 연간 소득과 소비 점수만 선택 후 표준화 (`StandardScaler`)
* Elbow Method를 활용하여 적절한 K값 탐색
* K-Means 모델 학습 및 클러스터 시각화
* Dendrogram을 통한 계층적 군집 분석
* Silhouette Score를 이용한 군집 품질 평가

---

## 🧠 핵심 코드 구성

```python
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
from sklearn.preprocessing import StandardScaler
from sklearn.cluster import KMeans
from sklearn.metrics import silhouette_score
from scipy.cluster.hierarchy import linkage, dendrogram
```

---

## 📈 결과 요약

* Elbow Method 결과: 최적의 클러스터 수(k) ≈ 3
* K-Means 클러스터링을 통해 3개 주요 고객 그룹 도출
  ① 고소득·고소비 그룹
  ② 중간소득·중간소비 그룹
  ③ 저소득·저소비 그룹
* Silhouette Coefficient: 약 0.55로, 비교적 명확한 군집 분리 확인
* 시각화를 통해 각 그룹의 소비 성향을 직관적으로 파악 가능

---

## 🚀 확장 아이디어

* 연령, 성별 등 추가 변수를 포함한 다차원 클러스터링
* PCA를 활용한 2D 차원 축소 후 군집 시각화
* DBSCAN, Gaussian Mixture Model 등과의 비교
* 각 클러스터별 고객 타겟팅 전략 수립 (마케팅 활용)

---

## 📂 파일 구성

```
AI_Assignment3_MallCustomerClustering/
├── AI-Assignment3-Clustering.ipynb    # 전체 코드 및 시각화
└── README.md                          # 과제 요약 문서
```
