
- Only 폰

- 사용자가 그래프를 이해하지 못하면 →  그래프를 이해하도록 다양한 그래프 표현?
	 - 사용자가 그래프 화면을 오랫동안 바라보고 있다 →  그래프를 이해하지 못한다
	 - 모바일 그래프 + 행동 데이터 + context-aware
- 건강, 헬스 쪽 앱 상에서 graph를 사용자에게 맞게끔 시각화하는데, 여기다가 context data, behavior data를 추가하여 개인화스럽게 시각화를 해보려고 생각중(more reflection)
	- 목적 : more reflection, 자신의 데이터를 더 깊게 이해할 수 있도록, 더 나은 행동 변화를 이끌어 낼 수 있도록
	Ex) 디바이스 스크린 크기나 카메라의 사용자 얼굴(기분, 나이 등), 개인적인 선호도 등을 추가하여 개인 데이터를 탐색하는 것

	- [[Narrating Fitness - Leveraging Large Language Models for Reflective Fitness Tracker Data Interpretation]] 그래프나 설명, 혼합 방법 등 가장 사용자들은 무엇을 좋아했는지
	- [[Exploring Context-Aware Mental Health Self-Tracking Using Multimodal Smart Speakers in Home Environments]]집 환경에서 
	- [[Data Formulator - AI-powered Concept-driven Visualization Authoring]]그래프 개인화
	- 대부분 콘텐츠를 개인화하거나, intervention, time 등도 개인화하기 시작함

##### 10/02
카메라의 사용자 얼굴로 나이 추적은 필요없을 듯, 어차피 요새는 Userprofile 정보 정도는 다 가지고 있어서...
사용자에게 몇가지 질문(논문에서 찾아야함)을 통해 사용자의 데이터 리터러시 정도를 파악.

