---
Author: Bahador Saket
진행상태: false
tags:
  - HCI
  - Visualization
시작일: 2025-02-18
sticker: lucide//settings-2
Jounal: TVCG 2018
---
- two-dimensional visualization types(Table, Line Chart, Bar Chart, Scatterplot, Pie Chart) across ten common data visualization design would benefit from considering context-dependent effectiveness.
- Based our findings, we derive recommendations on which visualizations to choose based on different tasks. →  Desicion tree

# 5. Results
---
- Results, aggregated over tasks and datasets, show that Bar chart is the most fastest and the most accurate visualization type
- Line Chart has the lowest aggregate accuracy and spped. But Line chart is significantly more accurate than other charts for Correlation and Distribution tasks.
- While Pie Chart is comparably as accurate and fast as Bar Chart and Table for Retrieve, Range, Order, Filter, Extremum, Derived and Cluster tasks, it is less accurate for Correlation, Anomalies and Distribution tasks.
- Bar Chart and Table are the two visualization types highly preferred by participants across most of the tasks.

- Retrieve Value
	- accuracy : Bar chart, Table, Pie chart
	- time : Table, Pie chart
	- preference : Table
- Filter
	- accuracy : all
	- time : Bar chart, Table
	- preference : Table, Bar chart, Pie chart
- Compute Derived Value
	- accuracy : Table, Bar chart, Pie Chart
	- time : Table
	- preference : Table
- Find Extermum
	- accuracy : all
	- time : Bar chart
	- preferences : Bar chart
- Sort
	- accuracy : Bar chart
	- time : Bar chart
	- preference : Bar chart
- Determine Range
	- accuracy : all
	- time : all
	- preference : all
- Characterize Distribution
	- accuracy : all
	- time : Scatter plot
	- preference : Bar chart
- Find Anomalies
	- accuracy : Scatter plot
	- time : Bar chart
	- preference : Bar chart, Scatter plot
- Cluster
	- accuracy : Bar chart, Pie chart
	- time : Pie chart, Bar chart
	- preference : Bar chart, Table
- Correlate
	- accuracy : Line chart, Scatter plot
	- time : Line chart, Scatter plot, Bar chart
	- preference : Bar chart, Line chart

# 6. Discussion
---
- we do not advocate generalizing the performance of a specific visualization on a particular task to every task.
- Our results show user preferences correlate with user accuracy and speed in completing tasks
### 6.3 which visualization type to use?
- G1. Use Bar chart for finding clusters
- G2. Use Line chart for finding correlations
- G3. Use Scatterplot for finding anomalies
- G4. Avoid Line chart for tasks that require readers to precisely identify the value of a specific data point
- G5. Avoid using Tables and Pie charts for correlation tasks