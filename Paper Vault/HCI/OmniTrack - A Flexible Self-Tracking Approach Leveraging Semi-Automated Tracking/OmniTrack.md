---
시작일: 2024-09-25
진행상태: false
tags:
  - HCI
sticker: lucide//settings-2
---

**핵심 요점**
1. OmniTrack은 수동 입력과 자동 데이터를 결합하여 유연한 셀프 트래킹 플랫폼을 제공함.
2. 이 시스템은 사용자가 추적 항목을 개인화할 수 있어 다양한 트래킹 요구 사항을 충족할 수 있음.
3. 사용성 연구 결과, OmniTrack은 초보자와 숙련된 셀프 트래커 모두가 쉽게 사용할 수 있음.

- semi-structed interview(12 participants), analyzing mobile tracking app(62 apps), usability study(10 participants), 3-week deployment study(21 participants)


# 1 Introduction
---
- 현재 셀프 트래킹 도구와 웨어러블 기기들이 매우 많음에도 불구하고, 사용자들이 자신의 **특별한 필요**나 **선호도**에 맞는 도구를 찾기 어렵다는 문제를 지적합니다.
- 상용 셀프 트래킹 앱들은 일반적으로 특정 기능에 한정되며, 사용자가 트래킹 방식이나 항목을 쉽게 **맞춤화**하거나 **변경**하기 어렵다는 한계가 있습니다. 이는 사용자가 초기 설계에 의해 도구의 기능에 **제한**을 받게 된다는 의미입니다.
- 사용자가 자신이 필요로 하는 데이터를 수동으로 입력하면서도 외부 기기나 서비스로부터 자동으로 데이터를 가져올 수 있는 유연성을 제공합니다.

### 3 Contributions
1. **design** - flexible & customizable self-tracking
2. **implement**
3. **evaluate**


# 2 Related Workd
---
### 2.3 Semi-Automated Tracking
- **반자동화 추적**을 수동 및 자동 추적 방식의 **어떤 조합**으로든 정의하며, 자가 모니터링 시스템을 설계할 때 **반자동화 추적**을 활용할 것을 제안[^1]
	- 데이터 캡처의 가능성, 자가 모니터링의 목적, 자가 추적자의 동기 수준
- Omnitrack : 외부 트래킹 서비스를 가져와 연동할 수 있다는 장점

[^1]: Semi-AutomatedTracking:A Balanced Approach for Self-Monitoring Applications(Cheo)

# 3 Preliminary Study
---
- Interviews
    - 인터뷰를 통해 사용자가 현재 셀프 트래킹 도구를 어떻게 사용하고 변형하는지 이해했으며, 상용 앱이 이들의 요구를 충분히 충족하지 못한다는 점이 드러났습니다. 특히 상용 도구의 불편함 때문에 많은 사용자가 일반 용도의 도구를 변형해 사용하고 있었음.
- Analysis of Trackgin App (Apple App Store):
    - 시장에 나와 있는 많은 트래킹 앱들은 특정 데이터를 추적하는 데 매우 **한정적**이고, 사용자 맞춤형 데이터 필드를 지원하지 않는 경우가 많습니다. 또한, 기존 앱들은 대체로 **수동 데이터 입력**에 의존하며, 외부 기기와의 통합이 제한적입니다
- **앱에서 지원해야 할 필드 유형** (숫자, 텍스트뿐만 아닌)을 식별하여 OmniTrack의 설계에 반영함. 이는 트래커를 보다 **유연하게 설계**하고, **맞춤형 필드**와 **외부 데이터 통합** 기능을 포함하도록 설계하는 데 중요한 역할을 함.


# 4 Omnitrack
---
#### Goal
1. Cover a braod range of tracking practices
2. Lower the data capture burden
3. easily create, manipulate, modify
4. support on the phone
- using *reminders*, *shortcut panel*  to ensure users don't forget to track their data

#### System Design
1. Trackers (lists all the existing trackers the users created)
	1. more diverse data fields (e.g., text, number, ratings, choice, location, image, etc.)
	2. using the last logged value, internal semantic, Fitbit data to reduce user input
	3. reminders to input a new tracking entry
2. Triggers (lists all the triggers the users created)
	1. when triggers are activated, Omnitrack retrieves tracking value from external services and automatically logs the values
	2. Time-based : triggers occur at preset time or periodic intervals
	3. Data-driven : trigger sets off an action when a tracking value passes the threshold set by users
3. external services
	1. easily connecting external data(Fitbit, Misfit) without requiring manual input
	2. value connection to use query scope(starting from 12:00 AM)
4. using Google Firebase to conduct usability study in real time
5. Visualization
	- Heatmap timeline
	- duration chart
	- line chart
	- histogram


# vs **M**indLamp
---
### 사용 목적
- Omni : 개인 맞춤형 셀프 트래킹, 자신의 개인적 목표, 맞춤화 O
- Mind : 환자 대상, 건강 상태 추적, 감정기록, 스마트폰 센서 데이터, 맞춤화 X

### 데이터 유형
- Omni : 수동 데이터 & 외부 데이터(Fitbit)
- Mind : 스마트폰 센서 데이터(GPS, ...), 감정 평가, 인지 테스트(survey)