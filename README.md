# HEProAI: AI and ML Internship
## Activity: 01 - Dataset Design & Student Profiling

### 1. Project Overview:
   
This repository contains the foundational dataset and profiling documentation for the Dedicated Mentoring System. The primary objective of this activity is to design and generate a multi-dimensional student dataset that represents various academic, wellness and career dimensions.

### 2. Repository Contents:
1. students.csv: The primary synthetic dataset.

2. data_generation.py: The Python logic used for data creation and pattern injection.

3. Data Dictionary & Behavioral Analysis.pdf: Comprehensive data dictionary and behavioral analysis report.

## Activity: 02 — Student Scoring System

### 1. Project Overview:
In this phase, I developed the Scoring & Classification Layer for the system. This module processes multi-dimensional feature vectors to calculate standardized performance scores and a holistic Student Readiness Index (SRI).The system enables proactive mentoring by automatically flagging students based on their academic, wellness and career readiness states. 

### 2. Repository Contents:
1. student_scoring.py: Python script containing normalization and scoring logic.
   
2. student_scores.csv: The updated dataset with calculated scores and categories.
   
3. Scoring_Logic_and_Thresholds_Explanation.pdf: Technical report detailing formulas and validation.


## Activity 3: Machine Learning - Student Segmentation & Risk Detection

### 1. Project Overview
In this phase, I shifted from rule-based scoring to **Unsupervised Machine Learning**. Using the K-Means clustering algorithm, I segmented the student population into four distinct behavioral groups. This allows the system to detect "hidden" risk patterns such as students with high grades but dangerously low wellness scores that traditional threshold based systems might overlook.

### 2. Key Machine Learning Tasks:
* **Data Preprocessing:** Standardizing features (APS, WWS, PTMS, CRS) to ensure distance-based clustering accuracy.
* **K-Means Clustering:** Iterative grouping of students into 4 clusters based on multi-dimensional similarity.
* **Segment Analysis:** Mapping clusters to specific personas like "Burnout Risk" and "High Performer."

### 3. Repository Contents:
* `student_segmentation.ipynb`: The notebook containing the ML pipeline and visualization.
* `Cluster_Interpretation.pdf`: Detailed analysis of the 4 detected student groups.
* `Recommendations for Each Cluster Type.pdf`: Targeted intervention strategies for each cluster.

## Activity 4: Mentor Matching & Intervention Recommendations

###  Objective
The final phase of the HEPro AI+ project focuses on **Operationalizing AI Insights**. The goal is to translate the patterns discovered by the K-Means clustering algorithm into a functional human-centric support system by automatically matching students with specialized mentors.

###  Key Features
* **Automated Mentor Dataset Creation**: A dynamic Python script that generates a database of mentors with specific specializations (Academic, Wellness, Career) and tracks their current workload capacity.
* **Intelligent Matching Logic**: 
    * Identifies the student's primary area of need based on their ML Cluster assignment.
    * Matches students with mentors based on **Expertise Alignment**.
    * Implements **Load Balancing** to ensure mentors are assigned based on availability, preventing burnout.
* **Proactive Alert System**: High-risk students (Cluster 1: Burnout and Cluster 2: At-Risk) are automatically flagged with ` CRITICAL` alerts to ensure mentors prioritize their intervention.

###  Activity 4 Repository Structure
| File | Description |
| :--- | :--- |
| `mentor_matching.py` | The main engine that creates the mentor database and executes the matching logic. |
| `mentors.csv` | The generated database of mentor profiles and capacity tracking. |
| `final_recommendations.csv` | The output table mapping all 60 students to specific mentors and intervention playbooks. |
| `Final_Recommendation_Table.pdf` | A formal report summarizing the assignment matrix and priority levels. |
| `End_to_End_Flow_Explanation.pdf` | A technical document explaining the internal logic of the matching pipeline. |


