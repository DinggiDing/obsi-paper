---
시작일: 2024-09-21
진행상태: true
tags:
  - HCI
  - Visualization
  - Ubiquitous
  - Personal-Informatics
  - VisualzationTool
sticker: emoji//1f469-200d-1f3eb
---
**multimodal Fusion**

텍스트, 이미지, 오디오 과 같은 다양한 소스의 데이터를 통합하여 기본 정보에 대한보다 포괄적이고 정확한 표현을 얻음.

# Introduction

스마트폰의 단점들로 인한(스크린 사이즈나 마우스 입력 X) 시각화의 어려움을 멀티모달 형식 (스피치와 터치)을 통해 해결함. → Fitbit API + iOS, Android

### 3 Key contribution

- **Data@Hand 앱의 설계 및 구현**: 이 앱은 스마트폰에서 개인 데이터를 탐색할 수 있도록 음성과 터치 입력 모달리티의 시너지를 활용한 최초의 모바일 애플리케이션입니다. 이 앱을 통해 사용자는 Fitbit 데이터에 접근하여 iOS와 Android에서 동작하며, Apple Speech Framework와 Microsoft Cognitive Speech API를 사용해 음성 인식을 지원합니다.
- **탐색적 연구 수행**: 13명의 장기 Fitbit 사용자와 함께 Data@Hand를 사용한 탐색적 연구를 진행하여, 사람들이 스마트폰에서 음성과 터치 상호작용을 사용해 개인 데이터를 탐색하는 방식을 이해했습니다. 이 연구를 통해 사용자들이 상호작용 선택에 대해 어떤 상황에서 어떤 이유로 선택했는지를 파악했습니다.
- **디자인 시사점 및 기회 제시**: 멀티모달 상호작용을 통한 모바일 데이터 시각화를 더 잘 지원하기 위한 디자인 시사점과 기회를 제시합니다. 사용자 관찰과 피드백을 반영하여, 개인 데이터 탐색을 보다 효과적으로 지원할 수 있는 설계 방향을 논의합니다.

- [[Think-Aloud]]

# 5C

### Category

Visualization, Personal informatics, Multimodal interaction

### Context

기존의 모바일 앱들은 제한된 화면 공간과 상호작용 방식으로 인해 유연한 데이터 탐색을 지원하지 못함 → 음성과 터치 상호작용을 결합하여 사용자가 스마트폰에서 더 쉽게 탐색할 수 있도록 돕는 방법을 제안

### Correctness

정량적 및 정성적 데이터를 통해 결과를 뒷받침하고, 윤리적 문제와 데이터 수집의 정확성을 고려하여 철저히 관리됨. 다만 연구의 표본 크기(총 13명)가 제한적이기 때문에 결과의 일반화에 한계가 있을 수 있음

### Contributions

- **Data@Hand 앱의 설계 및 구현**: 새로운 멀티모달 상호작용 방식의 도입.
- **사용자 연구를 통한 실증적 데이터 제공**: 멀티모달 상호작용이 개인 데이터 탐색에 미치는 영향을 연구.
- **디자인 시사점 제공**: 모바일 데이터 시각화를 개선할 수 있는 설계 방향 제시.

### **Clarity (명확성)**:

논문은 명확한 구조와 논리적 전개를 통해 연구 목표, 방법, 결과, 그리고 결론을 체계적으로 전달합니다. 각 섹션은 독자가 연구를 쉽게 이해할 수 있도록 구성되어 있으며, 시각 자료와 표를 사용하여 결과를 명확하게 제시합니다.

## 궁금증

- 어떻게 음성 명령으로 데이터를 탐색하거나 쿼리를 실행하였는지?
    - Compromise 라이브러리를 사용하여 텍스트에서 동사, 날짜, 데이터 소스 등을 파악함.
    - Chrono 라는 자연어 시간 파싱 라이브러리를 사용하여 다양한 시간 표현을 인식하고 해석할 수 있음.