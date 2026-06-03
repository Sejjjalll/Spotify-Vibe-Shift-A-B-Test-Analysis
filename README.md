
# Spotify Vibe Shift: A/B Test Analysis

**Sejal Khade** | MS Data Science Candidate | University of Texas at Arlington | May 2026

A product analytics project evaluating whether emotionally opposite music recommendations can increase user engagement and music discovery on a streaming platform.

**Data Source:** Spotify Dataset from Kaggle

---

## Project Overview

Music streaming platforms continuously balance personalization with discovery. While recommendation systems are highly effective at serving familiar content, excessive personalization can reduce exploration and limit user engagement over time.

This project evaluates a hypothetical feature called **Vibe Shift**, which recommends songs that are emotionally opposite to a user's typical listening preferences. Using user segmentation, experimental design principles, and statistical analysis, the project investigates whether strategic disruption can improve engagement while maintaining a positive user experience.

---

## Business Objective

Determine whether opposite-vibe recommendations increase user engagement compared with standard recommendations and identify which user segments benefit most from the intervention.

### Key Questions

- Does Vibe Shift increase engagement?
- Which users respond positively to opposite recommendations?
- Are there user segments where the feature creates negative experiences?
- Should the feature be launched universally or selectively?

---

## Key Findings

### Overall Result

The treatment group demonstrated a **9.7% increase in engagement** compared with the control group.

**Result:** Statistically significant (p < 0.001)

However, aggregate results masked substantial differences across user segments.

### Moderate Comfort Zone Users

**Best-performing segment**

- +11.9% engagement lift
- p < 0.001
- Cohen's d = 0.52
- Guardrails passed

**Recommendation:** Launch feature for this segment.

### Narrow Comfort Zone Users

- +10.1% engagement lift
- Marginal statistical significance
- Skip-rate guardrail violation (+11.9 percentage points)

Users showed increased exploration but also demonstrated resistance to highly disruptive recommendations.

**Recommendation:** Test modified versions before launch.

Potential follow-up experiments:

- Gradual recommendation shifts
- Genre-preserving emotional shifts
- User-controlled discovery mode

### Wide Comfort Zone Users

- +6.0% engagement lift
- Not statistically significant (p = 0.13)

These users already explore broadly and showed limited incremental benefit.

**Recommendation:** Do not launch for this segment.

---

## Business Recommendations

### Immediate Launch

Deploy Vibe Shift for Moderate Comfort Zone Users.

This segment demonstrated the strongest combination of:

- Engagement improvement
- Meaningful effect size
- Positive user experience metrics

### Additional Testing

Conduct follow-up experiments for Narrow Comfort Zone Users using less disruptive recommendation strategies.

### No Launch

Exclude Wide Comfort Zone Users because the feature produced no statistically significant improvement.

The findings highlight a classic example of heterogeneous treatment effects: the same intervention generates different outcomes depending on user characteristics.

For detailed recommendations, see:

**Business_Recommendations.md**

---

## Methodology

### Data Preparation

- Cleaned and processed approximately 32,000 Spotify tracks
- Removed duplicates and handled missing values
- Standardized audio features for analysis

### Exploratory Analysis

Analyzed Spotify audio features including:

- Valence
- Energy
- Danceability
- Acousticness
- Speechiness

Valence and energy were selected as the primary emotional dimensions for defining listening behavior and recommendation shifts.

### User Segmentation

Created listening diversity scores and segmented users using K-Means clustering into:

- Narrow Comfort Zone Users
- Moderate Comfort Zone Users
- Wide Comfort Zone Users

### Experimental Design

A simulated A/B test was developed to mimic a real-world product experiment.

**Control Group**
- Users receive standard recommendations aligned with existing preferences.

**Treatment Group**
- Users receive recommendations with emotional characteristics opposite to their typical listening patterns.

**Experiment Controls**
- Stratified random assignment
- Balanced user segments across groups
- Guardrail metrics for user experience monitoring

---

## Statistical Analysis

The experiment was evaluated using:

- Two-sample t-tests
- Confidence intervals
- Cohen's d effect sizes
- Segment-level treatment effect analysis
- Guardrail metric evaluation

---

## Tools & Technologies

- Python
- Pandas
- NumPy
- SciPy
- Scikit-Learn
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Dataset

- Source: Kaggle Spotify Dataset
- Approximately 32,000 songs
- 470 playlists treated as unique users
- Audio features including valence, energy, danceability, acousticness, and speechiness

---

## Repository Structure

```text
├── notebooks/
│   ├── 1_Data_Cleaning.ipynb
│   ├── 2_EDA.ipynb
│   ├── 3_Experiment.ipynb
│   └── 4_Stat_Test.ipynb
├── data/
├── Business_Recommendations.md
└── README.md
````

## Running the Project

### 1. Download Dataset

Download the Spotify dataset from Kaggle and place it in the `data/` folder.

### 2. Install Dependencies

```bash
pip install pandas numpy scipy matplotlib seaborn scikit-learn jupyter
```

### 3. Execute Notebooks

Run notebooks in the following order:

1. Data Cleaning
2. Exploratory Data Analysis
3. Experiment Simulation
4. Statistical Testing

---

## Limitations

This project uses simulated treatment effects to demonstrate experimentation, product analytics, and statistical inference workflows.

In a production environment, a real implementation would include:

* Live A/B testing
* Longitudinal retention analysis
* User research and feedback collection
* Revenue and lifetime-value impact measurement
* Controlled rollout strategies

---

## Future Enhancements

* Personalized recommendation-shift intensity
* Long-term retention analysis
* Adaptive experimentation frameworks
* User-level response modeling
* Additional behavioral segmentation techniques

---

## Contact

**Email:** [ssk8336@mavs.uta.edu](mailto:ssk8336@mavs.uta.edu)

**LinkedIn:** linkedin.com/in/sejallk

```
```
