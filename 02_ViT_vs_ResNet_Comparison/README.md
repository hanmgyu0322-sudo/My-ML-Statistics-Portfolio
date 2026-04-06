# 🌸 실습 02: ResNet-50 vs Vision Transformer (ViT) 성능 비교

이 프로젝트는 전통적인 **CNN(ResNet-50)**과 최신 **Attention(ViT)** 구조의 딥러닝 모델을 동일한 통계적 환경에서 비교 분석한 실습입니다.

## 🚀 실험 요약
- **목적:** 구조적 차이에 따른 꽃 30종 분류 성능 및 학습 효율성 비교
- **장비:** NVIDIA GeForce RTX 3070 Ti (CUDA 가속)
- **핵심 결과:** - ResNet-50 Test F1-Score: **(0.90)**
  - ViT-Tiny Test F1-Score: **(0.90)**

## 🔍 주요 시사점
1. **파라미터 효율성:** ViT-Tiny는 ResNet 대비 약 1/4의 파라미터만으로도 유사한 성능을 보임.
2. **지역성 vs 전역성:** CNN은 이미지의 지역적 특징에, Transformer는 전역적 문맥 파악에 강점을 보임을 추론 테스트를 통해 확인.
