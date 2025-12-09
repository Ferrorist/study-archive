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
* [x] IQR 기반 이상치 탐지
* [x] boxplot으로 이상치 시각 확인
* [x] Kaggle Titanic/Housing에서 이상치 제거 실습

---

# ✅ **12/8 (일) — 결측치 처리 + groupby 기본**

* [x] 결측률 계산 (`df.isnull().sum() / len(df)`)
* [x] 결측치 처리 전략 3종(평균/최빈/삭제)
* [x] `fillna()` 실습
* [x] `dropna()` 실습
* [x] groupby 기본 문법 학습
* [x] `df.groupby("컬럼").size()`
* [x] `df.groupby("컬럼")["Value"].mean()`

---

# ✅ **12/9 (월) — 범주형 처리 + groupby 심화 + sort_values**

* [x] `get_dummies()` 실습
* [x] Label Encoding 적용
* [x] groupby 다중 컬럼
* [x] `agg({"Fare": ["mean", "max", "min"]})`
* [x] `sort_values()` 오름/내림차순 실습

---

# ✅ **12/10 (화) — 시각화 핵심 + Titanic 그래프 3개**

* [ ] `hist()`
* [ ] `boxplot()`
* [ ] `scatter()`
* [ ] seaborn `pairplot()`
* [ ] Titanic에서 변수 2~3개 시각화

---

# ✅ **12/11 (수) — Kaggle 실전 #1 (Titanic 전체 파이프라인)**

* [ ] Kaggle Titanic 데이터 로딩
* [ ] EDA: head/info/describe/null 확인
* [ ] 전처리: 결측치/이상치/인코딩 처리
* [ ] groupby로 생존율 분석
* [ ] `sort_values()`로 요금 정렬
* [ ] `train_test_split`
* [ ] Logistic Regression 학습
* [ ] accuracy 계산
* [ ] Notebook 1개 완성

---

# ✅ **12/12 (목) — Logistic vs SVC**

* [ ] LogisticRegression 적용
* [ ] SVC 적용
* [ ] 두 모델 accuracy 비교
* [ ] 차이점 정리(선형 vs 비선형)

---

# ✅ **12/13 (금) — EDA + groupby 기출 풀이**

* [ ] filtering 기출 문제 3~5개
* [ ] groupby 기출 문제 2~4개
* [ ] Titanic 데이터 기반 해석 실습

---

# ✅ **12/14 (토 · 1.5~2h) — Kaggle 실전 #2**

추천 데이터: Heart Disease, Stroke Prediction, Mall Customers

* [ ] EDA 전체
* [ ] 전처리
* [ ] 시각화
* [ ] 모델링(Logistic/SVC/RandomForest 중 택1)
* [ ] 평가 지표 계산
* [ ] Notebook 1개 완성

---

# ✅ **12/15 (일) — 2주차 핵심 정리**

* [ ] 전처리 전략 요약
* [ ] groupby / agg / sort_values 정리 1장
* [ ] 시각화 핵심 패턴 정리
* [ ] Titanic 파이프라인 전체 흐름 요약

---

# 🔥 **12/16 (월) — Pandas 집중 암기 + Filtering**

* [ ] Pandas 핵심 함수 50개 중 필수 30개 암기
* [ ] Filtering 문제 15~20개
* [ ] 자주 틀리는 부분 기록

---

# 🔥 **12/17 (화) — 성능 지표 완전 정복**

* [ ] Accuracy 계산
* [ ] Precision / Recall / F1
* [ ] MAE / MSE / RMSE / R²
* [ ] 직접 계산 문제 5~10개

---

# 🔥 **12/18 (수) — 모의 실전 분석 #1 (40분 제한)**

* [ ] CSV 로딩
* [ ] EDA 10분
* [ ] 전처리 10분
* [ ] 모델링 10분
* [ ] 평가/해석 10분
* [ ] 40분 내 완성 목표

---

# 🔥 **12/19 (목 · 시험 전날) — 전체 흐름 리허설**

* [ ] Titanic 전체 파이프라인 30분 컷
* [ ] 함수/지표 최종 복습
* [ ] 약점 보완
* [ ] 불필요한 실습 금지, 정리만 수행

---

# 🏁 **12/20 (금 — 시험 당일)**

* [ ] 핵심 정리본 20~30분 가볍게 복습
* [ ] groupby / filtering / 모델 지표만 다시 보고 시험장 이동