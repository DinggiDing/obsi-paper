---
시작일: 2024-09-22
진행상태: false
tags:
  - HCI
  - EmpiricalStudies
sticker: lucide//settings-2
---
- **적용 분야**: 이 연구는 복잡한 다단계 작업 중 사용자 지원을 위해 대화형 에이전트(CA)에 상황 인식 기능을 통합하여 음성 에이전트를 개선할 수 있는 통찰력을 제공합니다.
- **결과**: 이 연구 결과를 적용하면 개발자는 오작동을 최소화하고, 사용성을 개선하며, 요리와 같은 복잡한 작업 중 인지 부하를 줄이는 더 자연스럽고 효과적인 VA를 만들 수 있습니다.
- **목표**: 상황 인식 VA가 복잡한 다단계 작업 중 상호작용을 어떻게 개선할 수 있는지 연구하며, 요리 작업을 사례로 사용합니다.

- [[Wizard-of-Oz Study]]을 사용

**연구 질문/가설**:
1. 상황 인식 VA는 복잡한 작업 중 대화적 문제를 줄일 수 있는가?
2. 작업과 대화의 상황을 통합하는 것이 VA 사용성을 어떻게 개선하는가?


# 1 Introduction
---
- 복잡한 작업에서의 상호작용은 여전히 만족스럽지 못하며 특히 연속적 대화에서 문제
- 긴급하거나 시간에 민감한 정보가 필요한 상황에서 VA가 어떻게 설계되어야 하는지에 대한 연구 부족
- VA의 **상황 인식 기능을 향상**시켜 복잡한 작업에서의 상호작용을 메커니즘을 개선하는 매커니즘을 제시


# 2 Related Work
---
- 현재 음성 에이전트의 한계
	- 단순 명령 구조(짧은 구문, 키워드)는 에이전트가 의사소통 실패를 겪을 수 있다는 인식


# 3 Experiments
---
### 3.1 Cooking Study 1: Commercial VA
- Using Google Assistant, 6 recipes
- They set up step on how the participant interact with the VA in the Cooking situation
- 3 participant from the University (None had used VA to cook before)

### 3.2 Cooking Study 2: Contextually-Aware Agent
- `Study 1` revealed the context misalignment
- They used [[Wizard-of-Oz Study]]
	- "Shared Vocabulary" development
	- "Receipe Progression" - The VA tracked the user's progress
	- "inclusion of proactive suggestions" - offering advice
- 16 participant from the University, 1 recipe
- Used [[Conversation Analysis(CA)]]

# 4 Result
---
### Object in Context
- 요리 중 사용자가 필요로 하는 구체적인 정보(재료, 도구)만을 제공함으로써 상호작용이 **더 자연스럽고 효율적**으로 진행되었습니다. 
- 사용자는 대화를 반복하거나 수정하는 일이 적었으며, 필요한 정보를 더 쉽게 얻을 수 있었습니다.

### The Task in Context
- 요리 작업의 **현재 상태를 정확히 인식**하고, 사용자가 완료한 작업을 바탕으로 **더 복잡한 명령을 처리** 가능

### Querying the Shared Context
- 이전 Context가 유지
- **전체 정보를 반복해서 묻지 않고**, 필요한 정보를 짧고 명확하게 요청
- Wake Word("Hey Google")을 반복하지 않고 가능

### Proactive Contextual Agents
- 타이머 설정, 대체 재료 등 추가적인 지원 제시
- Participant는 긍정적, 부정적 반응(VA's intervention 불편) 존재