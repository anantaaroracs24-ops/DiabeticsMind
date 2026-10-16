# DiabeticsMind 🩺
### AI-Powered Diabetes Risk Prediction and Mental Health Analysis

## 1. Overview

**DiabeticsMind** is a machine learning and AI-based healthcare project designed to predict diabetes risk and explore the relationship between diabetes, depression, and lifestyle factors.

The project uses publicly available health survey data to identify patterns in demographic, clinical, and behavioral characteristics. It aims to combine predictive analytics with a Retrieval-Augmented Generation (RAG) system to provide relevant, evidence-based health information.

## 2. Problem Statement

Diabetes is a major public health concern that can affect both physical and mental well-being. Traditional risk assessment approaches may not adequately consider the combined influence of lifestyle, demographic, clinical, and mental health factors.

DiabeticsMind aims to analyze these factors using machine learning and explore how diabetes and mental health indicators are associated.

## 3. Objectives

- Develop machine learning models for diabetes risk prediction.
- Analyze the relationship between diabetes and depression.
- Identify important demographic, clinical, and lifestyle factors.
- Perform exploratory data analysis and visualize health patterns.
- Compare the performance of different predictive models.
- Integrate a RAG-based system to retrieve relevant health information.
- Present results in an understandable and accessible format.

## 4. Dataset

The project uses publicly available data from the **National Health and Nutrition Examination Survey (NHANES)** conducted by the U.S. Centers for Disease Control and Prevention (CDC).

**Dataset period:** 2017–March 2020 pre-pandemic cycle.

**File format:** SAS Transport (`.XPT`)

### Dataset Components

| File | Description |
|---|---|
| `DEMO_J.XPT` | Demographic and socioeconomic information |
| `DIQ_J.XPT` | Diabetes questionnaire |
| `DPQ_J.XPT` | Depression questionnaire |
| `GHB_J.XPT` | Glycohemoglobin (HbA1c) |
| `GLU_J.XPT` | Blood glucose measurements |
| `BMX_J.XPT` | Body measurements, including BMI |
| `BPQ_J.XPT` | Blood pressure questionnaire |
| `PAQ_J.XPT` | Physical activity |
| `SLQ_J.XPT` | Sleep information |
| `SMQ_J.XPT` | Smoking information |
| `ALQ_J.XPT` | Alcohol use |

The relevant datasets are linked using the common participant identifier `SEQN`.

**Official source:** [CDC NHANES](https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?Cycle=2017-2020)

## 5. Technology Stack

- **Programming Language:** Python
- **Data Processing:** Pandas, NumPy
- **Machine Learning:** Scikit-learn, XGBoost
- **Deep Learning:** TensorFlow, Keras, CNN, RNN
- **Data Visualization:** Matplotlib, Seaborn
- **Database:** SQL
- **AI and RAG:** Large Language Models (LLMs), Embeddings, Vector Database
- **Development Environment:** Jupyter Notebook, VS Code
- **Version Control:** Git, GitHub

*The final implementation may use only the libraries and models required for the selected approach.*

## 6. Project Methodology

The project follows these major stages:

1. **Data Collection:** Obtain the relevant NHANES datasets.
2. **Data Loading:** Import `.XPT` files into Python using Pandas.
3. **Data Integration:** Merge relevant files using `SEQN`.
4. **Data Cleaning:** Handle missing values, duplicate records, and inconsistent data.
5. **Exploratory Data Analysis:** Study distributions, correlations, and patterns.
6. **Feature Engineering:** Select relevant features and construct appropriate target variables.
7. **Data Preprocessing:** Encode categorical variables and scale numerical features where required.
8. **Model Training:** Train selected machine learning and deep learning models.
9. **Model Evaluation:** Compare models using appropriate performance metrics.
10. **RAG Integration:** Retrieve relevant information from a curated health knowledge base.
11. **Result Presentation:** Present predictions, visualizations, and relevant information.

## 7. Machine Learning Approach

The project explores supervised learning for diabetes risk prediction.

### Candidate Models
- Logistic Regression
- Decision Tree
- Random Forest
- XGBoost
- Neural Networks

CNN and RNN architectures may be explored if justified by the data representation and project requirements.

### Model Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix

Since missing diabetes cases can have serious consequences, recall and other class-sensitive metrics are important alongside accuracy.

## 8. Exploratory Data Analysis

Exploratory data analysis helps identify patterns and relationships among the selected variables.

Planned analyses include:
- Distribution of diabetes status.
- Age and BMI distributions.
- HbA1c and blood glucose patterns.
- Depression score distribution.
- Diabetes status across demographic groups.
- Relationships between lifestyle factors and health indicators.
- Correlation analysis of numerical features.

Visualizations are created using Matplotlib and Seaborn.

## 9. RAG-Based Health Information System

The proposed RAG component complements predictive modeling by retrieving relevant information from a curated knowledge base.

### RAG Workflow

1. Collect reliable health documents and educational resources.
2. Divide documents into manageable text chunks.
3. Generate embeddings for the chunks.
4. Store embeddings in a vector database.
5. Retrieve relevant information based on a user's query.
6. Provide a response grounded in the retrieved content.

The RAG component is intended to support health education and explain relevant concepts. It does not replace professional medical advice.

## 10. Expected Outcomes

- A cleaned and integrated dataset for analysis.
- Comparative evaluation of diabetes prediction models.
- Visualizations of important demographic, clinical, and lifestyle patterns.
- Analysis of associations between diabetes and depression indicators.
- A foundation for integrating predictive analytics with RAG-based health information retrieval.

These are project objectives; actual performance and outcomes will be reported after implementation and evaluation.

## 11. Project Structure

```text
DiabeticsMind/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   └── exploratory_data_analysis.ipynb
│
├── src/
│   ├── data_preprocessing.py
│   ├── feature_engineering.py
│   ├── model_training.py
│   └── model_evaluation.py
│
├── models/
├── rag/
├── visualizations/
├── requirements.txt
└── README.md
```

## 14. Future Scope

- Develop a user-friendly web application.
- Improve model performance through systematic experimentation.
- Add explainability techniques such as SHAP.
- Expand the health knowledge base for RAG.
- Integrate additional validated datasets where appropriate.
- Explore personalized health education and risk-factor insights.
- Evaluate generalizability across different populations.

## 16. References

1. [CDC National Health and Nutrition Examination Survey (NHANES)](https://www.cdc.gov/nchs/nhanes/)
2. [NHANES 2017–March 2020 Pre-Pandemic Data Files](https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?Cycle=2017-2020)
3. [Scikit-learn Documentation](https://scikit-learn.org/stable/)
4. [TensorFlow Documentation](https://www.tensorflow.org/)
5. [Pandas Documentation](https://pandas.pydata.org/docs/)

---

**Developed as an academic machine learning and AI project.**
