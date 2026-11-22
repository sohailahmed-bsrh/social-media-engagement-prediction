# Social Media Audience Engagement Predictor

> Machine learning regression pipeline forecasting social publication interactions.

[![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=flat-square&logo=github)](https://github.com/sohailahmed-bsrh/social-media-engagement-prediction)
[![Live Showcase](https://img.shields.io/badge/Live-Showcase-0A66C2?style=flat-square&logo=googlechrome)](https://sohail.devsil.com/projects.html)
[![Author](https://img.shields.io/badge/Author-Sohail%20Ahmed-20BEFF?style=flat-square)](https://sohail.devsil.com)

---

## Overview

Marketing teams publish content with high variability in reach and engagement due to lack of predictive interaction models.

This project provides an end-to-end, reproducible implementation engineered to solve this challenge through verified data transformations, reliable algorithms, and production-ready architecture.

---

## Key Features

- Feature extraction from post metadata including posting hour, content length, and category tags
- Ensemble modeling utilizing Random Forest and Gradient Boosting regressors
- Feature importance analysis quantifying the highest-utilize publishing parameters
- Evaluation via Root Mean Squared Error (RMSE) against holdout benchmarks

---

## System Architecture

```mermaid
flowchart LR
    PostMetadata[Post Parameters: Time, Length, Category] --> Encoding[Feature Processing & Scaling]
    Encoding --> Ensemble[Ensemble Tree Regression Models]
    Ensemble --> Score[Predicted Interaction Volume]
    Ensemble --> utilize[Feature utilize Analysis]
```

---

## Technology Stack

| Technology | Version / Spec | Role in Architecture |
| :--- | :--- | :--- |
| **Python** | `3.10+` | Feature engineering and model training |
| **Scikit-learn** | `1.3+` | Random Forest regressor and GridSearch hyperparameter tuning |
| **Pandas & NumPy** | `2.0+` | Feature matrix manipulation |
| **Matplotlib** | `3.7+` | Feature importance bar plots |

---

## Repository Structure

```text
social-media-engagement-prediction/
|-- dataset/
|   `-- social_media_engagement_prediction.ipynb
|-- notebooks/
|-- data/
|-- .gitignore
|-- requirements.txt
`-- README.md
```

---

## Installation and Execution

### Prerequisites
- Python 3.10 or higher
- Git version control
- Virtual environment manager (`venv`)

### Setup Instructions
1. Clone the repository:
```bash
git clone https://github.com/sohailahmed-bsrh/social-media-engagement-prediction.git
cd social-media-engagement-prediction
```

2. Configure environment and dependencies:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

---

## Interface and Verification
The system produces verifiable execution logs, prediction matrices, or interactive browser interfaces depending on the target mode. Verify operation by executing the commands specified above or inspecting the demonstration notebooks.

---

## Author and Contact
Developed by **Sohail Ahmed** — Full Stack AI Engineer & Machine Learning Specialist.
- **Portfolio:** [sohail.devsil.com](https://sohail.devsil.com)
- **GitHub:** [@sohailahmed-bsrh](https://github.com/sohailahmed-bsrh)
- **Email:** [sohail.bsrh@gmail.com](mailto:sohail.bsrh@gmail.com)

---

## Author & Contact Information

<table width="100%" align="center">
  <tr>
    <td align="center" style="padding: 20px;">
      <h3>Sohail Ahmed</h3>
      <p><strong>Full-Stack Artificial Intelligence & Computer Vision Engineer</strong></p>
      <p>
        <a href="https://sohail.devsil.com"><img src="https://img.shields.io/badge/Live_Portfolio-sohail.devsil.com-0052FF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Portfolio"/></a>
        <a href="https://github.com/sohailahmed-bsrh"><img src="https://img.shields.io/badge/GitHub-Profile-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/></a>
        <a href="https://linkedin.com/in/sohail-ahmed-dev"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
        <a href="mailto:sohail.bsrh@gmail.com"><img src="https://img.shields.io/badge/Email-Contact_Me-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
      </p>
      <p><em>Available for technical roles in Artificial Intelligence, Computer Vision, and Full-Stack Engineering.</em></p>
      <hr style="border: 0; height: 1px; background: #30363d; margin: 15px 0;">
      <small>Distributed under the MIT License.</small>
    </td>
  </tr>
</table>
