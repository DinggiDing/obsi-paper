---
시작일: 2024-10-16
진행상태: false
tags:
  - HCI
  - Visualization
sticker: lucide//settings-2
---
- **EmphasisChecker** An interactive tool that highlights visually prominent chart featrues as well as the features emphasized by the caption text along with any mismatches in the emphasis (<font color="#245bdb">Interactive tool for analyzing and aligning chart-caption emphasis</font>)
- Misalignment between chart and caption emphasis reduces communication effectiveness
- It uses the *Ramer-Douglas-Peucher* algorithm, *BERT* embeddings and *Stanford CoreNLP* tool

# 1 Introduction
---
- When the chart and caption text emphasize the same aspects of the data, people tend to remember those aspects of the data as takeaways
	- Professional authors match chart and caption emphasis about 65% of the time and mismatches in the remaining 35%
	- In Non-professional authors, These mismatches are even more common
- They focus on *time-series line charts* as a first step
###### Algorithm
- **the prominent feature detector** - a new ε-persistence technique based on the Ramer-Douglas-Peuckerline simplification algorithm for approximating visual prominence
- **the chart-text reference extractor** - heuristics based on exapme analysis + modules within the Stanford CoreNLP toolkit + BERT embeddings <font color="#7f7f7f">(to find time references and data descriptions in the caption text and matches them with chart data)</font>

# 3 A Survey of Line Chart in the wild
---
- They found that 65% chart-caption pairs made by professional authors match emphases
- Mismatched captions often either emphasize non-prominent features or provide only basic descriptions without highlighting specific elements(93%)

# 4 Usage Scenario
---
1. Viewing visually prominent features in the chart as orange circles( 🟠) and bars (🟧) just above the chart
2. Typing a basic caption - no prominent feature
	 "the chart shows the real home price index between 1890 and 2006"
 3. Typing caption text that matches the most prominent visual feature
	 - *When Users update the caption*, this tool highlights the phrase in blue and displays <font color="#0070c0">a blue circle</font> on the year mentioned in phrase, and <font color="#0070c0">a blue bar </font>starting in the year to show references between the chart and caption
	 - This tool highlights the matching prominent feature in <font color="#00b050">green</font>, indicating that the caption and chart are now aligned
4. Typing caption text with an error
	- When Users typing wrong sentences, this tool highlights <font color="#ff0000">a red squiggly underline</font> in the caption text, indicating a factual inconsistency
5. Pushing through with caption text about a less prominent feature
	- The tool shows<font color="#00b0f0"> a blue squiggly underline</font> to indicate that the referenced trend is not a top five prominent feature but allows useres to proceed.


# 5 Components of EmphasisChecker
---
- This tools interfaces allows the user to edit both the chart and caption
	- The user can write captions and edit the dimensions and the x- and y-axis ranges
### 1 Time-Series Prominent Feature Detector
- Detect visually prominent featcure in time-series line chart
- Based on the strength of the <span style="background:rgba(240, 200, 0, 0.2)">Ramer-Douglas-Peuker(RDP) line simplification algorithm</span> in <span style="background:rgba(240, 200, 0, 0.2)">enhancing important extrema</span> in time series, they modify the RDP algorithm to compute ε-persistence for measuring visual prominence of both point and trend(추세) features.
- This tool displays the top five most prominent features above the chart in order, the most prominent closest to the chart, using circles to depict point features and bars to depict trend features.
### 2 Text References Extractor
1. Extract time references in caption text
	- Uses the *Stanford CoreNLP toolkit* to detect time expressions like "1981", "between 1990 and 2000"
	- To detect start and end point, they utilize the context template patterns near the time words like "since T", "previous to T" 
2. Extract data description in caption text
	- Extract trend description and local extrema in the caption text by looking for a predefined set of keywords
	- To capture any synonyms that we may have missed in our list, we use the cosine similarity of the *BERT contextual embedding vectors* between the words in the input sentence and the words in the keywords list.
3. Pairing time references with data desciptions
	- Obtain a dependency tree for the caption using Stanford CoreNLP dependency parser
4. Match text references with chart data
	- Get Disambiguation using multiple words
5. Match referenced feature with prominent featrues
	- Get the top 5 most prominent features


# 6 Results and Evaluation
---
- High Usability
- Improved alignment
- Errors detected

##### Limitation
- Only time-series line chart
- Bias toward visual features
- Limited Context Awareness