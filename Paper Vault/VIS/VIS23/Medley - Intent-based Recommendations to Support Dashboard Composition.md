---
시작일: 2024-12-09
진행상태: false
tags:
  - Visualization
  - VisualizationDashboard
  - DirectManipulation
  - VisualizationRecommendation
sticker: lucide//settings-2
---
- We present Medley, a mixed-initiative interface that assists in dashboard composition by recommending dashboard collections that map to speific analyical intents.
- The system recommends collections based on these analytic intents, and view and widgets can be selected compose a variety of dashboards.
- lightweight direct manipulation interface
- We discuss how Medley's recommendations guide dashboard composition and facilitate different user workflows.

# 1 Introduction
---
- Although current visualization tools offer considerable support for creating individual views by recommending visual encodings or data fields, they provide limited support for discovering coherent groups of view that can be used to compose dashboards.
- Through a series of interview with dashboard authors and a survey of 200 dashboards, we identified four high-level dashboard intents - namely, measure analysis, change analysis, category analysis, distribution analysis

# 3 Usage Scenario
---
1. Starting with system recommendations - Top four recommendations(one per intent) presented during a cold start
2. Narrowing in on an intent while updating the dashboard
3. Providing an overview
4. Finalizing dashboard interactions and layout

# 4 Design Process and Goals
---
### 1 Identifying Dashboard Intents and Collections
- To identify a list of dashboard intents and representative collections of views and widgets that map those intents, we curated a list of 200 dashboards from Tableau and Microsoft Power BI's dashboard galleries.
- To scope our search and initial prototype design, we only focused on dashboards that consisted of two or more basic chart type(bar chart, map, large numbers)
- Besides frequency of occurence, we also followed Wang et al.'s giudelines to ensure that the resulting dashboard do not have an overwhelming number of view.
### 2 Design Goals
- DG1 - Support flexibility in dashboard composition
- DG2 - Support explicit user specification of attributes and intents
- DG3 - Support context-driven recommendations
- DG4 - Select default attributes based on data interestingness
- DG5 - Apply multi-view design guidelines in recommendations
- DG6 - Provide descriptive text to aid interpretation
- DG7 - Support for interactions during dashboard composition

# 5 Medley
---
- Three main components : an input panel, a list of collection recommendations, the dashboard canvas
### 1 Collection Recommendation Engine
- the system first determines the set of attributes the user is interested in by inspecting the input panel for explicit attribute selections as well as views in the canvas for implicit attribute references
#### 1 Collection Generation
- Medley generates a dashboard collection based on the attributes and intents selected by users.
- Algorithm
	- Choose Intent (Change Analysis) →  Collection ID (CH1) →  Attribute Mapping( {Q, T, 4C, G}) →  attribute sets {Profit, Date, Category, ...} →  choose metrics (bar chart, heatmaps, ...)
	- adisplay=a∈Amax​(n∑i=1n​viinterestingness​​)
#### 2 Collection and View Ranking
###### Ranking Collections
- C relevance ​=C attrMatch (an attribute match score) ​+ C coverage​ (a view coverage score)
- By ranking collections with a higher C attrMatch first, the system ensures that recommendations that focus on the attributes of interest are shown first.
###### Rankding views within collections
- Medley also ranks views within each collection to promote views that might be most relevant for the user to add next.

### 2 Interaction Configuration
- when the data summary view is selected, other views are faded out to indicate that clicking on the data summary view cannot update other views.
- clicking on a state in the map will update categories and values in the bar chart.
- highllight, filter

# 6 User Study
---
1) understand if and how collectino recommendations aid dashboard composition
2) gather feedback on Medley's current recommendations and features

- All studies followed a  [[Think-Aloud]]protocol

# 7 Discussion
---
- Medley supports flexible dashboard composition workflows
- Recommendations facilitate rapid exploration of alternatives
- Understading intents and objectives needs onboarding
- The Medley interface supports easy configuration of interactions


##### Discussion
- 현재 Medley 추천은 대시보드를 수동으로 조사한 결과를 바탕으로 한 휴리스틱 기반. 좀 더 고급 추천 시스템 필요.
- 향후 과제로 도메인별 지식을 컬렉션 추천에 통합하여 파생 attributes과 의미적으로 관련있는 시각화 선호도를 포함하는 방법을 조사하는 것.