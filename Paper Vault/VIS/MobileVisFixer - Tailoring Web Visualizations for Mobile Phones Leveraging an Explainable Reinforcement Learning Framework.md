---
시작일: 2024-10-28
진행상태: false
tags:
  - HCI
  - Visualization
  - mobile
  - VisualizationDashboard
sticker: emoji//1f469-200d-1f3eb
---
![[MobileVisFixer.png]]

- MobileVisFixer identifies and resolves four common mobile-visualization issues (viewport overflow, font size, text clutter, and unwanted white space) using reinforcement learning. Its explainable framework aids users in understanding adjustments while preserving the integrity of visual data representation.

- It uses an explainable reinforcement learning framework to modify SVG visualizations, targeting specific issues such as text size, layout distortion, and element overlap to address mobile-friendly visualization issues
- The main challenges include handling readability, adapting layout within viewport constraints, and preserving visual encoding on mobile screens.

# 1 Introduction
---
- the mobile friendless text tools mentioned eariler do not properly handle SVG-based visualizations
- Existing automated solutions usually adjust visualizations by rule-based methods. But It face challenges such as large manual efforts and the combinatorial explosion of possible condition
- We focus on SVG-based, single-view Cartesian visualizations with linear or discrete scales, which are found common on the web

# 3 Mobile-Friendly Issues in Web Visualizations
---
- We note that we focus on layout-related readability issues of SVG-based visualization and do not consider interaction problems
#### 1 Mobile-friendly issues
1. Out of the viewport
2. Unreadable font size
3. Cluttered text
4. Distorted layout
5. Unwanted white space
- We found that 142 (37.9%) visualizations exhibited no changes between desktop and mobile designs, while only 98 (26.2%) visualizations exhibited none of the above five issue