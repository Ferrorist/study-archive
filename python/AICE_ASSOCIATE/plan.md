# 📘 AICE 대비 루틴 (12/2 ~ 12/19) — To-Do Checklist Version

*(groupby / agg / sort_values 완전 통합 버전)*

---

## 🧭 기본 전략

* **평일:** 30~60분 (집 3일 + 카페 2일)
* **주말:** 1~2시간 집중
* **Kaggle 실습 비중 강화**
* 목표: EDA → 전처리 → 시각화 → 모델링 → 평가 → 기출 대비 → 실전 분석 완성

---

# ✅ 2주차 (12/2 ~ 12/8) — 전처리 + 시각화 + 기초 ML + Kaggle 중심

---

## 📅 **12/2 (화) — 이상치 처리 + Kaggle 실습**

* [x] Z-score 개념 이해
* [ ] IQR 기반 이상치 탐지
* [ ] boxplot으로 이상치 시각 확인
* [ ] Kaggle Titanic/Housing에서 이상치 제거 실습

---

## 📅 **12/3 (수) — 결측치 처리 + groupby 기본**

* [ ] 결측률 계산
* [ ] 결측치 처리(fillna/dropna) 전략 2~3개 적용
* [ ] **groupby 기본 문법 학습**
* [ ] `df.groupby("컬럼").size()`
* [ ] `df.groupby("컬럼")["Value"].mean()`

---

## 📅 **12/4 (목) — 범주형 처리 + groupby 심화 + sort_values**

* [ ] get_dummies 실습
* [ ] Label Encoding 적용
* [ ] **groupby 심화(두 컬럼 이상)**
* [ ] `agg({"Fare": ["mean", "max", "min"]})`
* [ ] **sort_values 오름/내림차순 정렬**
* [ ] Titanic object 컬럼 자동 인코딩 함수 만들기

---

## 📅 **12/5 (금) — 시각화 실전**

* [ ] hist
* [ ] boxplot
* [ ] scatter
* [ ] seaborn pairplot
* [ ] 두 변수 관계 분석 그래프 3개

---

## 📅 **12/6 (토 · 집중 1.5h)**

### **Kaggle 실전 프로젝트 #1 — Titanic 전체 파이프라인**

* [ ] 데이터 로딩
* [ ] EDA(head/info/describe/null)
* [ ] 전처리(결측치/이상치/인코딩)
* [ ] 시각화
* [ ] **groupby로 생존율·평균 요금 계산**
* [ ] **sort_values로 요금 정렬**
* [ ] train_test_split
* [ ] Logistic Regression
* [ ] Accuracy / Confusion Matrix
* [ ] Notebook 1개 완성

---

## 📅 **12/7 (일 · 20~30분)**

### 2주차 정리

* [ ] 전처리 전략 요약
* [ ] **groupby / agg / sort_values 핵심 정리 1장**
* [ ] Titanic Notebook 정리
* [ ] GitHub 업로드

---

## 📅 **12/8 (월 · 30분)**

### 기초 ML 마무리

* [ ] Logistic Regression vs SVC 비교
* [ ] accuracy 비교
* [ ] Titanic에 두 모델 적용

---

# ✅ 3주차 (12/9 ~ 12/15) — 실전 기출 + 평가 지표 + Kaggle 확장

---

## 📅 **12/9 (월) — EDA 기출 풀이**

* [ ] filtering 기출 문제 3~5개
* [ ] groupby 기출 문제 2~3개
* [ ] Titanic 기반 데이터 해석

---

## 📅 **12/10 (화) — 모델링 기출 풀이 + 지표**

* [ ] accuracy 계산
* [ ] precision / recall / f1 계산
* [ ] confusion matrix 시각화
* [ ] Titanic 기반 문제풀이

---

## 📅 **12/11 (수) — 회귀 지표 정복**

* [ ] MAE
* [ ] MSE
* [ ] RMSE
* [ ] R²
* [ ] Kaggle Housing Prices로 실습

---

## 📅 **12/12 (목 · 카페 · 40~60분)**

### 실전 모의 분석 #1 (1시간 제한)

* [ ] EDA (15분)
* [ ] 전처리(15분)
* [ ] 모델링(15분)
* [ ] 평가/해석(15분)

---

## 📅 **12/13 (금 · 집 · 20~30분)**

### 기출 재풀이

* [ ] 기출 문제 5개 재풀이
* [ ] 틀린 문제 기록 및 해설 작성

---

## 📅 **12/14 (토 · 집중 1.5~2시간)**

### Kaggle 실전 프로젝트 #2 — 새로운 데이터로 전체 분석

추천 데이터:

* Heart Disease

* Stroke Prediction

* Mall Customers

* [ ] 전처리 → EDA → 모델링 → 시각화 → 평가 전체 구현

* [ ] Notebook 1개 완성

---

## 📅 **12/15 (일 · 20~30분)**

### 3주차 정리

* [ ] 전처리/지표/평가 핵심 정리
* [ ] 나의 약점 리스트 작성
* [ ] 암기 대상 추출

---

# ✅ 시험 직전 주간 (12/16 ~ 12/19) — 암기 + 모의 분석 + 최종 정리

---

## 📅 **12/16 (월)**

* [ ] Pandas 함수 50개 복습
* [ ] 전처리 전략 암기
* [ ] Filtering 문제 20개 풀이

---

## 📅 **12/17 (화)**

* [ ] 모델 성능 지표 암기
* [ ] accuracy / precision / recall / f1
* [ ] mse / rmse / r²
* [ ] 지표 계산 문제풀이

---

## 📅 **12/18 (수)**

### 실전 모의 분석 #2 (30~40분 제한)

* [ ] CSV 로딩 → EDA → 전처리 → 모델링 → 평가
* [ ] 모델 해석

---

## 📅 **12/19 (목 · 시험 전날)**

### 전체 흐름 1회 리허설

* [ ] 데이터 로딩 → EDA → 전처리 → 모델링 → 평가 전체 재현
* [ ] Titanic 30분 컷 연습
* [ ] 마지막 약점 보완
* [ ] 1~2시간 이내로 마무리

---

# 🏁 최종 요약

* **전처리 → 시각화 → 모델링 → 평가** 흐름 완성
* Kaggle 기반 실전 경험 강화
* 3주 주기 안에서 시험 수준까지 자연스럽게 상승
* 마지막 3일은 “암기 + 모의 분석” 집중