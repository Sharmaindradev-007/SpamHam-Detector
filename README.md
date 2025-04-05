# SpamHam-Detector
# 📧 Spam Detector: Classifying Messages as Spam or Ham Using Machine Learning

This project aims to classify text messages/emails as **Spam** or **Ham** using **Natural Language Processing (NLP)** and **Machine Learning** techniques. It uses TF-IDF vectorization and Logistic Regression for classification and includes data visualization and model evaluation.

---

## 📁 Dataset

The dataset used is a CSV file containing labeled messages with the following columns:

- `label`: Message type – `spam` or `ham`
- `text`: The content of the message
- `label_num`: Numerical encoding of label (1 for spam, 0 for ham)

---

## 📊 Exploratory Data Analysis & Visualization

- Count plot of spam vs ham
- Histogram of message lengths
- Bar plots of most frequent words in spam and ham
- Word clouds (optional)
- Confusion matrix for model evaluation

---

## 🧠 Machine Learning Workflow

1. **Preprocessing**  
   - Cleaned and explored the data
   - Extracted features using `TF-IDF Vectorizer`

2. **Model Building**  
   - Split the dataset (80% train / 20% test)
   - Applied `Logistic Regression`

3. **Evaluation**  
   - Accuracy score
   - Classification report (precision, recall, F1-score)
   - Confusion matrix

---

## 🧪 Example Prediction

```python
def predict_email(text):
    text_vectorized = vectorizer.transform([text])
    prediction = model.predict(text_vectorized)[0]
    return "Spam" if prediction == 1 else "Ham"

# Example:
new_email = "Get cheap watches and discount medicines now!"
print(predict_email(new_email))  # Output: Spam
