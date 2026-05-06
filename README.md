# Framing Generational Stereotypes on Reddit
## A Study of Interactional Reframing in Social Media Replies

**Author:** Iana Arefeva  
**Supervisor:** Prof. Manfred Stede (Applied Computational Linguistics, University of Potsdam)  
**Project Type:** Intermediate Module (IM) Cognitive Systems  

---

### 📌 Project Overview
This project investigates how Reddit users construct and contest generational stereotypes concerning Gen Z, Millennials, Boomers, and Gen X. By analysing 1,568 validated claims, we map the relationship between the "linguistic packaging" of stereotypes and the strategic "thematic pivots" users employ to defend their generational identity.

### 🔬 Research Questions (RQs)
* **RQ1:** Which thematic frames are most common across different generational groups?
* **RQ2:** Does the use of noun-label generics correlate with increased linguistic negativity?
* **RQ3:** How does the level of abstraction (Generic vs. Specific) influence the success of a counter-move?
* **RQ4:** What are the characteristic thematic transitions (pivots) used during reframing?
* **RQ5 (Exploratory):** How is Gen X positioned within high-friction generational discourse?

---

### 📚 Theoretical Framework & Methodology
The analysis is grounded in **Entman’s (1993) Framing Theory**, focusing on four functions: defining problems, diagnosing causes, making moral evaluations, and suggesting remedies.

#### Technical Pipeline: "LLM-as-Annotator"
Following **Grasso, Locci & Stede (2025)**, we utilised a Human-in-the-Loop pipeline:
* **Extraction:** Lexicon-based and dependency-cued sampling (spaCy) via the Reddit API.
* **Annotation:** Large-scale labelling using the GPT-5.2 API with a **Reasoning-First Strategy**, forcing the model to identify Entman's framing functions before assigning labels.
* **Validation:** Validated against a manually adjudicated Gold Standard ($N=200$).
    * **Thematic Framing Agreement:** $\kappa = 0.487$ (Moderate)
    * **Valence/Stance Agreement:** $\kappa = 0.462$ (Moderate)

---

### 📊 Key Findings

#### 1. The Noun-Label Effect (H1)
**Confirmed ($p = 0.0089$).** Noun-label generics (e.g., "The Boomers are...") co-occur significantly more with negative polarity than adjectival forms. This suggests that nominalisation facilitates the essentialisation and "othering" of generational groups.

#### 2. The Reframing Paradox (H2)
**Confirmed ($p < 0.001$).** Abstract **Generic Claims** act as "soft targets"; they trigger high disagreement but are reframed successfully 51.7% of the time. Conversely, **Specific Anecdotes** act as "evidence traps"; they are reframed only 30.0% of the time, as the granular details anchor the stereotype and make it harder to contest.

#### 3. Strategic Move Matrix: Frame Transitions (RQ4)
Our transition analysis reveals how users "move the goalposts" during an argument:
* **High-Stability Frames:** Ideological and structural topics like *Values/Politics* (81.0%) and *Work/Economy* (71.7%) are highly "sticky." Users tend to fight these stereotypes on their own thematic terrain.
* **High-Volatility Pivots:** Behavioural frames like *Competence* are the most unstable (only 26.3% retention). Responders frequently pivot to *Values/Politics* (36.8%), reframing a lack of skill as a symptom of a broader ideological clash.
* **The Meta Shield:** Users frequently pivot to *Meta/Identity* frames (up to 30.3% of the time) to challenge the validity of generational labels themselves rather than the content of the stereotype.

#### 4. Gen X Invisibility (H5)
**Confirmed.** Despite equal search parameters, Gen X appeared as a target in less than 0.4% of validated claims. This empirically identifies a process of **framing through omission**, where Gen X is largely excluded from the high-friction "battleground" of digital generational conflict.
