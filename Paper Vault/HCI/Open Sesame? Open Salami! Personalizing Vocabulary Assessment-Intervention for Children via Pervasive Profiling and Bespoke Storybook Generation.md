---
시작일: 2024-09-21
진행상태: false
tags:
  - HCI
  - AIGC
---
# Introduction

to enable personalized vocabulary assessment and intervention, by blending into a child’s everyday routines and bespoke creation of intervention aids.

### 3 Key contribution

- **임상 원칙에 기반한 맞춤형 어휘 평가 및 중재 시스템 구현**: OSOS는 아동의 일상 언어 환경을 프로파일링하고, 개인화된 목표 어휘를 추출한 후 이를 맞춤형 동화책으로 통합하여 제공하는 시스템입니다. 이 시스템은 기존 표준화된 도구의 한계를 극복하고, 아동의 고유한 언어 환경에 적응할 수 있는 평가 및 중재 방법을 제시합니다.
- **맞춤형 어휘 우선순위화 및 동화책 생성의 첫 구현**: 이 연구는 임상적 프레임워크에 기반한 맞춤형 어휘 우선순위화와 생성형 AI를 활용한 맞춤형 동화책 생성을 최초로 시도하였으며, 이를 통해 개인화된 어휘 중재가 가능함을 실증하였습니다.
- **실제 환경에서의 종합적인 연구 결과 보고**: OSOS를 9가족에게 4주간 배포하여 얻은 사용 경험과 임상적 시사점을 종합적으로 분석하였습니다. 이 연구는 시스템의 실제 적용 가능성을 평가하고, 이를 통해 아동의 어휘 학습을 개인화하고 일상 생활에 자연스럽게 통합할 수 있는 방법을 제시하였습니다.

# 5C

### Category

교육 기술, 언어병리학, AI 기반 교육 도구

### Context

아동의 언어 환경이 점점 더 다양해지고 있는 현대 사회에서, 표준화된 어휘 평가 도구가 각 아동의 개별적인 필요를 반영하지 못한다는 문제. 특히, 기존의 표준화된 도구들이 고정된 어휘 목록을 사용하여 개인 맞춤형 평가가 어렵다는 점 → 교육 기술과 언어 치료의 최신 흐름과 맞물려 있으며, AI와 생성형 모델의 발전을 활용하여 보다 개인화된 학습 경험을 제공하려는 시도를 반영합니다.

### Correctness

9가족을 대상으로 4주간의 실제 환경에서의 배포 연구를 수행했으며, 데이터 분석을 통해 맞춤형 어휘 중재가 아동의 어휘 습득에 미치는 긍정적인 영향을 명확히 제시합니다. 또한, 사용된 기술과 알고리즘에 대한 설명이 잘 이루어져 있으며, 윤리적 고려 사항과 연구의 한계도 명확히 언급되어 있습니다.

### Contributions

1. **임상적 원칙을 통합한 맞춤형 어휘 평가 및 중재 시스템 구현**: 아동의 개인적인 언어 환경에 적응하는 시스템을 제시함으로써 표준화된 도구의 한계를 극복했습니다.
2. **맞춤형 어휘 우선순위화 및 AI 기반 맞춤형 동화책 생성**: 임상적 프레임워크에 기반한 어휘 우선순위화와 맞춤형 동화책 생성을 최초로 구현하여 실질적인 중재 도구로 활용했습니다.
3. **실제 환경에서의 검증**: OSOS 시스템을 실제 가정 환경에 배포하여 종합적인 사용자 경험과 임상적 시사점을 도출했습니다.

### Clarity

논문은 명확하고 논리적으로 잘 구성되어 있으며, 연구의 배경, 목적, 방법론, 결과 및 결론이 명확하게 제시됨.

# OSOS System

아동의 가정에서 음성을 수집하여 언어 환경 분석.(아동이 자주 접하는 단어와 아직 익히지 않은 단어를 식별). 아동에게 가장 중요한 어휘들을 대상으로 LLM(GPT-4)을 사용하여 스토리라인 생성 + Stable diffusion 생성형 AI를 사용하여 일러스트 제작.

Linear Regression을 통해 우선순위 리스트 제작.

$$ priorityscore𝑠(𝑤𝑖) =𝑘𝑓 𝑓(𝑤𝑖)+𝑘𝑐𝑐(𝑤𝑖)+𝑘𝑝𝑝(𝑤𝑖) $$