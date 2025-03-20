---
시작일: 2021-01-01
tags:
  - HCI
  - Visualization
  - mobile
sticker: emoji//1f393
Author: Dae hyun Kim
---
- Intergration of information from Text to Visualizations
- Identifying references between Visualizations and Text
- Transparency in natural Language interaces for Visualizations

# 1 Introduction
---
- Prior research shows that text accompanying visualization is effective in guiding people's attention towards certain portions of the visualizations and that it can improve both recall and comprehension of certain aspects of the underlying data.
	- barrier 1 : the cognitive effort required to see how their contets are related
	- barrier 2 : connection between the text and visulaization is often mismatched
	- recently, text has become imporant modality for data exploration. However the text and visualization are connnected is not transparent

# 2 Related Work
---
### 1 Reading & Authoring Visualizations and Text
- while some studies found significant improvements in comprehension of information presented in the text, others, did not
	- Gloud[57] : the text directs the reader's attention throught visualization though eye-tracking study
	- Xiong[182] : the text is visually important components before viewing charts
	- Borkin[19] : the text, such as chart title, helps people remember message in visualizations
	- Laungard[104] : the text descriptions of visualization are classified into a 4-level classification
> Chapter 3 is the address issues

- to build tools to help readers incorporate visualizations into their flow of reading
	- Tufte[165] : sparklines (word-sized visualizations embedded in the text to reduce the effort in traversing back and forth between text and visualizations)
	- Chang[25] : fluid documents (allow document elements to reorganized and change style to bring supporting information into the main text)
	- TIARA[102, 103, 173] : ties text analysis with interactive visual tools to make summaries of collections of text easier to understand
	- Victor[169] : Explorable Explanations (a reading interface that encourages active reading by interacting with the data presented in text and visualizations)
- Many researchers have studied how to automatically generate text caption and annotations, as well as automate reference extraction between text and visualizations.
	- Badam[11] : parse text and a data table and link information between them to dynamically generate visuals
> Chapter 4 is the address issues

### 2 Natural Language Interfaces for Visualizations
 - Researchers have studied how people would use language when interacting with visualizations and incorporated the finding into natural language interface systems
	 - Amar[5] : used a collection of questions about visualizations to break analytics activity while using a visualization tool into ten low-level tasks.
	 - Hearst[65], Setlur[147] : how an intelligent system should respond when given a guery including vague modifiers, such as 'high' or 'expensive'
 - Natural language interfaces that has recently gained considerable attention is quesion answering
	 - Kafle[76] : traditional question answering methods for photographic images do not generalize to charts and introduced DVQA (one of the first question answering systems for charts)
- With the advancement of AI, understanding why and how a system makes a decision is often diﬃcult to comprehend. this issue is related to transparency
> Chapter 5 is the address issues



# 3 How Readers Intergrate Charts and Captions
---
> Dae Hyun Kim, Vidya Setlur, and Maneesh Agrawala. 2021. Towards Understanding How Readers Integrate Charts and Captions: A Case Study with Line Charts. (CHI 21)
- In prior study, the charts with captions can improve both recall and comprehension of some aspects of the underlying information, compared to seeing the chart or the caption text alone
#### 2 main hypotheses
**H1**. When a caption emphasizes more visually prominent features of the chart, people are more likely to treat those feature as the takeaway
**H2**. When a caption contains external infromation for context, the information serves to further emphasize the feature described in the caption and reader are therefore more likely to treat that feature as the takeaway

### 2 Study
- Using [[Crowdsourced experiment]]to understand how captions describing features of varying prominence levels and the effect of including or not including external information for context, interacts with the chart in forming the reader's takeaways.
- 43 line chart (27 generated chart + 16 real-world chart)
- Using the Generated prominance curve, identify visually 3 prominent features
- Using template, generate caption with prominent feature
- filter Task + Insturction →  chart & caption display →  Takeaway collection

### 3 Result
##### Assessing H1 
- a feature in caption leads to more takeaways compared to having no caption, This shows that caption do play a role in forming takeaways and the takeaway is thus more likely to mention that feature
- [[5-point likert scale]].  the participants relied on the chart more than the caption
- The results further suggest that the participants’ tendency to rely on the charts grew while their tendency to rely on the captions declined as the prominence of the feature described in the caption decreased
##### Assessing H2
- people are significantly more likely to take away the feature described in the caption when it includes external information than when it does not

