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

# 📅 **12/2 (화) — 이상치 처리 + Kaggle 실습**

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

# ✅ **12/9 (화) — 범주형 처리 + groupby 심화 + sort_values**

* [x] `get_dummies()` 실습
* [x] Label Encoding 적용
* [x] groupby 다중 컬럼
* [x] `agg({"Fare": ["mean", "max", "min"]})`
* [x] `sort_values()` 오름/내림차순 실습

---

# ✅ **12/10 (수) — 시각화 핵심 + Titanic 그래프 3개**

* [x] `hist()`
* [x] `boxplot()`
* [x] `scatter()`
* [x] seaborn `pairplot()`
* [ ] Titanic에서 변수 2~3개 시각화

---

# ✅ **12/11 (목) — Kaggle 실전 #1 (Titanic 전체 파이프라인)**

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

# ✅ **12/12 (금) — Logistic vs SVC**

* [ ] LogisticRegression 개념 복습 및 정리
* [ ] SVC 개념 복습 및 정리
* [ ] 차이점 정리(선형 vs 비선형)

---

# ✅ **12/13 (토) — EDA + groupby 기출 풀이**

▣ Part 1 — Logistic vs SVC 실전

* [ ] Titanic에 Logistic 적용
* [ ] Titanic에 SVC 적용
* [ ] accuracy 비교
* [ ] 차이점 정리 (표로 정리 추천)

▣ Part 2 — EDA + groupby 기출 풀이
* [ ] filtering 3~5개
* [ ] groupby 2~4개
* [ ] Titanic 기반 해석 문제

---

# 🍀 **12/14 (일 · 1.5~2h) — Kaggle 실전 #2 (새로운 데이터)**

→ 실전 응용 능력 강화

추천 데이터셋: Heart Disease / Stroke / Mall Customers

* [ ] EDA 전체
* [ ] 전처리
* [ ] 시각화
* [ ] 모델링(Logistic/SVC/RandomForest 중 택1)
* [ ] 평가 지표
* [ ] Notebook 완성

---

# 📘 **12/15 (월) — 기출 + 정리 중심(가벼운 날로 조정)**

👉 원래 너가 말한 것처럼 “핵심정리”가 월요일은 아님
👉 평일이므로 **정리 + 기출 반복** 위주로 최적화함

* [ ] 전처리 기출 3~5개
* [ ] groupby / filtering 문제 다시 5개
* [ ] Titanic 파이프라인 흐름 요약(1페이지)
* [ ] 내가 헷갈리는 개념 5~7개 정리

---

# 🔥 **12/16 (화) — Pandas 집중 암기 + Filtering 훈련**

→ 시험 전 4일차는 “암기 + 문제풀이”가 가장 효율적

* [ ] Pandas 핵심 함수 30개 외우기
* [ ] Filtering 문제 15~20개
* [ ] 틀린 문제 기록

---

# 🔥 **12/17 (수) — 성능 지표 완전 정복**

→ 수치 문제는 단기간 반복이 필요

* [ ] Accuracy
* [ ] Precision/Recall/F1
* [ ] MAE/MSE/RMSE/R²
* [ ] 계산 문제 5~10개 직접 풀기

---

# 🔥 **12/18 (목) — 모의 실전 분석 #1 (40분 타임어택)**

* [ ] EDA 10분
* [ ] 전처리 10분
* [ ] 모델링 10분
* [ ] 평가/해석 10분
  👉 시험의 “실전 감각” 키우는 날

---

# 🚀 **12/19 (금 · 시험 전날) — 전체 흐름 리허설 (가벼운 반복)**

→ 부담 높은 실습 금지, ‘복습만’ 수행

* [ ] Titanic 파이프라인 1회(30분)
* [ ] 전처리 전략 요약 다시 보기
* [ ] Filtering 5개
* [ ] 성능지표 공식 다시 확인
* [ ] 헷갈리는 부분 마지막 체크

---

# 🏁 **12/20 (토 — 시험 당일)**

* [ ] 핵심 정리본 20~30분만 보기
* [ ] groupby / filtering / 지표만 다시 확인
* [ ] 심리 안정시키고 시험장 이동