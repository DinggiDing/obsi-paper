---
시작일: 2024-12-02
진행상태: false
tags:
  - HCI
  - Self-Tracking
  - mHealth
  - Personal-Informatics
sticker: lucide//settings-2
---
- In this study on sleep tracking, we examine ways to reduce the capture burden of manual tracking while leveraging its benefit
- the widgets improved information access and encouraged self-reflection


# 1 Introduction
---
- our goal wwas to enhance the manual tracking method by designing a tool that supports in easily capturing and reflecting on multiple behavioral factors.
- We used Android's lock screen and home screen widgets to reduce the capture burden and improve access to information.
- We found that participants who used SleepTight with the widgets enabled had a higher sleep diary compliance rate than participants who used SleepTight without the widgets.

# 3 Sleeptight
---
- G1 : enable people to capture both target behaviors and contributing factors that are likely to influence the target behaviors
- G2 : to reduce the capture burden and create a consistent capturing habit
- G3 : to provide feedback to promote self-reflection

### Sleeptight Design
- Full system (lock screen widget, home screen widget, app)  /  App-only system (no widget)

##### Leveraging App Widgets
- Ex) Tapping on the caffeinated drink icon from the lock screen widget captures the time stamp of clicking the caffeinated icon.
- the widget provides easy access to the full App.
	- Ex) tapping on the timeline region invokes the Add Activity tab.
- the widget serve as a glanceable display

##### Providing Feedback about People's Sleep Behaviors
- **Sleep Summary Tab**
	- solid rectangel represents the actual sleep duration and its color represents sleep quality.
	- pink-hashed lines could indicate sleep problems such as insommia.
- **Comparison Tab**
	- within-subjects comparison, which is one of most popular data exploration techniques among self-trackers

# 4 Deployment Study
---
### Study Design
- We designed a between-subjects study to evaluate the effects of widgets by comparing the two versions of the SleepTight system.
- We used the t-test and Mann-Whitney U test to analyze both the tracking logs and usage logs to compare the overall usage between the Full-system and App-only system conditions

# 5 Result
---
### Data Capture Behavior
- FS Adherence rate > AS Adherence rate
- Most of participants(77%) was accessed from Home screen widget
- FS time < AS time
- FS participants said that the widget served as a visual reminder to capture the sleep diary and other daytime activities.
### Information Access
- FS Participants viewed the summary page more frequently than those in the AS condition
### Self-reflection with SleepTight
- The majority of self-reflection descriptions were about findings on participants’ sleep patterns.
- They were also able to compare within themselves the differences and similarities across weekends and weekdays and identify the ways in which the previous night’s sleep affects the following night’s sleep.
- But, in general, most of self-reflection descriptions contained vague associations between sleep and other factors