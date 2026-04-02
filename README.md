# Framing Generational Stereotypes on Reddit
## A Study of Interactional Reframing in Social Media Replies

**Author:** Iana Arefeva  
**Supervisor:** Prof. Manfred Stede (Applied Computational Linguistics, University of Potsdam)  
**Project Type:** Intermediate Module (IM) Cognitive Systems  

---

### 📌 Project Overview
This project examines how Reddit users formulate and contest generational stereotypes regarding Gen Z, Millennials, Boomers, and Gen X. By analyzing 1,568 validated claims extracted from 4,199 raw parent-reply pairs, we map the "linguistic packaging" of stereotypes and the sophisticated "reframing moves" users employ to defend their generational identity.

### 🔬 Research Questions (RQs)
* **RQ1:** What kinds of frames appear in generational stereotype claims?
* **RQ2:** How are stereotypes distributed by source type (auto-, hetero-, and counter-stereotypes)?
* **RQ3:** How do users respond (stance and counter-moves such as “not all,” counterexamples, and reframing)?
* **RQ4 (Exploratory):** How is Gen X positioned relative to the other groups?

---

### 📚 Theoretical Framework & Methodology
The analysis is grounded in **Entman’s (1993) Framing Theory**, focusing on four functions: defining problems, diagnosing causes, making moral evaluations, and suggesting remedies.

#### Technical Pipeline: "LLM-as-Annotator"
Following **Grasso, Locci & Stede (2025)**, we utilized a Human-in-the-Loop pipeline:
* **Extraction:** Lexicon-based and dependency-cued sampling (spaCy) via the Reddit API.
* **Annotation:** Large-scale annotation using the GPT-4o API with a Reasoning-First Strategy.
* **Validation:** The pipeline was validated against a manually adjudicated Gold Standard (N=200).
    * **Detection Agreement:** $\kappa = 0.476$ (Moderate)
    * **Thematic Framing Agreement:** $\kappa = 0.487$ (Moderate)
    * **Valence Agreement:** $\kappa = 0.462$ (Moderate)

---

### 📊 Key Findings & Hypothesis Testing

#### H1: Linguistic Packaging (Noun Labels)
**Confirmed.** Noun-label generics (e.g., "The Boomers are...") co-occur significantly more with boosters and negative polarity than adjectival forms, facilitating the reification and "othering" of social groups.

#### H2: The Reframing Paradox (Generic vs. Specific)
**Confirmed.** The "packaging" of a claim determines its defensibility:
* **Generic Claims** act as a **Systemic Shield**; they are reframed 51.7% of the time as users shift the "Diagnostic Cause" to economic or historical contexts.
* **Specific Anecdotes** act as an **Evidence Trap**; they are reframed only 30.0% of the time, as defenders are "trapped" by the specific facts of the event.

#### H3: Hetero- vs. Auto-Stereotypes
**Confirmed.** Hetero-stereotypes (othering) skew heavily negative (>50%), while Auto-stereotypes (self-ascription) are significantly more nuanced, often serving to mitigate or explain group behavior.

#### H4: Gen X Invisibility
**Confirmed.** Despite equal search parameters, Gen X appeared in less than 1% of validated claims, empirically confirming their status as the "Invisible Generation" in digital generational conflict.

### 🛠 Taxonomy of Reframing Moves
Our qualitative analysis identified five primary "pivots" used to redirect blame:
* **Systemic Shield:** Shifting cause to market forces (e.g., housing prices). Found in 30% of Economic reframes.
* **Information Shift:** Blaming the media ecosystem/algorithms. Found in 26% of Tech reframes.
* **Historical Context:** Explaining behavior through the era/upbringing of the group.
* **Individual Condition:** Pathologizing behavior as an individual trait (e.g., ADHD).
* **Empathy Pivot:** Shifting focus to shared human struggles or tragic loss.

---

### 📂 Repository Structure

```plaintext
├── data/                    # Samples of raw and annotated JSONL/CSV files
├── notebooks/               # Kaggle notebooks for extraction and analysis
├── visualizations/          # Heatmaps, Bar charts, and the Reframing Matrix
├── README.md                # Project overview and findings

---

*This project was completed as part of the Intermediate Module (IM) in Cognitive Systems at the University of Potsdam.*
