---
Author: Yasmeen Anjeer Alshehhi
진행상태: false
tags:
  - HCI
  - Visualization
  - mHealth
시작일: 2024-12-23
sticker: lucide//settings-2
Jounal: IEEE 2023
---
- This study investigates the needs and chellenges of mHealth app users with a focus on data visualisations.
- Bar and Pie charts were the most prefered forms for viewing health data. Users do not want to use complex chart.
- Users prefered a combination of text summaries and charts to make sure they correctly interpret the charts.
- Customisable and readable charts encouraged frequent app usage.

# 1 Introduction
---
- The market for mHealth tracking apps has grown significantly, with over 350,000 applications developed to assist users in mananging various health conditions.
- A ciritical features of successful and widely adopted health tracking apps is data visualisation. Current design practices acknowledge the importance of involving end-users in the initial stage of app design to ensure the development of effective mHealth apps that meet users needs, including data visualisation requirements.
- We found 18 data visualisations related to missing charts(based on data entries), chart interactivity(such as zooming to access more details), and chart layout and style. The poor quality of data visualisation resulted in a negative impact on the user experience and app rating.
- Therefore, our focus in this paper is on the UX and identifying the challenges and preferences of end users with respect to visualisation in mHealth apps.

# 2 Related Work
---
- Limited studies
	- A 2018 study([[Making Sense- An Innovative Data Visualization Application Utilized Via Mobile Platform]]) presented a prototype of a data visualisation app for health data using PhoneGap
		- 3 main concerns : colour usage, complex data visualisations, lack of ideal data visualisations.
	- Kim([[A Systematic Review on Visualizations for Self-GeneratedHealth Data for Daily Activities]]) highlighted the need to consider various aspects of data visualisation design, including selecting suitable data, determining effective visualisation type, and incorporating interactive feature to enhance user engagement.


# 3 Study Design
---
- the same as [[Needs and Challenges of Personal Data Visualisations in Mobile Health Apps User Survey]]

# 4 Survey Results
---
- 56 completed responses
### A. Participants Profile 
- The participants reported they used apps to track:
	- sports activity(26.79%)
	- heart rate monitoring(15.84%)
	- blood pressure(14.29%)
	- sleeping pattern(13.69%)
	- eating habits(12.5%)
##### RQ2 : Preferred data visualisation types.
- 75% of the respondents from all age groups preferred to represent their data using both text and charts, while only 19.64% of the respondents selected only charts.

### B. Users Needs
##### RQ3 : Data visualisation goals and tasks
- Interaction methods
	- read-only(32.14%), read and edit visualisation(26.79%), drill-down to show details edit visualisation(21.43%)
- Most common tasks 
	- finding the maximum and minimum(25.45%), showing the progess of activity and comparison(20.74%), 
- Chart functionality and styling options
	- controlling the chart and its presented data : Finding patterns, showing the history of previous data, editing chart titles

### C. Users's Pains and Gains
##### RQ4 : Issues and encouragement factors of mobile data visualisation
- top 5 challenges
	- Not showing the informations
	- Difficulty to drag points
	- Touch interface is not precise
	- Data displayed is too much
	- I cannot see a chart of my entries 
	![[스크린샷 2024-12-23 오후 6.05.22.png]]
- top 5 factors that affec tacceptance of data visualisation
	- Easy to read presented data
	- Data are complete and shown in the chart
	- Ability to set your own goal
	- Charts show progress
	- Easy to navigate
##### RQ5 : Suggestions to improve data visualisation
- we categorized into 5 key areas
- **Audiences**
	- Age-friendly data visualisation is one of the reported recommendations ( font size and colours)
- **Functional requirements**
	- They recommended adding a face scan to know the user's mood, comparing current and historical data, and the need for a daily dashboard in which users can personalise their presented data.
- **Data**
	- "I think one of the most important things is for charts not to be crowded"
	- "I need to be able to understand the 2 parameters being compared easily, descirbing data more understandably"
- **Interactivity**
	- "I would like to add high and low limit lines to the Y-axis on a graph so that any Y values above the high limit are easily seen as above or below those lines"

# 5 Survey Results
---
##### RQ1 Top mHealth apps
- The most frequently mentioned health apps : Apple Health, Sweatcoin, Samsung Health, Fitness App, and Step Tracker Pedometer.
##### RQ2 : Preferred data visualisation types and layouts
- Choe et al(26) stated that bar charts and line charts have also been shown as the most used charts among 21 other visualisation
- Katz et al(43) have stated that the pie chart scored high rates for being easy to read for participants.
- HOWEVER, the accuracy and readability of pie and doughnut charts have been criticised by (44), (45) and visualisation community (https://www.data-to-viz.com)
##### RQ3
- Users express interest in simple analysis, such as comparing their data and identifying trends, These findings suggest that simplicity is a key principle that users value, aligning with the concept of universal design(46)
- The correlation(between chart preference and their preferred tasks) highlights the importance of task relevance in influencing users' chart choices, emphasising the need for appropriate chart options that align with desired functionalities.
##### RQ4
- Our finding are align with (43). They found that users complained about the limitations of interactivity, inadequate data presentation, screen size limitations, and colour selection.
##### RQ5
- Participants stressed the importance of presenting data in a simplified manner within charts, considering themselves as non-expert users.

- In the industrial guidelines, The guidelines Google material design are comprehensive than the IBM design languages.
- However, These guidelines lack support for other components related to data visualisation, such as considering non-expert audiences, presented data, chart requirements, chart interactivity and alignment of presented chart design and functionality with the used mobile devices.