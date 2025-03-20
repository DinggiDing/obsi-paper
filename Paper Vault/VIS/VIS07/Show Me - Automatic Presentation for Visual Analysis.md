---
시작일: 2024-12-10
진행상태: false
tags:
  - HCI
  - Visualization
  - VisualAnalysis
  - AutomaticPresentation
  - VisualizationDashboard
  - Recommendations
sticker: lucide//settings-2
---
- Show Me, an integrated set of user interface commands and defaults that incorporate automatic presentation into a commercial visual analysis system called Tableau

# 2 Related Work
---
### 3 Chart Type Menus
- Excel supports the following workflow:
	1. Select the data to be presented
	2. Invoke a menu of chart types
	3. Select a chart type
- The user may not know the chart type that will address their task
- This Paper address this issues by using automatic presentation techniques to focus on the selected data rather than the list of chart types.
- In particular, the *Show Me Alternatives* menu described below contains only 14 items, which automatically build charts that have appropriate organization for the selected data

# 3 Automatic Marks
---
- Automatic Marks rules are based on data properties of the data fields that specify axes and header of the table panes.
	- 3 Data properties : Data type, Data role(measure or dimension), Data interpretation(discrete or continuous)
- Automatic Marks take advantage of the Tableau data model, which includes the following classification
	- C = Categorical (discrete and dimension), Cdate = Categorical date(date or date&time)
	- Q = Quantitative (continuous), Qd = Quantitative dependent(measure), Qi = Quantitative independent(dimension)

##### 이 논문에서의 추천
1. 데이터 속성 분석 : 데이터 유형, 역할, 해석
2. 추천 알고리즘 : Tableau 데이터 모델 분류와 Automatic Marks 활용
	- 연속형 시간 데이터 →  Line chart 가 Default
	- 이산형 범주 데이터 + 수치 데이터 →  Bar chart 가 Default
- 데이터의 행과 열 구조를 분석해 가장 적합한 차트를 결정 
- 데이터 필드간의 Affinity를 고려해 필드 배치를 조정
- 초보자는 Default에 의존할 수 있고, 전문가는 세부조정을 통해 원하는 시각화 생성할 수 있음.
- 휴리스틱 규칙 사용 (Affinity, Empty view에서 시작)