---
시작일: 2024-10-28
진행상태: false
tags:
  - HCI
  - Visualization
  - VisualizationDashboard
sticker: emoji//1f469-200d-1f3eb
---
- Difference overlays (GB+D[^1], SB+D[^2]) significantly outperformed other designs for maximum change tasks.
- Over 85% of participants prefered chart designs with difference overlays for ease of understanding and speed
[^1]: Grouped Bar Chart with Difference Overlays
[^2]: Single Bar Chart with Difference Overlays

![[what's the Difference?.png|500]]

**Research Questions**:
- Which bar chart variant best supports tasks involving identifying extremes, differences, and changes?
- How do difference overlays impact task completion time and accuracy?

# 1 Introduction
---
- *“I want to compare the traffic of the user during summer 2015 versus summer 2014.”* Unfortunately, it is not always possible to compare these values directly within a single chart; these values may be represented in separate charts, pages, and tabs, or they mmay only be visible following some interactive configuration.
- Results suggest that chart with difference overlays facilitate a wider range of comparison tasks than the charts without them, performing comparably to the grouped bar chart and difference chart on the comparison tasks for which those charts are better suited

# 3 Online Experiment
---
#### 4 chart design conditions
- implement Justaposition(병렬), Explicit encoding, Superposition(겹치기) for multi-series bar charts
- They decided to constrain our scope in two ways
	1. Fixed how the categories were sorted
		- In the Constant categories condition, diplayed from left to right
		- In the Varying categories condition, be ordered by their target series value

**Grouped Bar Chart(GB)
- One of the most familiar charts, and an instance of a `Justaposition`-based design
- Having no distractor bars may lead to more accuracy
**Difference Chart(D)
- instance of an `Explicit encoding`-based design that encodes dervied values
- the difference between correspoindg values across the two series can be negative
- as a baseline condition
**Single Bar Chart with Difference Overlays(SB+D)
- `Explicit encoding` + `Superposition`
- both target series values and the difference can be observed directly
**Grouped Bar Chart with Difference Overlays(GB+D)
- `Explicit encoding` + `Superposition` + `Justaposition`
- It has the most information encoded of all the chart design condition

# 4 Procedure
---
1. Introduction and conset
2. Chart design introduction
3. Data Introduction
4. Traning phase
	- no response time, feedback on the participant's responses
5. Testing phase
	- performance would be timed with no feedback provided
6. Preference specification
7. Demographic information submission

#### Hypotheses
Our overall hypothesis was that charts with difference overlays (GB+D) and (SB+D) facilitate more visual comparisontasks than exclusively explicit-encoding based charts (D) or exclusively juxtaposition-based charts (GB).
**H1**. Difference overlays are just as good or better than Justaposition alone for *extreme value identification* tasks, at least for the target series
**H2**. Difference overlays are just as good or better than Explicit encoding alone for the *identification of the maximum absolute changes*
**H3a**. Difference overlays are just as good or better than explicit encoding alone for *difference measurement*
**H3b**. Difference measurement is *difficult* without explicit encoding
**H4**. Difference overlays are the best way to *identify missing values* in either series

# 5 Result
---
#### Subjective Preference
- They most prefered. 63 participants selected the grouped bar chart with difference overlays
	- "provided the most information while being the least confusing"
	- "decreases the time to think about the amount in the difference"
#### H1
- Participants were comparably accurate with GB and GB+D when identifying extreme values in the source series
#### H2
- They were less accurate using the exclusively juxtaposition-based design (GB)
- Completion times followed a similar trend, as participants were slowest with GB.
#### H3
- explicit encoding does not guarantee more accurate difference measurement, but it appears to reduce the time to complete the task.
#### H4
- participants were fastest with GB and GB+D, and they were comparably accurate

# 6 Dicussion
---
- These chart(GB+D, SB+D) allow viewers to identify extreme values, large changes, and quickly assess the magnitude of changes, BUT they did not support the identification of missing values
- 63 participants opted for GB+D as their most prefered chart design
- when displaying difference overlays, It is preferable to have both target and source reference values as GB+D has more accurate than SB+D


# My Idea
- 차이가 중첩된 차트로써의 신박함. 상업적으로 사용되지 않다보니
- Limitation에도 있듯이 bar chart 뿐만 아니라 line chart와 bar chart를 겹쳤을 때에는 어떤 효과가 나타날까 라는 궁금증과 heatmap 등 다양한 차트타입에서 활용하면 신박한 차트 디자인이 나오지 않을까
- Difference를 사용자가 어디서 받아들일 수 있을까 생각하니, 헬스 데이터에서 이번 달 10일과 저번 달의 10일의 차이나, year 데이터로써의 차이나, 내가 목표로 세운 칼로리의 차이로 motivation 효과를 지니지는 않을까? 라는 생각이 듬
- 이런 차트는 스마트워치에서 유독 효과적이라고 생각이 드는데, 컴퓨터나 스마트폰에서는 비교적 스크린 사이즈가 크다보니 아무래도 다양한 차트를 보기에 효과적이지만, 스마트워치에서는 작은 스크린 사이즈로써 다양한 데이터를 보여줘야하는데, 그럴 때 너무나도 좋을 것 같다라는 생각이 듬