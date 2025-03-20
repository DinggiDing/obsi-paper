---
Author: Ben Philip
진행상태: false
tags:
  - HCI
  - DataCollection
  - mHealth
시작일: 2025-01-08
sticker: lucide//settings-2
Jounal: JMIR Mhealth Uhealth 2022
---
- This study aim to analyze what data mHealth apps across different categories usually collect from end users and how these data are collected.
- We downloaded apps that fulfiled our criteria from a mirror site hosting Android apps and analyzed them using a script that we developed around the popular AndroGuard tool.
- We found that not many health apps used built-in sensors or peripherals for collecting health data.

# 1 Introduction
---
- These mobile apps collect or generate health insights from 3 sources:
	  1. external devices(Bluetooth or WiFi-based sensors)
	  2. built-in smartphone sensors
	  3. manual data entry
- mHealth apps have been classified either as active or passive
	- the former generate or derive health data using sensors
	- the latter rely on manual user input
#### Built-in Sensors
- cameras were the most frequently used sensors where they were used for assessing one's heart rate and ever for automated skin cancer diagnosis

# 2 Methods
---
-  Identify mHealth app categories →  List apps in identified categories →  Download apps meeting inclusion criteria →  Extract Bluetooth service UUIDs / Identify internal sensors and hardware use(Android manifest)
#### Identifying and Collecting mHealth Apps
- We investigated the use of built-in sensors such as accelerometers, gyroscopes, GPS modules, and even the smartphone's cameer module in the identified apps.
- By analyzing app permissions, It is possible to infer to some extent what feature this app provide and how data are gathered.
#### Data Extraction From mHealth Apps
- **Extracting UUIDs from packages** - AndroGuard helped us the set of permissions and hardware features requested by apps, Bluetooth permissions.
- **The Use of Internal sensors** - AndroGuard was used to identify built-in sensors accessed by mHealth apps through the declared permissions.

# 3 Results
---
#### The use of Internal sensors
- We analyzed the set of 3251 apps.
- the camera being more popular across most search categories with GPS following closely, with the highest use seen in the Staying Healthy category.
#### The use of Bluetooth Peripherals
- not many standard health-related services were identified, and we note that only the Heart-rate measurement(1.26%) and the Heart-rate service(1.23%) UUIDs were found in the top 10 

# 4 Dicussion
---
#### Data collection
- Our findings indicate that although there is increasing use of smart wearable and the increasing popularity of peripherals, not many apps use them to collect health data. 
- Also, not many apps were found to use built-in smartphone sensors.
- Our results are consistent with a recent study by Wisniewski et al(27), where most apps relied on manual entry with limited support for any wearables.
- Our results show 20.57% and 18.39% of the apps used the camera and GPS modules.
- most devices and apps used proprietary algorithms, limiting their compatibility and use.
#### Data sharing
- A platform integrating a diverse set of apps, health records, and sensors could improve this aspect of mHealth apps with functionality and usability blending in seamlessly, potentially improving health outcomes.
#### Tools and Data Set
- Although usability is subjective, limited support for passive data collection with internal and external sensors can have a negative impact on app experience.

- To that end, we envision a connected ecosystem of mini health apps, sensors, and health records as a key mHealth technology of the future.
- We plan to use these results to develop a single mHealth platform for aggregating several wearables and health apps as mini health services.

# 5 Conclusion
---
- Given that user studies on app experience have highlighted convenience and data interconnectivity and aggregation as important factors, automating data collection can improve UX, expecially in apps requiring access to health metrics.
- Our analysis of 3251 apps indicates that 10.74% of the apps use smart devices and wearable devices to gather health metrics from users. very few apps used standard health-related Bluetooth services.
- a significant number of apps requiring manual data entry were found in our set, highlighting the need to focus more on developing mHealth apps that automate health data collection.


##### Discussion
- 초반에는 Choe 2017, Semi-automated tracking에 반대되는 입장이라고 이해했지만, 추후 manual entry의 적정 균형을 찾는 것이 핵심인 동일한 입장이라고 이해되었다. 즉, 이 논문에서는 manual entry를 최소화해야한다라고 얘기하고 있다.