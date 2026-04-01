# Framing Generational Stereotypes on Reddit
## A Study of Interactional Reframing in Social Media Replies

**Author:** Iana Arefeva  
**Supervisor:** Prof. Manfred Stede (Applied Computational Linguistics, University of Potsdam)  
**Project Type:** Intermediate Module (IM) Cognitive Systems  

---

### 📌 Project Overview
This repository contains the data, code, and analysis for a sociolinguistic study on how generational stereotypes (Boomers, Gen X, Millennials, and Gen Z) are constructed and contested in digital discourse. By analyzing **1,568 validated claims** extracted from Reddit, this project maps the "linguistic packaging" of stereotypes and the sophisticated "reframing moves" users employ to defend their generational identity.

---

### 🔬 Theoretical Framework
The analysis is grounded in **Entman’s (1993) Framing Theory**, focusing on four specific functions:

* **Define Problems:** What is "wrong" with a specific generation?
* **Diagnose Causes:** Who or what is to blame for the problem?
* **Make Moral Evaluations:** How is the group judged?
* **Suggest Remedies:** How should the conflict be resolved?

---

### 🛠 Technical Pipeline: "LLM-as-Annotator"
To analyze the scale of Reddit data (4,199 raw pairs), this project utilized a **Human-in-the-Loop** pipeline:

1.  **Extraction:** Custom Python scripts using the Reddit API (PRAW) to collect parent-reply pairs from both general (e.g., `r/AskReddit`) and generation-specific subreddits.
2.  **Annotation:** Large-scale annotation using the **GPT-5.2 API**.
3.  **Reasoning-First Strategy:** The model was prompted to generate a "Reasoning Trace" (Problem, Cause, Moral Evaluation) before selecting final labels.
4.  **Parameter Tuning:** Utilized the "medium reasoning effort" setting to capture complex dialogic nuances.
5.  **Statistical Analysis:** Final hypothesis testing and data visualization conducted in Python (Pandas, SciPy, Seaborn).

---

### 📊 Key Findings

#### 1. The Reframing Paradox
The "packaging" of a claim determines its defensibility.
* **Generic Claims** (e.g., "Millennials are lazy") act as a **Systemic Shield**; they are reframed **51.7%** of the time as users shift the blame to economic or historical contexts.
* **Specific Anecdotes** (e.g., "A Millennial did X today") act as an **Evidence Trap**; they are reframed only **30.0%** of the time, as defenders are "trapped" by the specific facts of the event.

#### 2. Auto vs. Hetero-Stereotypes
Confirming the "In-group" hypothesis, the data shows that **Auto-stereotypes** (self-ascription) are significantly more nuanced and positive than **Hetero-stereotypes** (othering). Claims from an outsider perspective are over **50% negative**, while self-talk is predominantly neutral or positive.

#### 3. Linguistic Packaging (Nominalization)
The choice of label form is a predictor of toxicity. The use of bare nouns (e.g., "The Boomers") correlates strongly with negative valence, supporting the theory that **nominalization** facilitates the reification and "othering" of social groups.

#### 4. Gen X Invisibility
Despite equal search parameters, Gen X appeared as a target in **less than 1%** of validated claims, empirically confirming their status as the "Invisible Generation" in digital generational conflict.

---

### 📂 Repository Structure

```plaintext
├── data/                   # Samples of raw and annotated JSONL/CSV files
├── notebooks/              # Jupyter notebooks for extraction and analysis
├── visualizations/         # Heatmaps, Bar charts, and the Reframing Matrix
├── README.md               # Project overview and findings
└── requirements.txt        # Python dependencies (PRAW, Pandas, SciPy)
```

---

### 🚀 How to Use

1.  **Requirements:** `pip install -r requirements.txt`
2.  **Data Extraction:** Run `scripts/reddit_extractor.py` (Requires Reddit API credentials).
3.  **Analysis:** Explore the statistical proofs and visualizations in `notebooks/final_analysis.ipynb`.

---

*This project was completed as part of the Intermediate Module (IM) in Cognitive Systems at the University of Potsdam.*
