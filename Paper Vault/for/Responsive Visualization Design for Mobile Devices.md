---
sticker: emoji//1f4da
---
- In Chapter 2.

- They used the term *responsive* to describe aspects of visualization that adapt automatically to various factors, such as changed device characteristics, environment, usage context, data or user requirements.

## 2.1 Context

- Mobile phone has different aspect ratio compared to tablet or PC or Smartwatch
- Wu[100] found that over 73% of Web-based visualization faced at least one issue when being displayed on mobile devices.

## 2.2 Responsive Design vs Responsive Visualization Design
- 단순 이미지와 다른 점은 Interactivity 가능한 것.

## 2.3 Factors 
- Device Factors, Usage Factors, Environmental-Factors, Data Factors, Human Factors

### Device Factors
- Display size
- interaction modalities 
	- touch gesture, pressure-sensitive touch
	- hardware button
	- spatial interaction(tilting recognized through built-in sensors)
	- speech input
### Usage Factors
- by how and in which posture a person in using the device
- one-handed, two-handed
### Enviromental Factors
- Indoor / Outdoor environments
### Data Factors
- visualization of many data points as individual marks can lead to rendering performance issues and a lagging interface on a mobile device.
- selecting marks can also become challenging due to the reduced precision with touch input or when marks are overlapping
- many datasets →  longer loading times, performance issues, inaccurate touch input
### Human Factors
- Levels of visualization literacy, subject matter knowledge, attention span, and motivation varytremendously between people

- WiFi signal →  the signal infered that users were indoors

## 2.4 Responsive Visualization Design Strategies

### Scale
- changing the layout or aspect ratio of content
- zoom and pan the content
### Aspect Ratio
### Layout
- visualization may be accompanied by text, control panel, images, or additional visualization elements.
### Level of Detail
- convert one chart into several charts by faceting on a demension of the data.
- Aggregation, Reclassification
### Amount of Data
- the entire visualization is visible from a desktop while a sampling of cropped areas of interest are visible from a mobile display.
### Annotation & Guides
- annotation and guides are often re-positioned, simplified, or removed altogether
### Attentional Cues / Dynamic Guides
- a mobile experience might augment a cropped, zoomed-in version of the chart with a minimap view of the entire chart: a form of focus + context or overview + detail.
### Animation / Streaming Data
- animation did not work on  both desktop and mobile devices 
- animation can be distracting and engaging or memorable
### Visual Encoding
- mobile-first design approach may lead designers to more responsive designs relative to a desktop-first approach
- consistent primary mapping + secondary mapping that varies depending on device. ( by Radloff )
<font color="#ff0000">- Q. Bremer, Camoes 는 어떻게 모바일 디스플레이에 최적화된 형태라고 생각했는가?</font>
- Semantic Zooming
- morph from a line plot to a horizon chart when the height of the graph falls below a certain threshold
- focus + context : matrix visualization →  scaled up to embedded chart
- Table (not a chart)
### Interaction
- There is the question of whether interaction in necessary.
- while interaction remains to be a topic of debate within the visualization practitioner community, entirely scroll-based interaction remains to be a populara design choice across devices.
- In non-communicative or explatory visualization contexts, Interaction is often essential to the analytical process, and thus it is necessary to rely upon discoverable interactions that allow similar levels of exploratory behavior across platforms.

## 2.5 Challenges & Opportunities
### 1 Develop Once, Deploy to Many
- to decrease cost and effort
- Existing Visualization design models such as the nested model, the visualization design triangle, or the five design sheets method do not explicitly consider the aspect of responsiveness
### 3 Evaluation
- It does not neccesarily require large human factors studies. 
- It seems to be viable to evaluate using a set of evidence-based heuristics and guidelines.