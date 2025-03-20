
- Sleeptight 처럼 Mobile에서 Lock screen widget에서 건강데이터로 시각화하는 것이 아이폰, 안드로이드에서 가능한지, 어느정도 가능한지 → 추후 걸음 수를 보고 싶으면, 여러 차트들을 보여주고 사용자들이 선택하도록, 그러면서 Health Literacy가 높아지게…, 또는 걸음수와 심박수를 같이 본다거나 (like omnitrack visualization version)
- 애플헬스, 삼성헬스, 구글헬스, 하웨이헬스에서 어떤 데이터들을 지원하고, 어떤 Visualization이 있는지
	- https://www.figma.com/design/InKD34FtoGHhb9uqqpdETN/MOBVIS?node-id=1018-2&node-type=canvas&t=neRXElU5UEEzRaRh-0
		- [[Data-Task-Visualization Analysis based on Top mHealth Apps]]

- iOS - Interactive Widget?
	- https://gyuios.tistory.com/267



- 데이터 : 건강 데이터(Apple Health, or Google Health) + 수동 데이터? + 외부 데이터?
- 위젯 크기에 따라 (2x2, 2x4, 4x4)
- direct manipulation interface
- workflow 간소화
- 데이터 선택 →  여러 차트 추천(도메인 기반) →  사용자가 차트 선택
- 자신이 track 할 차트만 보기 때문에 집중
- mobile widget visualization paper X

- 차트 추천
	- 휴리스틱 기반 
		- 데이터에 따라 ([[Show Me - Automatic Presentation for Visual Analysis]])
		- Intents 에 따라 ([[Medley - Intent-based Recommendations to Support Dashboard Composition]])
	- AI 기반
		- [[MultiVision- Designing Analytical Dashboards with Deep Learning Based Recommendation]]


- how to design visualization tool
	- followed Wang et al.’s guidelines (In the Multiple Views) to ensure that the resulting dashboards do not have an overwhelming number of views (e.g., collections focus on 1-3 primary attributes and contain no more than 10 views) [[Medley - Intent-based Recommendations to Support Dashboard Composition]] 
	- 건강 추적 앱의 주요 동기는 재미와 호기심. 또한 main challenges로는 차트와의 상호작용 부족, 제공된 데이터의 복잡성, 차트 표현의 일관성 부족. 읽기 쉬운 customizable and complete charts 는 앱을 자주 사용하는 데 도움을 줌. (Alshehhi_Needs and Challenges of Personal Data Visualizations in Mobile Health Apps: User Surver. BigComp 23)
	- 현재 타 헬스앱의 Widget 시각화 조사?
	- DG 1 : visualization tasks (filtering, ordering, grouping, maximum and minimum) [[Analysis of Personal Data Visualization Reviews on mHealth Apps]]
	- DG 2 : Interactivity (scrolling, zooming, landscape, choose graph options) [[Analysis of Personal Data Visualization Reviews on mHealth Apps]]
		- 작은 화면으로 안보이기 때문에 Zooming 필요
- Implementation
- 사용자 study 로 무엇을 도출하고 싶은지
	- 사용성 평가
	- 데이터 이해
	- 데이터 탐색
	- self-reflection 촉진
	- Feedback 위주로



- 위젯 시각화 조사?
- [[Towards Better mHealth Apps- Understanding Current Challenges and User Expectations]]respondents were more inclined towards a highly customizable app that would allow then to customizable features according to needs(44.3% + 34.3%)
- [[6DVF- Data Visualization Framework for mHealth Apps]]consider 1. identifying the target audience, 2. chart functionality, 3. data representation, 4. visual design and interactivity, 5. target device, 6. single/app visualization interface for non-expert users and the context of mhealth tracking.
- [[Needs and Challenges of Personal Data Visualisations in Mobile Health Apps User Survey]] Participants prefered to control the chart and its presented data.
	- We designed the study based on the *design thinking process* and the *value proposition canvas* as the two widely adopted.
	- These approaches were chosen as they were adopted in devloping and envaluating mHealth apps.
