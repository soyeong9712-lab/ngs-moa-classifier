# ngs-moa-classifier

 NGS-MoA Classifier: RNA-seq 기반 항암 약물 반응 예측 (Machine Learning)

 1. Overview

RNA-seq 기반 유전자 발현 데이터를 활용하여
항암 약물(12b)에 대한 반응성을 예측하는 머신러닝 프로젝트입니다.

소규모 실험 데이터 환경에서 높은 신뢰도를 확보하기 위해
Feature Selection + Ensemble 기반 모델을 설계함

2. Key Features
   
소규모 데이터(n=18)에 최적화된 머신러닝 모델
ElasticNet 기반 Feature Selection (핵심 유전자 추출)
RandomForest + LogisticRegression Soft Voting 앙상블
LOOCV 기반 모델 평가
생물학적 해석 가능한 모델 구조

3.  Model Architecture
   
✔ Feature Selection
Logistic Regression (ElasticNet)
L2 정규화 기반 핵심 유전자 선별
✔ Classification Model
Random Forest
Logistic Regression
Soft Voting Ensemble

4. Results
LOOCV (Leave-One-Out Cross Validation) 기반 평가
Classification Accuracy: 100%
오분류 0건

핵심 인사이트:

소규모 실험 데이터에서는 딥러닝보다
머신러닝이 더 안정적이고 신뢰도 높은 결과를 제공

5. Data
   
Internal Dataset
RNA-seq gene expression data
Sample size: n = 18
Treated (12b): 9
Control: 9
특징
실험 조건 통제 → 높은 라벨 신뢰도
소규모 데이터 → 과적합 방지 중요

6. Biological Insight
   
Feature Selection을 통해 약물 반응 관련 핵심 유전자 추출
MAPK pathway 등 생물학적 기전과의 연관성 확인

 단순 분류 모델이 아닌
 해석 가능한 바이오 AI 모델

7. Limitations
   
데이터 수 부족 (n=18)
외부 데이터 일반화 불가능
선형 모델 기반 → 복잡한 패턴 학습 한계

8. Role in Overall Project

이 프로젝트는:

✔ Deep-KPT 딥러닝 모델의 Baseline 역할
✔ 내부 데이터 기준 성능 검증 모델
✔ Feature Selection 기반 해석 제공

 즉, "신뢰도는 ML, 확장성은 DL" 구조의 핵심 축

9. Tech Stack
    
Python
Scikit-learn
Pandas / NumPy

10. Installation
    
python -m venv .venv
# Windows
.\.venv\Scripts\Activate.ps1

pip install -r requirements.txt
