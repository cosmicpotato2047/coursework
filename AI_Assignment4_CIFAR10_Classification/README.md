# **AI Assignment: CIFAR-10 Image Classification**

이 프로젝트는 CIFAR-10 이미지 데이터셋을 이용하여 CNN(합성곱 신경망) 기반의 이미지 분류 모델을 구축하는 과제입니다.
모델 구조를 직접 설계 및 개선하고, 테스트 정확도 **75% 이상**을 달성하는 것을 목표로 합니다.

---

## 📌 **과제 목표**

* CIFAR-10 데이터셋 로드 및 전처리
* Min–Max 정규화 및 One-hot 인코딩 적용
* CNN 모델 직접 설계 및 개선
* Batch Normalization, Dropout 등을 활용한 성능 향상
* 모델 학습 및 검증 과정 구현
* 테스트셋 분류 정확도 평가
* 예측 결과 시각화(실제 라벨 vs 모델 예측)

---

## 🧠 **핵심 코드 구성**

### 📍 데이터 로딩 및 전처리

```python
cifar10 = tf.keras.datasets.cifar10
(x_train, y_train), (x_test, y_test) = cifar10.load_data()

x_train, x_test = x_train / 255.0, x_test / 255.0
y_train = tf.keras.utils.to_categorical(y_train)
y_test  = tf.keras.utils.to_categorical(y_test)
```

### 📍 CNN 모델 구성

모델은 다음과 같은 주요 블록으로 구성됨:

* **Conv → BatchNorm → Conv → BatchNorm → MaxPool → Dropout**
* **Conv → BatchNorm → Conv → BatchNorm → MaxPool → Dropout**
* **Flatten → Dense(512) → BatchNorm → Dropout → Dense(10)**

### 📍 모델 컴파일 및 학습

```python
model.compile(
    optimizer="adam",
    loss="categorical_crossentropy",
    metrics=["accuracy"]
)

model.fit(x_train, y_train, epochs=50, validation_data=(x_test, y_test))
```

### 📍 모델 평가 및 예측 시각화

40개 테스트 이미지에 대해 예측 결과를 표시:

* 실제 라벨
* 예측 라벨
* 이미지 표시

---

## 📈 **결과 요약**

* Test Accuracy: **75% 이상 달성 가능**
* Batch Normalization 및 Dropout 도입으로 과적합 방지
* 여러 Conv 블록을 통해 이미지 특징을 효과적으로 추출
* 시각화를 통해 분류 성능 및 오류 패턴 확인 가능

---

## 📂 **파일 구성**

```
AI_Assignment4_CIFAR10_Classification/
├── CIFAR10_Classification.ipynb     # 전체 코드 및 시각화
└── README.md                        # 과제 요약 문서
```
