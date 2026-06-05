# Resume Screening and Candidate Ranking System

## Overview

This project develops a Machine Learning-based Resume Screening and Candidate Ranking System that automatically analyzes resumes, compares them with a job description, identifies relevant skills, calculates candidate-job fit scores, and ranks applicants accordingly.

The system helps recruiters and hiring managers quickly identify the most suitable candidates while reducing the time spent manually reviewing resumes.

---

## Problem Statement

Hiring teams often receive hundreds or thousands of resumes for a single job opening.

Manual screening presents several challenges:

* Time-consuming review process
* Inconsistent evaluation criteria
* Difficulty identifying qualified candidates quickly
* Risk of overlooking strong applicants
* Increased recruiter workload

To address these issues, organizations increasingly use AI and Machine Learning-based resume screening systems.

This project demonstrates a simplified Applicant Tracking System (ATS) that automates resume evaluation and ranking.

---

## Objectives

The system is designed to:

* Read resume data from a resume dataset
* Extract skills and relevant keywords
* Compare resumes with a job description
* Calculate candidate-job matching scores
* Rank candidates based on role fit
* Identify missing skills
* Generate recruiter-friendly insights

---

## Dataset

**File:** `Resume.csv`

### Dataset Features

| Column      | Description           |
| ----------- | --------------------- |
| ID          | Candidate Identifier  |
| Resume_str  | Resume text content   |
| Resume_html | Resume in HTML format |
| Category    | Resume job category   |

### Dataset Size

* 2484 resumes
* Multiple job categories
* Real-world resume content

---

## Project Workflow

### 1. Data Collection

Load resume data from the CSV dataset.

### 2. Data Cleaning

Preprocess resume text by:

* Converting text to lowercase
* Removing special characters
* Removing unnecessary spaces
* Preparing text for analysis

### 3. Skill Extraction

Identify technical and professional skills from resumes using a predefined skill database.

Example skills:

* Python
* SQL
* Machine Learning
* Pandas
* NumPy
* Git
* Tableau
* Power BI
* TensorFlow
* Deep Learning

### 4. Job Description Analysis

A job description is provided with required skills.

Example:

```text
Python Developer

Required Skills:
Python
Machine Learning
SQL
Pandas
NumPy
Scikit-Learn
Git
Data Analysis
```

### 5. Resume Matching

The system compares resume content against the job description using:

### TF-IDF Vectorization

Converts textual information into numerical feature vectors.

### Cosine Similarity

Measures how closely a resume matches the job description.

### 6. Candidate Ranking

Candidates are ranked according to their similarity score.

Higher score = Better match.

### 7. Skill Gap Identification

The system identifies:

* Matched skills
* Missing skills

This helps recruiters understand candidate strengths and weaknesses.

---

## Technologies Used

### Programming Language

* Python

### Libraries

* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Regular Expressions (re)

### Machine Learning Techniques

* TF-IDF Vectorization
* Cosine Similarity
* Text Mining
* Skill Matching

---

## System Architecture

```text
Resume Dataset
       ↓
Text Cleaning
       ↓
Skill Extraction
       ↓
TF-IDF Vectorization
       ↓
Cosine Similarity
       ↓
Match Score Calculation
       ↓
Candidate Ranking
       ↓
Skill Gap Analysis
```

---

## Visualizations

### Candidate Ranking Chart

Displays the top-ranked candidates based on match scores.

### Resume Category Distribution

Shows the distribution of resumes across job categories.

### Match Score Distribution

Displays overall candidate-job matching performance.

---

## Sample Output

### Job Description

```text
Python Developer
```

### Candidate Skills

```text
Python
SQL
Pandas
Git
```

### Match Score

```text
75%
```

### Missing Skills

```text
Machine Learning
NumPy
Scikit-Learn
```

---

## Example Ranked Candidates

| Rank | Candidate ID | Match Score |
| ---- | ------------ | ----------: |
| 1    | 105          |       92.4% |
| 2    | 287          |       89.8% |
| 3    | 452          |       87.6% |
| 4    | 910          |       84.3% |
| 5    | 1225         |       82.1% |

---

## Business Benefits

### Faster Hiring

Reduces manual resume screening time significantly.

### Improved Candidate Selection

Identifies the most relevant applicants automatically.

### Consistent Evaluation

Ensures all resumes are evaluated using the same criteria.

### Skill Gap Analysis

Highlights missing competencies before interviews.

### Reduced Recruiter Workload

Allows HR teams to focus on interviewing qualified candidates.

---

## Business Applications

### HR Technology Platforms

Automated resume screening.

### Recruitment Agencies

Candidate shortlisting and ranking.

### Corporate Hiring Teams

Large-scale hiring campaigns.

### Applicant Tracking Systems (ATS)

Resume filtering and recommendation.

---

## Model Evaluation

Candidate suitability is evaluated using:

### Cosine Similarity Score

Measures similarity between:

* Resume content
* Job description

Score Range:

```text
0 → No Match
100 → Perfect Match
```

---

## Output Files

The project generates:

### candidate_ranking.csv

Contains:

* Candidate ID
* Resume Category
* Match Score
* Matched Skills
* Missing Skills

---

## How to Run

### Install Dependencies

```bash
pip install pandas numpy matplotlib scikit-learn
```

### Run the Project

```bash
python resume_screening.py
```

### Generated Outputs

* Candidate Ranking Table
* Top Candidate Report
* Skill Gap Analysis
* Ranking Visualizations
* candidate_ranking.csv

---

## Future Enhancements

* PDF Resume Parsing
* spaCy-based Named Entity Recognition (NER)
* BERT-based Semantic Matching
* Advanced ATS Scoring
* Experience-Based Ranking
* Education Qualification Matching
* Real-Time Recruitment Dashboard
* Interview Recommendation Engine

---

## Conclusion

This project demonstrates how Machine Learning and Natural Language Processing can automate resume screening and candidate ranking. By extracting skills, comparing resumes with job descriptions, calculating similarity scores, and identifying skill gaps, the system enables faster, more consistent, and data-driven hiring decisions. It serves as a practical implementation of a simplified Applicant Tracking System (ATS) used by modern recruitment platforms and HR technology solutions.
