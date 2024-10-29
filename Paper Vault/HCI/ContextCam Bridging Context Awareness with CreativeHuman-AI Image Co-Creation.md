---
시작일: 2024-09-21
진행상태: false
tags:
  - HCI
  - AIGC
  - context-aware
---
**AIGC : AI-generated content**

# 1. Introduction

AI + environmental information(location, weather) + personal states(facial expression, music, screen content)

“framing” + “focusing”

- framing : user intent → 3 themes for the image inspiration
- focusing : image feedback (edit using natural language command and selection)

Analyze : log data + interview

- [[Open Coding]]사용
- [[Thematic Analysis]]사용

# 4. System design

- 색상을 이용하여 주제 1,2,3에 어떤 데이터가 사용되었는지 표시
    - 녹색(모든 주제) / 파란색(주제1,2) / 노란색(주제3) / 흰색(관련X) / 회색(사용자가 닫은 정보)

- [[Weng's LLM-powered system]]사용
- [[Few-Shot-CoT]]사용

### Few-Shot-CoT
- 2 Phase(framing, focusing) + 5 agent(Context selector, topic agent, tool manger, artist agent, personalization agent)
    
    ### Context selector
    
    - 모든 컨텍스트를 줄 필요가 없기 때문에 적절한 컨텍스트만 선택하기 위한 agent
    - 위치, 화면 콘텐츠, 표정, 날씨, 음악 정보를 Standard Vector로 표현
        - User Intention Mode에 따라 Standard Vector가 달라짐
    
    ### Topic agent
    
    - 컨텍스트 데이터를 바탕으로 사용자가 선택할 수 있는 3가지 이미지 주제를 추천
    - 주제 1과 2는 Standard Vector 기반으로 만들어짐
    - 주제 3은 Vice Vector 로 일부 Context 데이터를 추가하거나 제외하여 다른 주제를 제안(이는 더 다양한 아이디어를 제공하기 위한 목적)
    
    ### Tool Manger
    
    - 이미지를 생성할지 편집할지 도구를 결정 (Stable diffusion, ControlNet 중 결정)
    - 과거 기록을 통해 사용자의 선호 스타일을 기억
    
    ### Artist Agent
    
    - 사용자가 선택한 주제에 맞는 아이디어 제안 및 이미지 설명(image-to-text model)
    
    ### Personalization Agent
    
    - 이전의 agent들에서 사용자의 선호도를 기억

# 5. User study

- [[7-point likert scale]]사용
- [[Content Analysis]]사용
- [[grounded theory methodology]]사용

# 7. Limitations and future work

- With the advancements in sensing technology, we will incorporate real-time detection of user physiological data, including heart rate, body temperature, activity levels, sleep quality, and step count
- 수집하는 컨텍스트 데이터의 양과 민감도를 고려하여, 사용자 프라이버시 보호와 데이터 보안을 강화해야하는 연구 필요.
- 다양한 동기부여 매커니즘 등 개인화 작업에 필요.

# 5C

### 1. Category (카테고리)

이 논문은 **인간-컴퓨터 상호작용(Human-Computer Interaction, HCI)** 및 **AI 기반 창작 도구**에 관한 연구로 분류됩니다. 특히 **컨텍스트 인식**과 **이미지 생성** 기술을 결합한 새로운 **인간-AI 협업** 모델을 제안하고 있으며, 이는 창의적 AI 응용 분야에 속합니다.

### 2. Context (컨텍스트)

이 연구는 AI 기술이 점점 더 창의적인 작업에 적용되는 시점에서 진행되었습니다. 기존의 AI 이미지 생성 도구들은 사용자 개인의 컨텍스트를 충분히 반영하지 못한다는 한계를 가지고 있었는데, 이 논문은 이러한 한계를 극복하기 위해 컨텍스트 인식을 도입한 **ContextCam** 시스템을 제안했습니다. 이 시스템은 사용자의 환경적 요소(위치, 날씨, 감정 등)를 반영하여 더욱 개인화되고 의미 있는 창작 경험을 제공하려는 의도에서 개발되었습니다.

### 3. Correctness (정확성)

논문의 연구 방법론과 결과는 신뢰할 만한 것으로 보입니다. 연구진은 사용자의 컨텍스트 데이터를 수집하고, 이를 기반으로 이미지 생성 및 편집 작업을 수행하는 **ContextCam** 시스템을 개발했습니다. 이를 평가하기 위해 실제 사용자들을 대상으로 한 **사용자 연구**를 실시하였으며, 높은 사용자 만족도와 참여도를 보고했습니다. 논문에 제시된 데이터와 분석 방법은 논리적이고 체계적이어서 연구의 정확성을 뒷받침합니다.

### 4. Contribution (기여도)

이 논문은 AI와 인간의 협업을 더욱 효율적이고 창의적으로 만드는 중요한 기여를 합니다. 특히 **컨텍스트 인식**이라는 새로운 접근 방식을 통해 AI가 더 개인화된 창작 도구로 발전할 수 있음을 보여줍니다. 이는 AI 이미지 생성 기술의 새로운 방향을 제시하며, 향후 다양한 창작 분야에서 응용될 가능성이 큽니다. 또한, 논문은 **LLM 기반 멀티 에이전트 시스템**을 활용하여 AI와 사용자의 상호작용을 향상시키는 방법을 제안함으로써, 기술적 혁신을 이끌어 냈습니다.

### 5. Clarity (명확성)

논문은 전반적으로 명확하게 작성되었습니다. 연구 목표, 방법론, 결과, 그리고 결론이 체계적으로 서술되어 있으며, 각 섹션이 논리적으로 연결되어 있습니다. 특히 **framing**과 **focusing** 단계, 그리고 **멀티 에이전트 시스템**의 구성 요소들이 잘 설명되어 있어, 독자가 연구의 흐름을 쉽게 이해할 수 있습니다.

# 궁금증

- Context selector에서 어떻게 컨택스트를 선택한건지
    - 0과 1로만 컨택스트의 중요성을 나타내는 것은 다소 아쉬운 부분이 아닐까?