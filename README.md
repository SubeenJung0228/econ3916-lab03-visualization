# Honest vs. Misleading Visualizations

**Objective:** This project demonstrates how identical statistical summaries
and identical datasets can be visually framed to tell contradictory stories,
and establishes a quantitative standard (the Lie Factor) for detecting when
a chart distorts the data it claims to represent.

## Methodology

- Recreated Anscombe's Quartet, four datasets sharing identical means,
  variances, and correlation coefficients, to demonstrate that summary
  statistics alone cannot substitute for visual inspection of data
- Quantified chart distortion using Tufte's Lie Factor metric, calculating
  a value of 49.0 for a truncated-axis revenue chart before redesigning it
  as an honest, appropriately-scaled visualization
- Constructed four distinct visualizations of the same real average hourly
  earnings series (FRED AHETPI, deflated to 2020 dollars) to illustrate how
  axis truncation, time-window selection, and scale choice can each
  independently shift a reader's interpretation of identical underlying data
- Executed a systematic four-step exploratory data analysis (structure,
  distributions, relationships, anomalies) on a World Bank GDP panel
  spanning 262 countries and 64 years
- Developed an interactive dashboard (ipywidgets) enabling real-time
  toggling between nominal and real earnings, adjustable axis truncation,
  and a live-updating Lie Factor readout

## Key Findings

- Anscombe's Quartet confirmed that four datasets with identical correlation
  (r ~ 0.816) can range from a clean linear relationship to a curve, an
  outlier-driven fit, and a near-vertical cluster, underscoring that summary
  statistics must never be trusted without a corresponding plot.
- The truncated revenue chart exaggerated an actual 4.1% increase into an
  apparent 200% surge, a Lie Factor of 49.0, illustrating how a seemingly
  minor axis choice can misrepresent a real, modest result as explosive
  growth.
- The four-panel wage series showed that the same real earnings data can be
  framed to support opposite narratives: a truncated axis dramatizes
  short-term stagnation, a cherry-picked recent window hides four decades of
  decline, and a log scale visually compresses the very structural breaks
  most relevant to policy analysis.
- The World Bank GDP panel was extremely right-skewed (skewness of 8.4,
  reduced to 0.2 after a log transform) and exhibited missingness
  concentrated at both ends of the time series, consistent with data that
  is Missing Not At Random (MNAR) rather than a random reporting gap.
