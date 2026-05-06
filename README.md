# Framing Generational Stereotypes on Reddit
## A Study of Interactional Reframing in Social Media Replies

**Author:** Iana Arefeva  
**Supervisor:** Prof. Manfred Stede (Applied Computational Linguistics, University of Potsdam)  
**Project Type:** Intermediate Module (IM) Cognitive Systems  

---

### Project Overview
This project investigates how Reddit users construct and contest generational stereotypes concerning Gen Z, Millennials, Boomers, and Gen X. By analysing $N = 1,568$ validated claims, we map the relationship between the "linguistic packaging" of stereotypes and the strategic "thematic pivots" users employ to defend their generational identity.

--- 

### Hypotheses & Key Findings
This project tested four core hypotheses derived from framing theory and sociolinguistic literature. All hypotheses were statistically supported.

#### H1: The Noun-Label Effect (Linguistic Packaging)
* **Hypothesis:** Noun-label generics (e.g., "The Boomers are...") co-occur more with negative polarity than adjectival forms.
* **Result: Confirmed ($p = 0.0089$).** Nominalisation facilitates the essentialisation and "othering" of social groups. Claims using bare nouns were significantly more likely to be negative than those using descriptive adjectives.

#### H2: The Reframing Paradox (Abstraction vs. Contestation)
* **Hypothesis:** Generic/abstract claims elicit higher levels of disagreement and successful reframing than concrete anecdotes.
* **Result: Confirmed ($p < 0.001$).** Generic claims act as "soft targets"; they trigger high disagreement but are reframed successfully **51.7%** of the time. Conversely, specific anecdotes act as "evidence traps"; they are reframed only **30.0%** of the time, as granular details anchor the stereotype.

#### H3: Strategic Move Matrix (Frame Transitions)
* **Finding:** Reframing is a strategic thematic shift. While ideological topics like *Values/Politics* are highly stable (**81.0%**), behavioural frames like *Competence* are volatile (only **26.3%** retention). Responders frequently pivot from competence to politics (**36.8%**) to de-legitimise the original claim.

#### H4: In-group vs. Out-group Bias (Perspective)
* **Hypothesis:** Hetero-stereotypes (talking about other groups) elicit more negative counters than auto-stereotypes (self-ascription).
* **Result: Confirmed ($p < 0.001$).** Out-group talk is more than twice as likely to be negative (>50%), while auto-stereotypes are frequently used to justify or mitigate group behaviour through systemic explanations.

#### H5: Generational Invisibility (Exploratory)
* **Hypothesis:** Gen X appears significantly less frequently in high-friction generational discourse.
* **Result: Confirmed.** Gen X was the target of less than **0.4%** of validated claims, identifying a process of **framing through omission** on the platform.

---

### Theoretical Framework & Methodology
The analysis is grounded in **Entman’s (1993) Framing Theory**, focusing on four functions: defining problems, diagnosing causes, making moral evaluations, and suggesting remedies.

#### Technical Pipeline: "LLM-as-Annotator"
Following **Grasso, Locci & Stede (2025)**, we utilised a Human-in-the-Loop pipeline:
* **Extraction:** Lexicon-based and dependency-cued sampling (spaCy) via the Reddit API.
* **Annotation:** Large-scale labelling using the GPT-5.2 API with a **Reasoning-First Strategy**, forcing the model to identify Entman's framing functions before assigning labels.
* **Validation:** The pipeline was validated against a manually adjudicated Gold Standard ($N=200$).
    * **Thematic Framing Agreement:** $\kappa = 0.487$ (Moderate)
    * **Valence/Stance Agreement:** $\kappa = 0.462$ (Moderate)

