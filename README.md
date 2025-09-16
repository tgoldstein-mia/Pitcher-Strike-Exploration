Pitcher Strike Exploration 

Pitch Types: Fastballs only (Four-Seam, Sinker, generic Fastball) for a single pitcher.

Goal: Quantify how individual biomechanics/kinematics relate to release velocity, then visualize how key metrics vary by date and throughout each outing.

Uses: 
Robust filtering: Per-metric MAD outlier screen (±3×MAD) to reduce sensor noise before modeling.
Bayesian regressions: For each numeric metric, fit a separate Bayesian linear model (stan_glm) predicting releaseSpeed ~ metric; extract slope/intercept and plot fitted lines.
Automation & export: Generate a PDF report with one scatter-plus-fit plot per metric.


Exploration views:
By date: Boxplot + jitter to compare a metric’s distribution across session dates.
Within outings: Faceted time-series of a metric vs. pitch number (ordered by PITCH_RELEASE_DATETIME) to spot in-game drift/fatigue patterns.
