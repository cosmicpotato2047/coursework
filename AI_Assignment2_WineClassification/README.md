# AI Assignment 2: Wine Classification

이 프로젝트는 sklearn의 `load_wine` 데이터셋을 사용하여 와인의 화학 성분을 기반으로 종류를 분류하는 과제입니다.  
Logistic Regression, Decision Tree 등 여러 분류 알고리즘 중 하나를 자유롭게 선택하여 모델을 학습했습니다.

---

## 📌 과제 목표
- `load_wine()` 데이터셋을 이해하고 데이터프레임으로 변환
- Train/Test 데이터 분리 (`test_size=0.3`)
- 데이터 스케일링 (`StandardScaler`)
- 분류 모델(Logistic Regression) 학습 및 예측
- 모델 정확도 및 분류 성능 평가

---

## 🧠 핵심 코드 구성
```python
from sklearn.datasets import load_wine
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import classification_report
```

📈 결과 요약

모델 정확도: 약 0.98

Classification Report: 모든 클래스에서 Precision, Recall, F1-score > 0.9

결론: Logistic Regression은 스케일링 후 빠르고 안정적으로 수렴하며, Wine 데이터셋 분류에 효과적임

🚀 확장 아이디어

Decision Tree, Random Forest, SVM 등 다른 모델과 성능 비교

PCA를 이용한 차원 축소 후 정확도 변화 분석

Confusion Matrix 시각화

📂 파일 구성
AI_Assignment2_WineClassification/
├── AI-Assignment2-Classification.ipynb   # 전체 코드 및 결과
└── README.md                             # 과제 요약 문서
