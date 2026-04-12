# 🌸 실습 03: ConvNeXt V2 기반 꽃 30종 분류 및 특징 다양성 분석

본 프로젝트는 CNN의 효율성과 Transformer의 학습 기법을 결합한 최신 아키텍처인 **ConvNeXt V2**를 활용하여 고정밀 이미지 분류를 수행하고, 모델 내부의 특징 추출 메커니즘을 통계적으로 검증한 실습입니다.

## 🚀 실험 요약
- **모델:** ConvNeXt V2 (Atto) - FCMAE Pre-trained
- **장비:** NVIDIA GeForce RTX 3070 Ti (8GB VRAM)
- **핵심 결과:** - **Test Accuracy/F1-Score:** 90% 달성
  - **특징 다양성 점수:** 0.9982 (특징 붕괴 방지 검증 완료)

## 🔬 심화 분석: FCMAE & Feature Collapse
단순 분류 성능 측정을 넘어, 논문에서 제시한 **GRN(Global Response Normalization)** 레이어의 효과를 정량적으로 분석했습니다.
- **FCMAE Masking:** 이미지의 60%를 가린 상태에서도 핵심 특징을 추출하는 강건함(Robustness) 확인.
- **Feature Diversity:** 채널 간 코사인 거리를 계산하여 특징 붕괴 현상이 없음을 증명.

## 📊 실험 환경
- **Optimizer:** AdamW (lr=1e-4, weight_decay=0.05)
- **Loss:** CrossEntropyLoss
- **Split:** Train 70% / Val 15% / Test 15% (Seed 42)

## 🔍 주요 시사점
1. **현대적 CNN의 효율성:** ResNet-50 대비 적은 파라미터로도 최신 기법(LayerNorm, GELU, GRN)을 통해 우수한 성능 기록.
2. **이론적 근거 확보:** 특징 다양성 지표를 통해 모델의 내부 표현력을 수치화하여 분석함.