- [[Personal Data Visualisation on Mobile Devices- A Systemtatic Literature Review]]
	- We found that, small screen is the main issues of adopting personal data visualisation on mobile devices. Futhermore, scale-ability, battery drain and limited functionality issues were results of studies conducted in reviewing applications.
	- In contrast, the built in sensors, powerful processor, high resolution display, providing personal space, low maintenance and easy access to data have supported mobile devices to be adopted in visualizing personal data.
- [[Understanding User Perspective on Data Visualization in mHealth Apps - A Survey Study]]이 논문이 종합.
	- Relatedwork로
		-  A 2018 study([[Making Sense- An Innovative Data Visualization Application Utilized Via Mobile Platform]]) presented a prototype of a data visualisation app for health data using PhoneGap
			- 3 main concerns : colour usage, complex data visualisations, lack of ideal data visualisations.
		- Kim([[A Systematic Review on Visualizations for Self-GeneratedHealth Data for Daily Activities]]) highlighted the need to consider various aspects of data visualisation design, including selecting suitable data, determining effective visualisation type, and incorporating interactive feature to enhance user engagement.
- https://www.data-to-viz.com  - 어떤 차트를 선택해야하는지 Decision Tree 제공
- 왜 D3가 아닌 모바일 언어를 사용했는지...
- 위젯 - reflection 높인다.



# Customizable mHealth Visualization widget 개발 평가

## 연구 범위 설계
- 사용자가 스마트폰 위젯을 통해 자신의 건강 관련 지표(걸음 수, 심박수, 수면 패턴 등)를 즉각적으로 확인할 수 있도록 하는 차트들을 제공.
- 사용자들은 위젯 상에서 차트를 슬라이드하거나 선택하여 특정 기간, 특정 지표를 확대/축소해 볼 수 있음.
- 이를 통해 사용자가 ~~자신의 건강 상태 변화를 더 잘 이해~~하고, 필요한 경우 운동량을 늘리거나 식습관을 개선하는 등 피드백 루프를 형성.
- (Snakable contents, Databiting)

연구 질문(Research Questions)
1. RQ1: 모바일 위젯 형태의 건강 데이터 시각화는 사용자가 ~~자신의 건강 상태를 쉽게 이해~~하는 데 도움을 줄 수 있는가?
    - 예: 기본적으로 제공하는 숫자 정보(걸음 수, 심박수) 대비 차트 기반 시각화가 변동 추세 파악, 주기적 패턴 인식 등에서 이점이 있는지.
2. RQ2: 사용자 커스터마이제이션(Customization)을 이용할 경우, 사용자의 만족도, 사용성, ~~정보 이해도가~~ 어떻게 달라지는가?
    - 예: 사용자들이 좋아하는 차트(라인, 바, 히트맵), 표시 기간(일간, 주간, 월간), 강조 지표(걸음 수 vs 심박수)를 스스로 선택할 때 더 빈번한 조회나 높은 만족도가 나타나는지.
3. RQ3: 해당 위젯 사용 경험이 사용자 행동이나 인식에 단기적 변화(운동량 증가, 수면 시간 관리)를 유발할 수 있는가?
    - 예: 위젯 사용 전후로 사용자들이 운동 목표를 설정하거나 수면 패턴 개선 의지를 갖는지.


## 연구 방법 설계
- Prototype 
	- **모바일 위젯(Android/iOS)**: 안드로이드 스튜디오(Android) 또는 Xcode(iOS) 네이티브 언어(위젯에 Webview를 못 겹침)를 사용하여 실제 동작 가능한 위젯 형태로 구현.
	- **사용자 실제 건강 데이터** : 구글 핏(Google Fit), 애플 헬스킷(Apple HealthKit) 등의 API, 테스트시에는 샘플(더미) 데이터 이용.
