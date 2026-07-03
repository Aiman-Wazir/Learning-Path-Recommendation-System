# Learning-Path-Recommendation-System
Learning Path Recommendation System using Collaborative Filtering (SVD Matrix Factorization).A Matrix Factorization (SVD) model was developed to recommend personalized learning modules by identifying hidden patterns in intern-course interactions. The model predicts unseen course ratings and suggests the most suitable courses for each intern.
# Personalized Learning Path Recommendation System using Collaborative Filtering (SVD Matrix Factorization)

## Overview

This project implements a Personalized Learning Path Recommendation System that suggests relevant learning modules to interns based on their previous learning interactions. The recommendation engine uses Collaborative Filtering with Singular Value Decomposition (SVD), a Matrix Factorization technique, to predict unseen course ratings and generate personalized recommendations.

The model is trained using the Open University Learning Analytics Dataset (OULAD), where students are treated as interns and course modules are considered learning modules.

---

## Features

- Personalized course recommendations
- Collaborative Filtering using Matrix Factorization
- SVD-based recommendation engine
- Course rating prediction
- Model evaluation using RMSE and MAE
- Trained model saving and loading
- Google Colab compatible
- Google Drive integration
- Recommendation generation for any intern

---

## Project Structure

```
Learning-Path-Recommendation-System/
│
├── dataset/
│   ├── interns.csv
│   ├── courses.csv
│   ├── learning_history.csv
│   └── original_oulad_files/
│
├── models/
│   └── learning_path_recommender.pkl
│
├── notebooks/
│   └── Learning_Path_Recommendation.ipynb
│
├── recommendations/
│   └── recommendations.csv
│
├── README.md
├── requirements.txt
└── LICENSE
```

---

## Dataset

This project uses the **Open University Learning Analytics Dataset (OULAD)**.

The following files were used:

- studentInfo.csv
- studentAssessment.csv
- assessments.csv
- courses.csv

The datasets were merged and transformed into a final interaction dataset containing:

| Column | Description |
|----------|-------------|
| intern_id | Unique intern identifier |
| course_id | Learning module identifier |
| rating | Converted rating (1–5) |

---

## Data Preprocessing

The following preprocessing steps were performed:

- Loaded OULAD datasets
- Renamed columns
- Merged multiple datasets
- Removed missing values
- Converted assessment scores into ratings (1–5)
- Created Intern-Course interaction dataset

---

## Machine Learning Model

Algorithm:

- Collaborative Filtering
- Matrix Factorization
- Singular Value Decomposition (SVD)

The model learns hidden relationships between interns and learning modules to predict missing ratings and recommend the most relevant courses.

---

## Workflow

```
Raw OULAD Dataset
        │
        ▼
Data Cleaning
        │
        ▼
Dataset Merging
        │
        ▼
Create Intern-Course Matrix
        │
        ▼
Train SVD Model
        │
        ▼
Predict Missing Ratings
        │
        ▼
Generate Top-N Recommendations
        │
        ▼
Evaluate Model
```

---

## Evaluation Metrics

The recommendation model was evaluated using:

- RMSE (Root Mean Squared Error)
- MAE (Mean Absolute Error)

### Results

| Metric | Score |
|----------|--------|
| RMSE | 0.8496 |
| MAE | 0.6851 |

The results indicate that the model effectively predicts intern preferences and provides personalized learning recommendations.

---

## Installation

Clone the repository

```bash
git clone https://github.com/yourusername/Learning-Path-Recommendation-System.git
```

Move into the project

```bash
cd Learning-Path-Recommendation-System
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## How to Run

1. Open the notebook in Google Colab or Jupyter Notebook.
2. Upload the dataset.
3. Install dependencies.
4. Run all notebook cells.
5. Train the SVD model.
6. Save the trained model.
7. Generate personalized recommendations.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Surprise
- Joblib
- Google Colab
- Google Drive

---

## Future Improvements

- Flask Web Application
- Streamlit Dashboard
- Hybrid Recommendation System
- Deep Learning-based Recommendation
- Content-Based Filtering
- Real-time Recommendation API

---

## Author

Aiman Wazir

---

## License

This project is intended for educational and academic purposes.
