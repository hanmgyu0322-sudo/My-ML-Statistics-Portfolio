# 🌸 실습 01: ResNet-50 기반 꽃 30종 이미지 분류

본 실습은 딥러닝의 대표적인 CNN 구조인 **ResNet-50**을 활용하여 아카시아를 포함한 30가지 종류의 꽃 이미지를 분류하는 프로젝트입니다.

## 🚀 실험 개요
- **목적:** 사전 학습된(Pre-trained) ResNet-50 모델의 전이 학습(Transfer Learning) 성능 검증
- **장비:** NVIDIA GeForce RTX 3070 Ti (CUDA 가속)
- **주요 지표:** Weighted F1-Score **0.92** 달성

## 📊 실험 환경 (Environment)
- **Framework:** PyTorch 2.5.1
- **Architecture:** ResNet-50 (Residual Learning 적용)
- **Dataset:** 30 Classes (Acacia, Rose, Tulip, etc.)
- **Split:** Train 80% / Validation 20%

## 📈 주요 결과 (Key Takeaways)
- **Residual Connection의 효과:** 깊은 층에서도 기울기 소실(Gradient Vanishing) 문제 없이 안정적으로 학습됨을 확인.
- **통계적 검증:** 클래스별 데이터 불균형을 고려하여 **Weighted F1-Score**를 최종 평가지표로 채택, 모델의 신뢰성을 확보함.

## 📁 주요 파일
- `flower_classification_resnet.ipynb`: 학습 및 검증 전체 코드
- `loss_curve.png`: 에폭별 Loss 변화 그래프
