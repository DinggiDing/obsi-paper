---
Author: Yoojung Kim, Bongshin Lee, Eunkyung Choe
진행상태: false
tags:
  - HCI
  - Personal-Informatics
  - HealthInformatics
  - mHealth
  - Self-Tracking
시작일: 2025-01-20
sticker: lucide//settings-2
Jounal: JAMIA 2019
---
- [ ] to unveil the current state of the data accessibility - the degree to which people can access their data - of personal health apps
- 240 apps →  45 apps (criteria)
- Personal data should be accessible to the people who collect them, but existing methods lack sufficient support for people in accessing the fine-grained data.

# 1 Introduction
---
- Exist.io, Gyrosco.pe are to integrate multiple data source in a new service.
- some companies do not provide the data at all, and people have not pay an extra charge to access their data.
- In this work, we bring the notion of data accessibility - a common used term to denote the degree to which data can be accessed by an agent - in the personal health data context.

### Background
- one of the essential issues around PHRs(Personal Health Records) is to define what and how many data should be shared with patients.
- People's data are scattered across many databases in a silo.

# 2 Materials and Methods
---
- Data Accessibility - Data access method and Data types
- Data access method refers to how individuals with a varying level of technical skills and diverse purposes can access their self-tracking data.
- Data types referes to a target of the measure, such as step, heart rate, weight and sleep.
- A combinations of data access methods and data types determines the granularity, which we define as the minimum time interval of the accessible data.
	- measuring weight does not need to be doen every day.but capturing blood presure is benifical when done continuously.

- Data access method
	1. APIs
	2. health platform connection
	3. file download
		- CSV, FIT, GPX, KML, TCX file format.

# 3 Result
---
- Data can be accessed through 3 types of data access methods
	- health platform (36)
	- file download (22)
	- API (15)
- All (8), two methods (16), only one method (17)

- Data types (23 types)
	- Daily Activity
		- Step Count, Calories Burned, Distance, Flights Climbed, Activity Level, Elevation, Resting Energy, Walking Time, Brushing, Stress
	- Workout
		- Workout Session, Route
	- Sleep
		- Sleep Analysis
	- Body mesurement
		- Weight, Body Fat, Body Mass Index, Body Mass, Oxygen Saturation, Respiratory Rate, Body Temperature
	- Cardiac measurement
		- Heart Rate, Blood Pressure, Pulse Wave Velocity

### Data granularity
- Overall APIs provide fine-grained data access than health platform and file downloads
- APIs <= Health platform < File Downloads

# 4 Dicusssion
---
### Towards better data accessibility
- We interpret data accessibility as a way to utilize their data better to meet their goals.
- Although Apple Health supports health data intergration, it does not provide rich insights from multiple data sources.
### Data schema standards
- In our analyses, we learned that no clear standards exist in personal health data schema, resulting in data loss when transferring data between services.