### 4 Design Guidelines
- *the several ways* for authors to emphasize aspects of the data in chart so that reader's attention is drawn to these visual features
	- to ensure that aspects of the data such as trends and outliers are presented at the right level of detail or interval range (do not too-broad of a mesurement interval)
	- to enhance visualization with highlighting and graphical overlays such as annotations to guide the audience's attention to the image area they are describing
		- Sometimes, a different chart altogether may be more effective to emphasize a particular aspect of the data


# 4 Linking Visualizations and Text
---
> Dae Hyun Kim, Enamul Hoque, Juho Kim, and Maneesh Agrawala. 2018. Facilitating Document Reading by Linking Text and Tables (UIST 18)
- Our interactive document reader **automatically** extracts such references for an input PDF document. Reader can click on a sentence to highlight the corresponding table cells and vice versa
	 -  It was designed to facilitate reading such documents and reduce split attention

#### Process
1. In the table structure extraction stage, It identifies the data type(text, number, percent) and cell type(title, header) of each table cell
2. It next matches sentence text to cells based on NLP techniques
3. Finally, It applies rule-base refinement of the matches based on the table structure

### 2 Automatic Reference Extraction
##### Stage 1: Extract Table Structure
- analyze the input table to extract low-level information about the spatial indices and spans, data types, cell type of each table cell, normalizing the values held in each cell to a standardlized format
- spatial indices and spans -  `<tr>`, `<td>` tags corresponding to each table row and column in HTML table. Then they generate row and column indices and spans
- data types - Money, Percent, Date, Time, Number, Text using Stanford Named Entity Recognizer(NER)
- cell type - Title cells, Header cells, Data cells
	- how to classify - there are two types of table
		- topmost row and leftmost column of this grid are headers at the finest level of granularity
		- some table do not contain row or column headers
- normalize cell values 

##### Stage 2: Match Sentence Text to Table Cells
- 4 different strategies using NLP
1. Matching text cells based on unique words
	- The strategy involves matching sentence words with unique words in table cells to identify references, but simple matching can lead to errors, so syntactic and semantic analyses are used for better accuracy.
2. Matching based on syntactic analysis
	- Syntactic analysis improves the matching algorithm by using phrase structure to identify multi-word phrases that uniquely match a single table cell, even when individual words do not.(with Stanford CoreNLP toolkit)
3. Matching based on semantic analysis
	- our syntactic matching strategy to compare each sub-phrase in the breadth-first traversal of the phrase tree using a distance based on word2vec
4. Handling cells containing numeric and time values
	- To match sentence text to cells containing numeric values, we first detect all strings in the sentence that represent numbers using the Stanford Named Entity Recognizer and convert them into numerals

##### Stage 3: Rule-based Refinement of Matches
- Stage 2 + consider table structure
- Add implicit data cells in the intersection of headers
- Remove data cells not in the intersection of headers
- Add implicit header cells if data cells match uniquely
- Remove potentially irrelevant header cells

### 3 Pipeline Evaluation
- Gold Reference Set - for the (sentence, table) pairs in the Pew and Academic data sets following the reference annotation guidelines of Kong[88]
- This result suggests that the performance of our pipeline is somewhat independent of writing style. (compared to the Kong, Pew, Academic dataset)

### 4 Interactive Document Reader
- Clicking on such a sentence highlights it and the table cells it refers to in yellow. Similarly, clicking on a cell highlights all the sentences that refer to it.

### 5 User study
**H1**. our interactive document reader will help users locate table cells relevant to sentences in the text more accurately and quickly than the baseline reader
**H2**. FP errors cause more harm(lower speed and accuracy) than FN errors
- 24 trials, 12 in each condition, [[5-point likert scale]], to express their opinions about the usefulness of the interface in a free-form text response.
- We find that our interactive reading interface significantly outperforms the baseline interface **in terms of accuracy and speed**  (H1)
- We also find that presenting a reference containing FP errors in our interface harms accuracy and speed much more than presenting a reference containing only FN errors (H2)


# 5 Visual Explanations for Chart Question Answering
---
> Dae Hyun Kim, Enamul Hoque, and Maneesh Agrawala. 2020. Answering Questions about Charts and Generating Visual Explanations. (CHI 20)

[[Answering Questions about Charts and Generating Visual Explanations]]


# 6 Limitation and Future Work
---
### 1 Generalization of Findings and Algorithms
- Future work could study captions with various natural language expressions and diﬀerent ways of emphasis. (this paper used template-based approach)  in Chapter 3
- reference extraction need to support many types of visualizations other than some basic chart types  in  Chapter 4
### 2 Implementation and Improvements of Algorithm
- In Chapter 4, we verified that readers are better oﬀ with our interactive document reader although the accuracy was only 48.8%.
- Our question answering system in Chapter 5 achieves an accuracy of 51% and can be improved further