- Dashboard Design
	- **Design Guideline** 
		- 모바일 특성을 고려한 간결한 시각화
		    - 작은 화면, 터치 기반 인터랙션의 제약 → 복잡도 낮추기, 색상 명확히, 데이터 단계적 표시.
			- [[Making Sense- An Innovative Data Visualization Application Utilized Via Mobile Platform]]에서 복잡한 시각화, 부적절한 컬러는 이용을 방해함.
		- 사용자 목적(Goal)·태스크(Task)를 구체적으로 지원
		    - 데이터 타입에 따른 시각화, 최댓값/최솟값 파악, 비교 차트 등 주요 기능에 집중.
		    - https://www.data-to-viz.com 의 Decision Tree를 활용
		    - [[A Systematic Review on Visualizations for Self-GeneratedHealth Data for Daily Activities]]에서 건강 데이터 시각화에는 데이터 타입과 사용자 태스크에 적합한 차트 선택이 중요함을 강조.
		    - [[Understanding User Perspective on Data Visualization in mHealth Apps - A Survey Study]]RQ3에서 최댓값/최솟값 찾기(25.45%), 활동 진행도·비교(20.74%)가 대표 태스크임을 지적.
		- 데이터 완결성과 탐색 편의성 보장
		    - 불완전한 데이터는 분명히 안내, 필요한 정보에 빠르게 접근 가능하게 UI 설계.
			- [[Understanding User Perspective on Data Visualization in mHealth Apps - A Survey Study]]RQ4에서 ‘Not showing the information’, ‘I cannot see a chart of my entries’ 등이 반복적으로 거론.
			- 불완전한 데이터는 UX 및 사용성에 안좋은 영향을 미친다는 것을 여러 논문에서 말함.
		- 충분한 커스터마이제이션과 상호작용 범위 제공
		    - Read-only부터 Drill-down, 차트 편집까지 다양한 니즈에 대응하되, 복잡도를 최소화할 수 있는 디자인이 중요.
	
	- View 구성
		- Data Selection View →  Chart Selection View > Task Selection View→  Visualization View
		- 작은 화면 크기로 인해 View를 나눔.
		- Chart selection 먼저일지, Data selection 이 먼저일지...?
- 사용자 연구 방법
	- **사용 로그 데이터**
		- Firebase analytics 이용
		- “사용자가 위젯을 몇 시에 몇 번 열어봤는지”, “차트 타입을 며칠에 몇 번 변경했는지” 등 사용자 행동을 기록하는 로깅 설계.
		- 개인정보 보호를 위해 최소한의 식별자(익명화 ID)와 행동 기록만 저장.
	- “정적 위젯 vs 개인화 가능한 위젯”처럼 두 조건을 비교하는 A/B 실험인지, 하나의 위젯을 특정 기간 사용하게 한 뒤 설문과 인터뷰를 병행하는지

## 프로토타입 개발
- Low-fidelity → High-fidelity
	- Figma →  xcode + android studio
- Pilot study



또한, 많은 연구들은 paper-based 연구가 많고, 디자인에만 치중할 뿐, 실제 데이터 형식 및 정보 구조화에 관한 연구는 개발을 해야 확인이 되므로 연구가 미흡하다.

사용자 건강 데이터 통합하여 시각화하기 전에, 데이터가 어떻게 구조화되고 정리되어야 사용자들이 가장 쉽고 의미 있게 활용할 수 있는지 정보 설계(Information Architecture) 관점에서 탐구하고자 합니다. 구체적으로는,

- 여러 기기·앱에서 수집된 다양한 유형의 건강 데이터를 통합하고,
- 데이터가 사용자 목표(다이어트, 만성질환 관리 등)에 맞춰 알기 쉬운 형태로 정리·필터링·요약될 수 있도록,
- 여러가지 데이터 구조화 방식 중에서 사용자 UX가 증가한 데이터 구조화 방식

Li et al.’s stage-based model of personal informatics systems 에서 reflection stage의 여러 장벽들의 문제는 reflection stage만의 문제가 아닌 그 전 단계들인 preparation, collection, integration 들로 인해 발생되지 않나?  →  논문에 따르면 그 전 단계들이 영향을 끼친다. →  즉, 우리는 Intergration을 통해 뒤의 Reflection의 문제점을 해결하고자 한다.

- 왜 이런 방식이 필요한가? 사용자들이 더욱 customization을 잘하도록 하기 위해, 더 데이터 선택을 잘하기 위해
- 정보 설계는 결국 data를 잘 찾기 위해서 한다. customization을 할 때, 결국에 검색을 할 것이고, 이 과정에서 건강 데이터 타입을 찾을 것인지, 날짜를 찾을 것인지, 디바이스 별로 볼 것인지 (나아가 task를 볼 수도) 다양한 방법이 존재한다. 