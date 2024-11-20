---
시작일: 2024-11-01
진행상태: false
tags:
  - HCI
  - Visualization
  - Responsive-Visualization
sticker: lucide//settings-2
---
![[Dupo - A Mixed-Initiative Authoring Tool for Responsive Visualization.png|500]]

- Users can adopt Dupo at streamline the development of responsive visualizations, exploraing automated and manual customization for designs across screen sizes
- **Dupo** successfully combines manual customization with automated suggestions to create a user-guided, iterative visualization design experience. It supports designers in quickly prototyping responsive layouts and preserving critical design elements across platforms

# 1 Introduction
---
- Consequently, some recent work proposes automated approaches to responsive design or visualization retargeting[[MobileVisFixer - Tailoring Web Visualizations for Mobile Phones Leveraging an Explainable Reinforcement Learning Framework]]
- They designed and implemented Dupo, a mixed-initiative authoring tool. 
- Dupo implements a two-step design recommandation pipline(Exploration and Alteration) 
	- `Exploration` : changes to the layout, encoding choices, data transoformation
	- `Alteration` : more subtle changes to axis labes, legend position

# 2 Related Work
---
### 1 Responsive Visualization Authoring
- Prior work identifies programmatic difficulties, artboard management, design exploration, and changes to takeaways as some of the major challenges in adapting visualizations for different screens
- Computational (semi-) automation is often recommended
- When exploring automated design alternavtives, authors still need to reason about how effectively the responsive versions maintain high level design goals such as intended as takeaways for viewers
- Kim ([[An Automated Approach to Reasoning About Task-Oriented Insights in Responsive Visualization]]) propose a set of measures that approximates changes to visualization insights between responsive versions in terms of data indeifiability, comparison discriminability, and trend recognition

# 3 Usage Scenarios
---
#### Desktop-first, novice author (Riley)
- Riley, a novice in responsive design, begins with a desktop visualization of a line chart showing oil price changes. (A1)
- Uses a mixed-initiative tool to explore mobile-friendly versions. (A2)
- Notices some suggestions violate organizational guidelines (e.g., no temporal fields on vertical axes) and marks them as "undesired."
- Selects two versions for team discussion: a reduced-width layout and a heatmap.
- Adjusts overlapping annotations for better readability. (A3)
- Accepts the tool’s suggestion to add a tick mark for clarity.
#### Simultaneous editing, experienced author (Frankie)
- Frankie, an experienced visualization designer, prefers creating responsive designs across multiple artboards (desktop, tablet, mobile) simultaneously.
- Begins with a horizontal bar chart on greenhouse gas emissions by country.
- Finds the desktop version too wide and retrieves design recommendations to optimize space usage.
- Chooses a one-dimensional dot plot that uses the horizontal space effectively without altering the core message.
- Highlights two countries by changing their colors for emphasis; this change propagates to tablet and mobile versions.

# 4 Design Considerations
---
- Support Design Exploration(DC1) - Users effectively explorate many different options and avoid design fixation
- Support User Control(DC2) - Users should be able to fine-tune the recommandation methods
- Support Progressive Authoring(DC3) - Users should be able to search easily as needed
- Support Flexible Artboard Management(DC4) - Users may have different preference in creating responsive visulizations

# 5 Recommandation Pipeline
---
### 1 Exploration: High-level Transformations
#### 1 Input
- The Exploration pipelines takes a source design and a set of user constrains as input
##### 1a. Source Design
- If the source design is a pie chart, the transformation strategies for a bar chart are omitted from the search space unless there is a change to the mark type
- Dupo uses the source design to determine inapplicable transformations while maintaining the underlying data characteristics (e.g., data type), aesthetic choices (e.g., encoding scales), and text contents.
##### 1b. User Constraints
1. responsive locks - provide explicit preferences about what elements cannot be updated
2. hidden recommandations - provide implicit feedback about what transformations are undersirable
3. recommander parameters - provide abstract feedback on the outputs and weights applied by the recommender
#### 2 Search space generation
- These suggestions are translated into Cicero [[Cicero - A Declarative Grammar for Responsive Visualization|Cicero: A Declarative Grammar for Responsive Visualization]]specifications so that the Cicero compiler can convert the design accordingly.
- These pre-defined techniques include high-level transformation rules for mark type, layout (rows and columns; small multiples), data transformations (e.g., filtering or aggregation), and encoding channels
- While Dupo suggests further Exploration suggestions, it only suggests those default transformations for tablets in a desktop-first direction unless requested by the user.
#### 3 Ranking measures
-  Dupo evaluates them using several ranking measures in comparison with their source design in terms of “message” and density
### 2 Alteration: Low-level Transformations
- For example, Alteration from phone to desktop suggests adding labels for a quantitative axis, internalizing a short title, and adding a tooltip.
### 3 Augmentation: Next-step Transformations
- Dupo supports a variety of **quick edits** including adding or removing tick lines after repositioning annotations and moving the title text into the chart area when it is added for desktop or tablet versions,

# 6 Dupo User Interface
---
- Dupo supports designing communicative visualizations with common visualencodings, annotations, and interactivity (including zoom+pan, tooltips,a brush-based context view, and an interactive legend for selecting marks on hover).

- Implementation Details
	- Each **Cicero** rule is composed of a specifier (what to change; e.g., axis, layout), action (type of change; e.g., add, modify), and option (how to change; e.g., font size, marktype). with Vega-Lite

# 7 User Study
---
- **RQ1**: Dupo에서 저자가 대안 디자인 아이디어를 얼마나 잘 탐색할 수 있는가?
- **RQ2**: 저자들이 수동 편집과 자동화된 디자인 제안을 어떻게 결합하는가?
- **RQ3**: 액션 위젯과 상호작용할 때 Dupo의 추천기 제어 옵션을 어떻게 사용하는가?
또한, Dupo의 일반적 실행 가능성과 유용성에 대한 질문을 다루었습니다
- **RQ4**: Dupo의 디자인 제안과 최종 결과가 저자들에게 합리적으로 평가되는가?
- **RQ5**: 저자들이 Dupo를 일상적인 반응형 시각화 작업에 사용할 만한 도구로 여기는가?
- **RQ6**: Dupo의 유용성을 개선하기 위해 해결해야 할 과제는 무엇인가?

## Idea
- It only provided only desktop-first approach만 고려
- 이 논문의 Userstudy 참가자는 graphics reporters로 모두 데이터 리터러시가 풍부한 참가자들이었다.