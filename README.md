# Social Media Engagement Prediction & Virality Modeling

<p align="center">
  <a href="https://sohail.devsil.com"><strong>Portfolio</strong></a> | 
  <a href="https://github.com/sohailahmed-bsrh"><strong>GitHub Profile</strong></a> | 
  <a href="https://github.com/sohailahmed-bsrh/social-media-engagement-prediction"><strong>Source Repository</strong></a>
</p>

---

## Executive Summary & Problem Statement

Social media algorithms prioritize posts that achieve rapid early engagement (likes, shares, comments, retweets). Marketing teams and content creators often publish without knowing which parameters (posting time, hashtag density, media type, caption length, sentiment) maximize distribution algorithms.

This project implements a **Predictive Social Media Engagement Pipeline**. By modeling historical audience interactions, content features, and temporal publishing variables, the engine forecasts engagement velocity prior to publication, allowing marketing teams to optimize post metadata for maximum reach.

<div align="center">
  <img src="https://raw.githubusercontent.com/sohailahmed-bsrh/myportfolio/main/assets/images/thumbnail/social-media-engagement.jpeg" width="650" alt="Social Media Engagement Prediction"/>
  <p><em>Predictive virality modeling and content parameter optimization engine.</em></p>
</div>

---

## Real-World Industry Applications

- **Editorial Scheduling Optimization**: Determines the optimal hour and day of week to release high-priority corporate announcements.
- **Content Format Decision Making**: Quantifies expected engagement lift between static imagery, carousels, and video formats.
- **Influencer Campaign Valuation**: Estimates expected impressions and engagement rates for prospective sponsored brand deals.
- **Copywriting A/B Calibration**: Analyzes caption character length and sentiment polarity to maximize discussion and share rates.

---

## Technical Architecture & Engineering Walkthrough

```
                     [Social Media Multi-Platform Dataset]
                                       │
                                       ▼
                   [Feature Extraction & NLP Sentiment Analysis]
                 (Hashtag Count, Sentiment Score, Post Hour, Media)
                                       │
                                       ▼
                   [Multi-Output Target Definition (Log-Scaled)]
                         (Likes, Comments, Shares, Retweets)
                                       │
         ┌─────────────────────────────┼─────────────────────────────┐
         ▼                             ▼                             ▼
[Random Forest Regressor]       [Gradient Boosting (GBDT)]      [XGBoost Regressor]
(Non-Linear Tree Splits)      (Sequential Residual Shrinkage)  (L1/L2 Regularized Trees)
         │                             │                             │
         └─────────────────────────────┼─────────────────────────────┘
                                       │
                                       ▼
                     [SHAP Attribution & Feature Importance]
                                       │
                                       ▼
                [Pre-Publication Optimization Recommendations]
```

### Step 1: Content Ingestion & Metadata Processing
Loads and cleans engagement logs (`dataset/social_media_engagement_prediction.ipynb`). Normalizes engagement distributions across follower counts to establish standardized engagement ratios.

### Step 2: Feature Engineering & NLP Enrichment
Extracts temporal signals (Hour of Day, Day of Week, Weekend Flag), structural signals (Character Length, Word Count, Hashtag Density), and content indicators (Presence of Video, Image, Link).

### Step 3: Target Transformation
Social metrics follow extreme power-law distributions where viral outliers distort linear estimators. Applies logarithmic scaling `y = log(1 + engagement)` to linearize target variances.

### Step 4: Machine Learning Model Benchmarking
Trains and cross-validates multiple regression architectures (Random Forest, Gradient Boosting, XGBoost), optimizing for low Mean Absolute Error (MAE) and high explained variance ($R^2$).

### Step 5: Feature Importance & Interpretability
Calculates feature importance rankings via SHAP and permutation importance, pinpointing the exact levers that drive viral velocity across social channels.

---

## Technology Stack & Implementation Specifications

| Component | Technology | Version | Architectural Function |
| :--- | :--- | :--- | :--- |
| **Machine Learning** | Scikit-Learn | 1.3+ | Regressor architectures, cross-validation, scaling |
| **Tree Ensembles** | XGBoost | 2.0+ | Extreme gradient boosted decision trees |
| **Data Engine** | Pandas / NumPy | 2.x | Column transformations, time series indexing |
| **Visualization** | Matplotlib / Seaborn | 3.8+ | Target distribution plots and feature importance charts |

---

## Installation & Execution Guide

```bash
git clone https://github.com/sohailahmed-bsrh/social-media-engagement-prediction.git
cd social-media-engagement-prediction
python -m venv venv
# Windows: venv\Scriptsctivate | Unix: source venv/bin/activate
pip install -r requirements.txt
jupyter notebook dataset/social_media_engagement_prediction.ipynb
```

---

## Author & Contact Information

<table width="100%">
  <tr>
    <td width="150" align="center" valign="middle">
      <img src="https://avatars.githubusercontent.com/u/231165170?v=4" width="120" style="border-radius: 50%;" alt="Sohail Ahmed"/>
    </td>
    <td>
      <h3>Sohail Ahmed</h3>
      <p><strong>Senior Software Engineer & AI Systems Architect</strong></p>
      <p>Specializing in Full-Stack AI Application Development, Computer Vision, Deep Learning Pipelines, and Scalable Automation Architectures.</p>
      <p>
        <a href="https://sohail.devsil.com"><strong>Portfolio Website</strong></a> | 
        <a href="https://github.com/sohailahmed-bsrh"><strong>GitHub Profile</strong></a> | 
        <a href="https://www.linkedin.com/in/sohail-ahmed-devsil/"><strong>LinkedIn</strong></a> | 
        <a href="https://www.kaggle.com/sohail2411126"><strong>Kaggle</strong></a> | 
        <a href="https://x.com/ahmed241126"><strong>Twitter/X</strong></a> | 
        <a href="mailto:se906403@gmail.com"><strong>Email Contact</strong></a>
      </p>
    </td>
  </tr>
</table>
