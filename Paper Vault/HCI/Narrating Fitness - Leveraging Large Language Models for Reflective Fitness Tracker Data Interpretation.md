---
시작일: 2024-09-24
진행상태: false
tags:
  - HCI
  - EmpiricalStudies
sticker: lucide//settings-2
---
**핵심 결론**
- LLM이 생성한 질적 피드백은 기존의 차트만 제공된 경우보다 더 많은 성찰과 집중을 유도합니다.
- 텍스트와 차트를 함께 제공하는 방식이 사용자에게 효과적인 피트니스 데이터 해석 방법으로 확인되었습니다.
- 사용자들은 일반적인 피드백보다 더 구체적이고 개인화된 설명을 선호합니다.

# 1 Introduction
---
- Their goal takes different path by emphasising the role of **reflection** in understand personal fitness data
	- Tranditional system support quantitive goals(steps taken, calories burns)
- Many users are reluctant to accept recommendations from the PI system
- Research Question : "How can we use LLMs to encourage engagement with and facilitate reflection on fitness tracker data?"
- 10 participants(for insights) → 273 participants, [text-only / standard chart / text + chart]
	- reflection, UX measurement
### 3 Contributions
1. **pre-study interview**  : How users feel about transforming fitness data and automatically generated descriptions
2. **online experiment** : How there AI-generated narratives influence reflection on the users' personal data
3. **insights on the potential of generative AI** : improving the quality of reflection in PI systems


# 3 Method
---
- tailored GPT-4 prompt, [[open-ended question]]to capture feedback

# 4 Pre-study : Interviews
---
- They used open-coding with 2 authors independatly
	- →  3 Themes : Abstraction, Tone, Role of AI
		- Abstraction : ambiguity from AI text
		- Tone : too optimistic and positive
		- Role of AI : challenge of unclear, transparency

# 5 Online study
---
연구는 **Terra API**를 사용해 참여자들의 피트니스 트래커 데이터(걸음 수)를 수집했습니다. 이 데이터는 할당된 조건에 따라 시각화 또는 텍스트 서사로 변환되었습니다.

- **LLM 텍스트 생성**: **GPT-4**를 사용하여 텍스트 서사를 생성했습니다. 텍스트는 **사용자의 성찰**을 유도하기 위해 일일 활동 패턴을 비교하고 인사이트를 제안하며, 지나치게 지시적이지 않도록 설계되었습니다.

#### 5.3 성찰 및 참여 측정
참여자들의 경험을 평가하기 위해 두 가지 주요 측정 도구가 사용되었습니다:
1. **TSRI (Technology-Supported Reflection Inventory)**: 참여자들이 자신의 피트니스 데이터에 대해 얼마나 성찰했는지 측정했습니다. **인사이트**, **비교**, **탐색** 같은 요소에 중점을 두었습니다.
2. **UES-SF (User Engagement Scale - Short Form)**: 제공된 피드백에 대한 사용자 **참여도**를 측정했으며, **집중력**, **사용 편의성**, **보상성**을 평가했습니다.

#### 5.4 연구 절차
참여자들은 **Prolific**을 통해 모집되었으며, 무작위로 세 가지 조건 중 하나에 배정되었습니다. 피드백(텍스트, 차트, 또는 텍스트+차트)을 검토한 후, 참여자들은 성찰(TSRI)과 참여도(UES-SF)를 측정하는 설문을 작성했습니다.

- **소요 시간**: 연구는 약 15분이 소요되었으며, 참여자들은 자신의 데이터를 검토하고 설문을 완료했습니다.


# 6 Online study results
---
- Text-only > Text + chart > chart