- 스마트워치, 스마트폰, 태블릿, 컴퓨터에서 모두 헬스데이터를 확인? (Databite)
    - 적절한 수준의 Low level
    - [https://www.reddit.com/r/MacOS/comments/10ig27b/apple_health_on_macos/](https://www.reddit.com/r/MacOS/comments/10ig27b/apple_health_on_macos/)
    - When 스마트워치 → 스마트폰, Usability? (반대(Databiting))
- Time granularity
- responsive visualization tool은 대부분 복잡함. 예를 들어, annotation, filtering, tooltop, axis 등등
- 기존의 헬스케어앱에서는 어떤 그래프들을 사용하고 있는지
- 시각화 변환에 있어서, 해당 그래프가 어떤 것을 나타내고 싶어하는지를 잘 묘사하는 게 중요
- Template-based Tools:
	- 이 도구들은 사전 정의된 템플릿을 사용하여 데이터를 입력하면 즉시 시각화가 생성됩니다. 사용자는 특정 형식의 차트를 선택해 빠르게 시각화를 만들 수 있지만, 템플릿의 범위를 넘어선 세부적인 맞춤화는 제한적입니다.
    - **Datawrapper**: 사용자가 데이터만 넣으면 표준형 막대, 선, 파이 차트 등의 템플릿을 통해 간단하게 시각화를 생성할 수 있습니다.
    - **Flourish**: 다양한 차트 템플릿을 제공하여, 초보자도 복잡한 시각화를 손쉽게 구현할 수 있도록 돕습니다. 예를 들어 애니메이션 맵이나 타임라인 차트 등의 템플릿이 있습니다.
- 분 단위의 헬스데이터(Step Data)? > Swift HealthKit에서 상세하게 Step Data가 나와있음 (Start Time, End Time, Steps)
- 차트를 바꾸고 싶음. (mobile-first) 
	- mobile →  Desktop, Smartwatches
		- Time granularity 
		- 사람들은 데스크톱에서 어떤 데이터를 어떻게 활용하기를 원할까?
			- Chart + Data table
		- 스마트워치에서는 ?

### 11/12
##### 다양한 헬스 데이터 통합 및 디바이스별 맞춤형 시각화를 통한 개인 건강 관리 플랫폼 개발
*개인화 요소:
1. 사용자별 중요한 건강 지표 선택
    - 맞춤형 데이터 선택: 사용자가 자신의 건강 목표와 관심사에 따라 중요한 헬스 데이터 선택. (ex. 체중 감량을 목표로 하는 사용자는 칼로리 소모량과 섭취량에 집중할 수 있고, 수면 개선을 원하는 사용자는 수면 패턴과 질에 초점을 맞출 수 있음)
2. 개인 목표 설정 및 시각화 커스터마이징
    - 개인 목표 설정: 사용자가 달성하고자 하는 목표(예: 하루 10,000보 걷기, 수면 시간 8시간 확보 등) 설정.
    - 시각화 커스터마이징: 사용자가 선호하는 그래프 종류(막대 그래프, 선 그래프, 파이 차트 등), 색상 테마, 데이터 표시 방식 등을 선택하여 인터페이스 개인화.
3. 디바이스별 인터페이스 개인화:
    - 디바이스 특성 반영: 각 디바이스의 화면 크기, 상호작용 방식, 사용 맥락에 따라 시각화 요소와 인터페이스 최적화.
    - 사용자 선호도 반영: 스마트폰에서는 간단한 요약 정보와 알림을, 데스크톱에서는 상세한 분석과 보고서를 제공하는 등 사용자가 원하는 방식으로 정보 제공.

*1. 데이터 통합 방법*:
- 다중 디바이스 연동: 스마트워치, 스마트폰, 스마트 홈 기기 등에서 수집된 데이터
- 서드파티 앱 및 서비스 연동: 타사 건강 관리 앱이나 의료 기관의 데이터와 연동하여 더 풍부한 정보를 제공합니다. (건강검진, 수술기록 등)
- Self-tracking Data : 식습관 기록이나 혈압수치 등

 *2. 디바이스별 맞춤형 시각화*
**스마트워치
- 실시간 모니터링: 심박수, 걸음 수 등 실시간 데이터를 간단한 그래픽(예: 링 형태의 진행 바) 표시.
- 직관적인 알림: 목표 달성 여부나 활동 부족 시 진동이나 간단한 메시지로 알림 제공.
- 간단한 인터랙션: 터치나 제스처로 데이터 간 전환이 용이하도록 설계.
**스마트폰**
- 대화형 시각화: 터치 인터페이스 활용 스크롤, 줌 인/아웃 등으로 상세 데이터 탐색.
- 개인 목표 및 진행 상황 : 대시보드에 개인 목표와 달성률을 시각적으로 강조.
- 알림 및 피드백: 푸시 알림을 통해 중요한 이벤트나 조언 제공.
**데스크톱**:
- 심층 분석 도구: 복잡한 그래프와 차트를 활용하여 장기적인 추세 분석.
- 커스터마이징 가능한 대시보드: 위젯을 추가하거나 배치를 변경하여 사용자 정의 인터페이스 구성.
- 데이터 비교 및 상관관계 분석: 다양한 지표 간의 관계를 분석하고 시각화하여 인사이트 제공.

*3. 그 외*
- 사용자 선호에 따른 데이터 우선순위 설정 : 사용자가 선택한 주요 건강 지표만 (스마트워치, 스마트폰)에서만 보여주거나 관심없는 데이터는 숨기기
- 시각화 방식 : 사용자가 선호하는 시각화 방식 채택하여 데이터 이해도 높이기
- 데이터 프라이버시 : 사용자가 데이터 공유 범위와 대상을 설정 (의사, 가족)

*4. Persona*
**프로필**
- 나이 : 30대 직장인들로 구성된 팀
- 목표 : 개인별 걸음 수 챌린지 참여
스마트워치
- 실시간 걸음 수 추적: 개인의 일일 걸음 수를 측정하고 표시.
스마트폰
- 팀 대시보드: 개인 전체의 걸음 수 합계와 다른 사람과의 비교를 시각화.
데스크톱
- 종합 성과 분석: 챌린지 기간 동안의 활동 데이터를 분석하여 개인별, 팀별 성과를 평가.
- 다양한 시각화: 걸음 수, 걸음 속도, 외부 날씨 등 Multi-View 시각화

**프로필**
- 나이 : 70세
- 목표 : 일상생활에서의 안전과 건강 상태 모니터링, 가족과의 건강 정보 공유
스마트워치
- 낙상감지: 갑작스러운 충격이나 움직임 없을 경우, 감지
- 활동 수준 추적: 일일 활동량 모니터링
스마트폰
- 약 복용 관리 : 알람과 큰 글씨 등 복용 여부 확인
- 비상 연락 버튼 : 가족이나 의료 서비스에 연락
데스크톱
- 실시간 상태 모니터링 : 허가된 가족이나 의사가 데이터 체크
- 수술 기록 : 건강검진 데이터, 수술받은 기록 등 확인

**프로필**
- 나이 : 50세
- 목표 : 혈압과 혈당 관리하여 합병증 예방
스마트워치
- 실시간 모니터링 : 심박수와 혈압을 지속적으로 측정
스마트폰
- 혈당 관리 : 혈당 수치 기록 및 시각화
데스크톱
- 시각화 : 지난 6개월간의 혈압, 혈당, 체중 변화 등
- 의료진 공유 : 생성된 데이터들로 치료 계획 조정
- 식단 기록 : 당 섭취량을 관리하기 위해 음식 섭취내역 기록

### 11/20
Research Question
- Health Domain + Mobile에서 Interactive Visualization에서 interaction(zoom, 등)이 가능할 때, 사람들은 어떻게 데이터 탐색을 위해 사용하고 있는지와 데이터를 잘 이해하는지
	- 더욱 깊은 데이터탐색을 위해 어떻게 해야 Interaction을 사용할 수 있는지
	- 어떤 Interaction을 통해 data literacy를 높일 수 있는지
	- 시각화 차트에서 숨겨진 인터랙션을 확인할 수 있는지
- 모바일 Visualization을 고려할 때 많은 것들이 있음. 
	- Scale, Aspect ratio, Layout, Level of Detail, Amount of Data, Annotation & Guides, Attentional Cues / Dynamic Guides, Animation & Streaming Data, **Visual Encoding, Interaction.**
- AI? 버튼 크기 AI


- ### Visual Encoding
	- mobile-first design approach may lead designers to more responsive designs relative to a desktop-first approach
	- consistent primary mapping + secondary mapping that varies depending on device. ( by Radloff )
	- <font color="#ff0000"> Q. Bremer, Camoes 는 어떻게 모바일 디스플레이에 최적화된 형태라고 생각했는가?</font>
	- Semantic Zooming
	- morph from a line plot to a horizon chart when the height of the graph falls below a certain threshold
	- focus + context : matrix visualization →  scaled up to embedded chart
	- Table (not a chart)

연구 질문  
"모바일 기기에서의 상호작용형 시각화 기술이 사용자의 데이터 탐색 행동과 건강 데이터 이해에 어떤 영향을 미치며, 데이터 literacy 향상과 더 깊은 데이터를 탐색시키기 위한 상호작용 설계는 무엇인가?"
1.  숨겨진 상호작용
    - 숨겨진 상호작용 기능을 사용자가 어떻게 발견하는지
2. 사용자 상호작용 패턴
    - 사용자가 모바일 기기에서 건강 데이터를 탐색할 때 시각화와 어떻게 상호작용하는지(예: 줌, 팬 등) 분석.
	    - zoom&pan, Focus+context, Overview+detail, semantic zooming
1. 데이터 이해
    - 이러한 상호작용이 데이터를 더 잘 이해하도록 돕는지 평가.
2. 설계 전략
    - 데이터 문해력을 향상시키는 데 효과적인 상호작용 설계 및 프로토타입(예: 의미적 줌, 차트 변환 등) 확인.

---
~~연구 질문(more narrowly)
"모바일 건강 시각화에서 데이터 literacy 향상시키는 효과적인 시각적 인코딩 및 상호작용 기술은 무엇이며, 숨겨진 상호작용을 사용자가 쉽게 발견할 수 있도록 하는 방법은 무엇인가?"
1. ~~시각적 인코딩 기술
    - 모바일 화면에서 데이터를 효과적으로 표현하는 방법.
2. 상호작용 기술
    - 의미적 줌, 초점+맥락(focus+context)과 같은 기술이 깊이 있는 데이터 탐색에 어떻게 기여하는지.
3. 상호작용의 발견 가능성
    - 사용자가 사용할 수 있는 상호작용 기능을 인식하도록 만드는 전략.~~~~