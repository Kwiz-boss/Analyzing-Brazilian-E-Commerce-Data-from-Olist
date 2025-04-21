# Olist E-Commerce Dataset Analysis and Modeling using Random Forest

A data science project aimed at analyzing and predicting customer satisfaction using the Olist E-commerce dataset. This project merges relational data from various domains (orders, products, sellers, payments, etc.), extracts insightful features, and builds a machine learning model to predict customer review scores.
---

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Setup and Installation](#setup-and-installation)
- [Data Preparation](#data-preparation)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Future Work](#future-work)
- [Contributors](#contributors)
- [License](#license)

---

## Overview

### Purpose

This project explores patterns in Brazil’s largest e-commerce platform and builds a predictive model to classify customer review scores. It enables:

- Insightful understanding of delivery behavior, seller performance, and product features.
- Predictive modeling to forecast whether a customer is likely to leave a positive review.

### Key Features

- **Data Exploration and Understanding:** 
- **Data Preprocessing**
- **Exploratory Data Analysis (EDA)**
- **Operational Analysis**
- **Business Insights and Recommendations**
- **Pre-trained Machine Learning Model** using Random Forest Classifier.
- **Feature Importance & Visuals:** Insights into the top features influencing satisfaction.

---

## Dataset

### Source

The dataset is sourced from [Kaggle: Olist Brazilian E-Commerce Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce).

### Contents

The dataset is composed of 100k+ orders and 9 CSV tables:

- Customers
- Geolocation
- Orders
- Order Items
- Order Payments
- Order Reviews
- Products
- Sellers
- Product Category Name Translation

These were joined and cleaned to form a unified dataset used in modeling.

---

## Project Structure

```plaintext
Analyzing-Brazilian-E-Commerce-Data-from-Olist/
├── data/                    # CSV files (raw & processed)
│   ├── orders_merged.csv
├── models/                  # Trained model
│   └── model.pkl
├── results/                 # Evaluation plots
│   ├── classification_report_heatmap.png
│   ├── confusion_matrix.png
│   ├── Top 20 features.png
├── requirements.txt         # Python dependencies
├── README.md                # This documentation file
├── notebooks/               # EDA and modeling Jupyter notebooks
```

---

## Setup and Installation

### Prerequisites

- Python 3.8 or higher
- pip package manager
- Git

### Installation Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/Kwiz-boss/Analyzing-Brazilian-E-Commerce-Data-from-Olist.git
   cd Analyzing-Brazilian-E-Commerce-Data-from-Olist
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

---

## Data Preparation

- All CSV files were merged into a consolidated dataframe `orders_merged.csv`.
- Categorical columns (e.g. city, product) were label-encoded.
- Numerical features were scaled using `StandardScaler`.
- The review score was transformed into binary classification (positive vs. negative).
- Feature selection was performed based on importance metrics.

---

## Modeling

- **Model Used:** Random Forest Classifier
- **Training Environment:** Pre-trained and saved (`models/model.pkl`)
- **Features Used:**
  - Delivery duration
  - Freight value
  - Payment installments and values
  - Product category
  - Customer and seller location
  - Order item counts

---

## Evaluation

The model performed well with balanced precision and accuracy:

- **Accuracy:** 85%
- **Precision:** 86%
- **Recall:** 72%
- **F1-Score:** 76%

### Confusion Matrix:

- **True Positives:** 17,367  
- **True Negatives:** 2,660  
- **False Positives:** 3,010  
- **False Negatives:** 430

---

## Future Work

- Incorporate NLP on review comments for text sentiment analysis.
- Expand classification to multi-class (1–5 star ratings).
- Develop and Deploy Web App as a full-stack solution with backend APIs.
- Integrate continuous learning using live feedback.

---

## Contributors

- 👨‍💻 **Kwizera Jean Bosco**  
  Researcher in AI, Machine Learning & Computer Vision  
  [GitHub](https://github.com/Kwiz-boss) | [LinkedIn](https://www.linkedin.com/in/jean-bosco-kwizera-95a517321/)
- 👨‍💻 **Shreeshan panda**
- 👨‍💻 **Marron Tarlue**

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

