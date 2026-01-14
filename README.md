# Behavioral Anomaly Detection in Study Hours

## Overview
This project detects abnormal study behavior by analyzing daily study hours over time.
Instead of predicting outcomes, it identifies days where study patterns significantly deviate
from the student’s own historical behavior.

The focus of this project is **understanding behavior patterns** using simple and explainable
statistical techniques.

---

## Problem Statement
Students often have consistent study routines. Sudden drops or spikes in study hours may
indicate unusual circumstances such as fatigue, stress, exams, or loss of motivation.

This project aims to:
- Model normal study behavior dynamically
- Detect days with abnormal study hours
- Visually and logically validate detected anomalies

---

## Dataset
The dataset is a time-series dataset containing:

- `date` – Daily dates
- `study_hours` – Number of hours studied per day

The dataset is synthetically generated to simulate realistic study patterns along with
intentional anomalies.

---

## Methodology
1. Generated daily study hour data for 90 days
2. Loaded and inspected the dataset using Pandas
3. Visualized raw study behavior over time
4. Calculated rolling mean and rolling standard deviation (7-day window)
5. Defined dynamic anomaly thresholds using:
   - Rolling Mean ± 2 × Rolling Standard Deviation
6. Flagged days outside this range as anomalies
7. Visualized anomalies to validate detection logic

---

## Key Observations
- Normal study behavior remains within a stable range of daily hours
- Anomalies occur on days with extremely low or high study hours
- Detected anomalies represent sudden deviations, not gradual behavior changes
- The approach adapts to changing behavior patterns over time

---

## Tools & Libraries Used
- Python
- Pandas
- NumPy
- Matplotlib

---

## What This Project Demonstrates
- Time-series data handling
- Rolling statistics for behavioral analysis
- Explainable anomaly detection
- Data visualization for validation
- End-to-end data science workflow

---

## Future Improvements
- Sensitivity analysis using different threshold values
- Isolation Forest–based anomaly detection
- Multivariate anomaly detection using additional behavioral features
- Application to real-world data

---

## Note
This project prioritizes interpretability and understanding over complex models or high accuracy,
making it a strong foundation for advanced data science projects.
