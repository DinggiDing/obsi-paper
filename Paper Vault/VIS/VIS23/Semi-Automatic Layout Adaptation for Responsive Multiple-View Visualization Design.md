---
시작일: 2024-10-10
진행상태: false
tags:
  - HCI
  - Visualization
  - LayoutAdaptation
sticker: lucide//settings-2
---
- AdaMV algorithm, based on simulated annealing, automates and optimizes multi-view visualizations

# 1 Introduction
---
- Existing guidelines for visualization design remain primarily tailored for the desktop, which do not transfer well to small displays such as mobile phones and tablets.
- **The AdaMV Algorithm** uses **simulated annealing** to optimize the layout of multiple views, automatically selecting the best layout.
- Differentiation from Existing Research: Unlike previous research, this work focuses on **multiple-view visualizations** rather than single charts.

# 2 Related Work
---
#### Responsive Visualization
- Prior studies enrich the nuanced understanding of visualization design on small displays, yet most of them focus on specific data types (e.g., range data [11]), chart types (e.g., bar, donut, and radial bar charts [10]), or application contexts (e.g., public transit [32]).
- Prior studies focus a single chart. So This Study contribute an automatic layout adaptation technique based on the geometric and authoring system that allows propagating design edits of MV visualization across different screen sizes.
#### Computational UI Retargeting
- There are two approaces to achieve computational UI Retargeting
	- Model-based : templates or optimization algorithms(simulated annealing, greedy heuristics)
	- Data-Driven : automatically transform desktop-customized UIs as examples of good designs.
- **Goal** :  formulating a series of retargeting heuristics from design patterns of the input MV visualization and output display, and adopting *a simulated annealing* method to produce optimal MV layouts on the target display.

# 3 Overview
---
### 1. Research Focus
- Responsive MV visualization needs to consider layout, visual mapping, underlying data and interaction
### 2. Requirements and Considerations
- **Hard constraints**
	- Keep all views - In a small target viewport, considering extra viewports using page flipping or tabs.
	- Avoid overlap - affecting the data interpretability
- **Soft constraints**
	- Avoid unnecessary extra viewports
	- Minimize white space
	- Maintain aspect ratios and relative sizes in target layouts
	- Preserve view topology
	- Improve view readability
### 3. Method Formalization and Overview
- 2 Framework
	- Layout Retargeting (to fulfills the requirements R1, R2, C1-C4)
		- The AdaMV algorithm(based on simulated annealing) organizes view into a hierarchical tree structure and searches for the best layout by minimizing a cost fuction
	- View Tailoring
		- This stage focuses on fine-tuning individual view to improve readability
		- This algorithm detects issues like out of viewport, unreadable labels, and cluttered text, and adjusts the encodings accordingly by adjusting the visualization specifications


# 4 MV Layout Adaptation
---
- 아이디어만 봄. 
- 이 부분부터는 디테일하고 수식적