---
시작일: 2024-10-10
진행상태: false
tags:
  - HCI
  - HealthInformatics
  - Ubiquitous
sticker: lucide//settings-2
---
- MoodCapture presents a novel approach that assesses depression based on images automatically captured from the front-facing camera of smartphones as people go about their daily lives
- We show that **a random forest** trained with face landmarks can classify samples as depressed or non-depressed and predict raw PHQ-8 scores effectively

# 1 Introduction
---
- It explains that the need for research on depression, given its serious impact worldwide. Smartphone can caputre uses' faces in real-time, as well as track daily smartphone usage, social media interactions, and more.
- Prior research utilizing facial images to detect depression focus on capturing these images in *controlled settings*
- It evaluates the performance of several machine learning and deep learning models for depression detection and PHQ-8 score prediction.

# 3 Methodology
---
### 3.3 Ground truth
- Data quality was ensured through validation techniques like reverse questions, and the filtered data reflected the complex variability of depression.
	- The data was filtered using methods such as 'Reverse Question Validation' and 'Handling Inconsistent Responses'

### 3.4 Image Characteristics
- They utilize BLIP visual question answering(VQA) model
	- **BLIP** : language-image pre-trained model. (for image explanation, image-based search)
	- **VQA** : generated answer model from image. (for context-aware system, contents explanation)
- The study analyzed images caputured by participants' front-facing cameras based on various attributes such as Lighting Conditions, Dominant Colors, Photo Location, Background Objects, Number of People in the Image, Image Angle.

# 4 Results
---
- The study evaluates the performance of several machine learning and deep learning models, including Random Forest and EfficientNet
- The RF model using **3D facial landmarks**, performed better in classifying depression
	- Key facial features included lips and face contours, with facial asymmetry being a critical predictive factor.
- The EffNet achieved a balanced accuracy of 0.61 in classification tasks, but the RF model outperformed it in terms of MCC
- The study also analyzed bias in model performance based on gender and race, finding that prediction performance was higher for white females(because their dataset predominantly consists of white females). →  <u><font color="#d83931">This was limitation</font></u>

# 5 ETHICAL CONSIDERATIONS AND USER ACCEPTANCE
---
This section likely covers important ethical issues related to privacy, data security, informed consent, and user acceptance of technologies like **MoodCapture**, which continuously collect personal images for depression detection.


# **Q**
1. The study predominantly used a dataset biased towards white females
2. the model has balanced performance, but low accuracy still exists 
3. This study havs different settings compared to prior studies. but it still focuses on indoor environments, not outdoor ones.