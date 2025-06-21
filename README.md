# 🌟 Hotel Review Sentiment Analyzer

This project uses machine learning and natural language processing to analyze hotel customer reviews. It predicts review sentiment (Positive or Negative) and identifies key service-related topics like **"room service"**, **"food quality"**, and **"cleanliness"**. The final output is a structured CSV report ready for business insights.

---

## 📌 Project Overview

**Goal**:  
- Predict customer sentiment (Positive/Negative)  
- Identify frequently mentioned service-related topics  
- Generate an actionable, clean CSV report  

**Data Source**:  
- Reviews and ratings stored as CSV in **IBM Cloud Object Storage**

---

## 🧠 Features

- ✅ Sentiment classification using Logistic Regression  
- ✅ TF-IDF vectorization for text feature extraction  
- ✅ Topic tagging using keyword-based matching  
- ✅ CSV report generation for easy analysis  

---

## 🛠️ Technologies Used

| Category            | Tools & Technologies                         |
|---------------------|----------------------------------------------|
| Language            | Python                                       |
| Libraries           | `pandas`, `scikit-learn`, `TfidfVectorizer`, `ibm_boto3` |
| ML Model            | Logistic Regression                          |
| Text Processing     | TF-IDF Vectorization                         |
| Cloud Storage       | IBM Cloud Object Storage                     |
| Output Format       | CSV (Excel-friendly)                         |
| Authentication      | IBM IAM (via API Key)                        |

---

## 📂 Workflow

1. **Data Collection**  
   - Load reviews and ratings from a cloud-hosted CSV.

2. **Preprocessing**  
   - Remove missing values and filter valid sentiment ratings (1 or -1).  
   - Normalize text (convert to lowercase).

3. **Model Training**  
   - Train a Logistic Regression classifier using TF-IDF features.

4. **Sentiment Prediction**  
   - Predict sentiment for each review and label it as "Positive" or "Negative".

5. **Topic Extraction**  
   - Use keyword matching to tag topics like `"room service"` or `"clean"`.

6. **Report Generation**  
   - Output the results into a well-structured CSV file:
     - `Review`
     - `Predicted Sentiment`
     - `Topics Mentioned`

7. **CSV Preview**

```python
import pandas as pd

csv_preview = pd.read_csv("review_sentiment_topic_report.csv")
print("Preview of the generated CSV:")
print(csv_preview.head())

📊 Sample Output
Below is a preview of how the final CSV output looks. It contains each customer review, the predicted sentiment, and the topics mentioned within the review:

| Review                                           | Predicted Sentiment | Topics Mentioned       |
|--------------------------------------------------|----------------------|-------------------------|
| The food quality was amazing!                    | Positive             | food quality            |
| Room service was slow and disappointing.         | Negative             | room service            |
| Loved the location and clean environment.        | Positive             | location, clean         |
| Customer service was poor and unhelpful.         | Negative             | customer service        |
| Great staff, clean rooms, and delicious food.    | Positive             | clean, food quality     |

📄 review_sentiment_topic_report.csv
├── Review
├── Predicted Sentiment
└── Topics Mentioned



Feel free to connect if you’d like to improve or extend the project.
Happy analyzing! 🚀
