
-  InBody(체중/체지방 등), Apple Health(심박수 등), Google Fit(걸음 수 등)처럼 여러 소스에서 수집된 건강 데이터를 **한 곳**에서 자동 연동(Aggregation)하고,
- 사용자가 원하는 지표만 골라, 데이터에 맞는 최선의 시각화 UI 뷰를 사용자가 UI를 자유롭게 커스터마이징 할 수 있는 **mHealth Aggregator/Customizer** 앱을 제안.

- Problem
	- [[Towards Better mHealth Apps- Understanding Current Challenges and User Expectations]]
	- 여러 앱 간 기능 중첩: 여러 헬스앱을 쓰다 보면 비슷한 기능들이 중복되어 UI가 복잡해지고, 어떤 앱을 꺼내야 할지 헷갈림.
	- 불필요한/사용하지 않는 기능: 많은 헬스앱이 다양한 기능을 제공하지만, 사용자 입장에서는 일부만 필요하고 나머지는 사용하지 않음(40% 정도).
	- 수동 입력과 데이터 동기화 번거로움: InBody, Apple Health, Google Fit 등에서 데이터를 각각 수동 입력하거나, 앱 간 동기화가 제대로 이뤄지지 않아 중간에 누락이 생김(응답자의 55.7%가 불편함 호소).
	- most respondents preferred a unified platform for managing their health data(44.3% + 34.3%)
	- [[Toward a Unified mHealth Platform- A Survey of Current User Challenges and Expectations]]
	- 여러 앱을 사용할 때 주요 pain : data management
	- Apple HealthKit, Google Fit Framework에서 데이터 공유 메커니즘(robust data sharing mechanism)이 있지만, 모든 상업적인 앱들이 사용하지 않음.
	- 하나 이상의 앱을 사용하고 있는 절반 이상의 참가자(55.7%)가 사용하고 있는 앱들에서 수동적인 데이터 로깅에 불만이 있음.
	- 78.6%가  high levels of feature customizability와 single app 를 선호
	- complexity 문제 (mHealthSwarm 에서도 다룸)
	- privacy, security 문제
	- End-user toggle - to make apps customizable using feature toggles to manage an app's complexity and appeal.
	- Design Consistency - 모든 앱에서 각기 다른 UI를 사용.
	- Most users(40%) also accepted storing their health data on the cloud, which can also indicate their desire for simplified data mangement.
	- [[Data Collection Mechanisms in Health and Wellness Apps- Review and Analysis]]
	- 생각보다 많은 앱들은 건강정보를 모으기 위해 built-in sensor, wearable, bluetooth peripherals을 사용하지 않는다.
	- 이 논문과 Wisniewski의 논문 모두에서) 많은 앱들은 wearable에 대한 제한된 지원과 함께 manual entry에 의존한다. 
	- 많은 앱들과 디바이스가 독점 알고리즘을 이용해 호환성과 사용을 제한함.
	- 외부 및 내부 센서를 통한 수동 데이터 수집에 대한 제한된 지원은 UX 떨어트림.
	- [[A large scale analysis of mHealth app user reviews]]
	- 많은 사용자들이 그들의 니즈가 있고, 이를 mHealth app에 녹여내고 싶어함. (user review에 작성)
	- external device를 완벽히 지원하지 않아서 user review에 작성됨.
	- [The Spae of Mobile Health: A Sysmetic Review of Health Visualizatino on Mobile Devices]
> [!NOTE]
> “하나의 앱 안에서 사용자가 원하는 건강 데이터만 선택해서 자동으로 불러오고, 필요 없는 기능은 숨겨두거나 제거”

- https://www.businessofapps.com/data/health-app-market/?utm_source=chatgpt.com  Health App Market Share


**고려사항**
- Samsung Health SDK 같은 경우, Samsung partnership을 얻어야 사용 가능.
	- Google HealthConnect
- Apple HealthKit, Google Fit Framework에서 데이터 공유 메커니즘(robust data sharing mechanism)이 있지만, 모든 상업적인 앱들이 사용하지 않음.
- mHealthswarm 처럼 설계에 집중? User study X ?
- 설계 가이드라인
	- 앱의 데이터만 가져올껀지, ~~아니면 그 앱의 시각화 방법도 가져올껀지~~,(design consistency)
	- 예를 들어 그 앱의 수동데이터를 가져올 수도 있는지 등 파악. (제한적)
	- 
	- 여러 앱을 사용할 때 주요 pain : data management
	- complexity 문제 (mHealthSwarm 에서도 다룸_customization)
	- privacy, security 문제
	- 다양한 기기(Wearable, app)에 대한 데이터 필요
- User study 필요함. 
- 사용자가 데이터를 선택하고 그 데이터를 바탕으로 가장 좋은 시각화로 보여준다. 
- Motivation 이 중요하고, 이거에 대한 Needs를 잘 정리해야함.(Choe)
- FHIR , jamia 논문 보기.
- 여러 API 문의 요청드려놓기
- 클라우드 와 캐시 


- [[Investigating data accessibility of personal health apps]]
	- 3개의 Data access method로 Health platform, API, File Downloads도?
	- https://gyrosco.pe, https://exist.io 가 있다. 
	- 데이터 타입을 어느정도까지 해야하는지...

