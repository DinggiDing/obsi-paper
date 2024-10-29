---
시작일: 2024-09-21
진행상태: false
tags:
  - HCI
  - CollaborativeSocial
  - Personalization
  - AIGC
---
번역 시스템이 사용자의 개인적인 언어 스타일에 더 잘 맞춰져 다국어 커뮤니케이션 도구의 광범위한 채택과 만족도를 높이는 결과를 기대할 수 있습니다. Using UGTC(User-Generated Textual Content)

# 1. Introduction

- 현재 기계 번역 시스템에서는 언어적 스타일과 관련된 충분한 사용자 데이터를 수집하기 어렵고, 어떤 문장이나 단어가 개인화되어야 하는지에 대한 명확한 기준이 부족합니다
- So considering a user’s linguistic style preference in machine translation can be helpful for the systems to generate translations that are easily comprehended by the user and improve user experience.

# 2. Related Work

## 1. Linguistic Style

- each person has her/his preferred linguistic style and a unique stylistic ten- dency in communication.
- many features are proposed to represent linguistic style, including character-based features (e.g. the number of special characters and the number of white- space characters), word-based features (e.g. the total number of words and vocabulary richness), function words(e.g. the number of article words and the number of pro-sentence words), etc

## 3. Personalized Language Models

- Explicit Personalization : 성별, 전문성, 개인적 관심사 등 명서적 페르소나 프로필을 언어 모델에 도입
- Implicit Personalization : 사용자의 과거 활동에서 페르소나 프로필을 추출

# 3. USER-ORIENTED PERSONALIZED MACHINE TRANSLATION MODEL

- Transformer 사용하여 텍스트의 의미를 유지하면서 사용자 선호 스타일을 반영한 번역을 생성.
- BLEU를 사용하여 모델의 성능 평가
- 스타일 변환(사용자가 SNS에서 수집된 UGTC를 학습)
- 예를 들어, 사용자가 평소에 사용하는 친근한 표현이나 특정한 어휘를 번역에 반영함으로써, 번역 결과가 사용자에게 더 자연스럽고 친숙하게 느껴질 수 있습니다.