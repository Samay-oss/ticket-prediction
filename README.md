# ticket-prediction
Here’s an example GitHub documentation for the **Ticket Purchasing Prediction Model** and **Customer Sentiment Analysis** projects done for British Airways. You can adapt it further depending on your implementation details.

---

# Ticket Purchasing Prediction Model & Customer Sentiment Analysis for British Airways

## Table of Contents
1. [Project Overview](#project-overview)
2. [Ticket Purchasing Prediction Model](#ticket-purchasing-prediction-model)
   - [Dataset](#dataset)
   - [Modeling](#modeling)
   - [Results](#results)
3. [Customer Sentiment Analysis](#customer-sentiment-analysis)
   - [Data Collection](#data-collection)
   - [Sentiment Analysis](#sentiment-analysis)
   - [Insights](#insights)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Contributing](#contributing)
7. [License](#license)

---

## Project Overview

This repository contains two primary projects developed for **British Airways**:

1. **Ticket Purchasing Prediction Model**: A machine learning model designed to predict whether a customer would purchase a ticket based on historical data and customer behavior patterns.
2. **Customer Sentiment Analysis**: Web-scraped customer reviews analyzed to determine the overall sentiment (positive, negative, or neutral) towards British Airways, providing actionable insights into customer satisfaction.

---

## Ticket Purchasing Prediction Model

### Dataset
- **Source**: Historical data of customer interactions with the airline's website, including session duration, pages visited, ticket prices viewed, and other behavioral metrics.
- **Preprocessing**: 
  - Handled missing values using median imputation.
  - Standardized the features using MinMaxScaler.
  - Categorical variables were converted to numerical using one-hot encoding.

### Modeling
- **Algorithms Used**:
  - Logistic Regression
  - Random Forest Classifier
  - XGBoost Classifier
- **Training and Evaluation**:
  - The dataset was split into training (80%) and testing (20%) sets.
  - Used cross-validation to optimize hyperparameters.
  - Metrics evaluated include accuracy, precision, recall, F1 score, and AUC (Area Under the Curve).

### Results
- **Best Performing Model**: Random Forest with an accuracy of **87%** and AUC of **0.92**.
- **Key Features**: 
  - Number of pages visited
  - Session duration
  - Time spent on payment page

---


## Installation

### Prerequisites
- Python 3.8 or higher
- The following Python libraries:
  ```bash
  pip install pandas scikit-learn xgboost nltk vaderSentiment beautifulsoup4 scrapy
  ```

### Clone the Repository
```bash
git clone https://github.com/yourusername/ba-ticket-purchase-sentiment-analysis.git
cd ba-ticket-purchase-sentiment-analysis
```

### Download Dataset
For the **Ticket Purchasing Prediction Model**, use your historical data. Example format of the data:
```csv
customer_id, session_duration, pages_visited, price_viewed, ticket_purchased
1, 120, 5, 300, 1
2, 90, 3, 250, 0
```

For the **Sentiment Analysis**, scrape customer reviews using the provided web scraping script under `/scraper/`.

---

## Usage

### Ticket Purchasing Prediction Model
To train and test the model:
```bash
python train_ticket_prediction.py
```

---

## Contributing

We welcome contributions to enhance the model, improve web scraping, or extend the sentiment analysis! If you would like to contribute:
1. Fork this repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit and push (`git push origin feature-branch`).
5. Open a Pull Request.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

