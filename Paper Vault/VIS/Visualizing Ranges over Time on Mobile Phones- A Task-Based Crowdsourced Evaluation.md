---
시작일: 2024-10-17
진행상태: false
tags:
  - HCI
  - Visualization
  - mobile
  - crowdsourcing
sticker: lucide//settings-2
---
- VIS 18
- This paper address the growing need for effective visual representations of **time-based** range data on mobile phones (with [[Crowdsourced experiment]])
- They **compare** two ways that one is a conventional **linear layout** that strikes a balance between quantitative and chronological scale resolution, the other is a less  conventional **radial layout** that emphasizes the cyclicality of time and prioritize discrimination between values at its periphery[^1]
[^1]: Outside the boundary of something
- Quickly completed tasks : Linear > Radial
- Error rate : Linear ≈ Radial

# 1 Introduction
---
- we study how people experience visual representations of quantitative information when constrained by the size and aspect ratios of small displays.
- They analyze 4 factors in crowdsourced experiment using their own mobile phones
	- Layout
		- linear layouts
		- radial layouts
	- Data source
		- a city's daily high & low temperatures
		- a person's sleep schedule of bedtimes & waking times
	- Granularity(세분성)
		- Week, Month, Year
	- Task
		- five value retrieval(검색)
		- comparison tasks

# 3 Experiment
---
### 1. Two Source of Range data
- Temperature range data -<font color="#7f7f7f"> Seattle's daily high and low temperatures for every day of 2015</font>
- Sleep duration range data - from a person's data posted on reddit
- Performing data preprocessing on both
- These two datasets differ in data charicteristic from the perspectives of pattern period, average period and data domain

### 2. Three Levels of Temporal Granularity
- Existing weather and sleep-tracking mobile apps vary in terms of the ranges shown in a single chart, from 7 days of ranges to a range for every day in a month
- Week(7), Month(28~31), Year(365, 366)

### 3. Two Layouts: Linear and Radial
- In a Linear range chart, the quantitative scale is orthogonal to the chronological scale(horizontal)
- In a radial range chart, the quantitavie scale emanates from lower value in the centertoward higher values at the periphery(주변)
	- Advantage : emphasizes visual continuity, reinforcing cycles
	- Disadvantage : It may suggest continuity where none exists

### 4. Range Encoding
- our implementation applies a unique color gradient to each range via a LAB interpolation through a 3-class diverging red-yellow-blue scale

### 5. Tasks
- Locate Date
- Read Value
- Locate Min / Max
- Compare Values
- Compare Ranges

### 8. Metrics
- Completion Time
- Error Rate
- Subjective Responses

### 9. Participants
- Using Amazon Mechanical Turk (survey platform)


# 4 Result
---
- Participants' Completion Times grew as the `Granularity` increased
- more participants preferred a Linear layout to a Radial one, and they were more confident using a Linear layout
- participants were less confident as the `Granularity` increased


# 5 Dicussion
---
- `Linear layout` - more confident in using
- `Radial layout` - indentifying trends or deviations from seasonal patterns
- Performance generally worsened as the `Granularity` increased
- For large data(Yearly data), aggregation techniques or hierarchical navigation(drill down interaction) can be employed to enhance usability on mobile devices