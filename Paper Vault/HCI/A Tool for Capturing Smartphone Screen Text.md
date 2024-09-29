---
시작일: 2024-09-21
진행상태: false
tags:
  - HCI
  - Ubiquitous
---
- 스마트폰에서 화면 텍스트를 캡처하는 새로운 센서를 개발하였으며, 이는 기존의 키보드 입력 또는 스크린샷 기반의 텍스트 수집 방법에 비해 더 정밀하고 지속적인 데이터를 제공합니다.

# 1. Introduction

- 기존의 텍스트 수집방법(in Smartphone)
    - 키보드 입력 데이터 수집 (감정, 스트레스 등 추론 가능)
    - 스크린샷 기반 데이터 수집 (OCR 기술 사용)
- AWARE-Light 프레임워크 이용하여 데이터 수집

# 2. Related Work

### 2.1 Context-aware smartphone sensing of behavior

- **헬스케어 분야**: 디지털 표현형(digital phenotyping) 연구에서는 GPS 데이터를 활용하여 정신 건강 상태, 사회성, 전반적인 건강 상태 및 웰빙, 성격 등을 평가할 수 있음을 보여주었습니다. 예를 들어, 우울증을 앓고 있는 사람들은 이동량이 적은 경향이 있으며, 반면에 이동량이 많은 사람들은 더 큰 사회적 네트워크를 가지고 행복감이 증가하는 경향이 있습니다.
- **교육 분야**: 스마트폰 센싱 전략은 교육에서도 광범위하게 탐구되었습니다. 예를 들어, WoBaLearn은 스마트폰의 빛 센서와 마이크를 사용하여 학습자에게 맞춤형 교육 콘텐츠를 제공하며, GPS 데이터를 활용한 개인화된 맥락 인식 학습 시스템은 학습자의 현재 위치를 기반으로 인근 학습 자료를 알리는 등의 방식으로 사용됩니다.
- 127, 120 참고문헌, 38, 73

# 3. Methodology

- Textual Feature : Screen(하나의 스냅샷), Phrase(텍스트 덩어리) 수집
- Text Metrics : total number of screens(정보 업데이트 정도), number of phrases per screen(정보를 측정하는 밀도), phrase difference(연속 두 화면 사이의 텍스트 변화량 측정)
- 보안

# 5. Result

- 감정분석 - 텍스트 + 행동패턴(시간대 사용 빈도, 화면 스크롤 속도 등) 을 이용하여 VADER 모델을 사용하여 Positivity, Negativity를 판단.