# Spam Detection System 

This repository contains a simple yet effective end-to-end Machine Learning application that classifies SMS messages as either **Spam** or **Not Spam**. The project uses a Naive Bayes classifier and features a clean, web-based user interface built with Streamlit.

##  Project Overview
In the modern digital age, filtering unwanted communication is essential. This tool automates the process of identifying spam by analyzing word patterns and frequencies within messages. By training on a dataset of labeled SMS messages, the model can accurately distinguish between legitimate conversations and promotional or fraudulent content.

##  Real-World Applications
This application is a foundational example of how Natural Language Processing (NLP) is used in industry. Some practical use cases include:

* **Email Filtering:** Automatically diverting promotional offers, phishing attempts, and "get rich quick" schemes into a separate folder to keep the primary inbox clean.
* **SMS & Messaging Security:** Telecommunication companies use similar logic to block fraudulent texts or "smishing" (SMS phishing) attacks before they reach the user.
* **Content Moderation:** Social media platforms and comment sections use these classifiers to filter out bot-generated spam, keeping discussions relevant and safe.
* **Customer Support Automation:** Businesses use text classification to sort incoming customer queries into "Urgent," "Feedback," or "Spam," ensuring that human agents focus on real issues.

##  Key Features
* **Automated Data Cleaning:** Removes duplicate entries and standardizes labels for higher model reliability.
* **Natural Language Processing:** Utilizes `CountVectorizer` to handle text preprocessing and stop-word removal.
* **Fast & Accurate:** Implements the **Multinomial Naive Bayes** algorithm, which is highly efficient for text-based classification tasks.
* **Interactive Dashboard:** A user-friendly interface that allows for real-time testing and validation.

## 🛠️ Technical Stack
* **Python:** Core programming language.
* **Pandas:** For data manipulation and analysis.
* **Scikit-Learn:** For machine learning model training and text vectorization.
* **Streamlit:** For building and deploying the web application.

##  Dataset
The model is trained using a `spam.csv` file which includes:
- **Category:** The label (ham/spam).
- **Message:** The actual text content of the SMS.

##  How to Run the Project

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/your-username/spam-detection.git](https://github.com/your-username/spam-detection.git)
    cd spam-detection
    ```

2.  **Install Requirements:**
    ```bash
    pip install pandas scikit-learn streamlit
    ```

3.  **Run the Application:**
    ```bash
    streamlit run spamDetection.py
    ```

##  Model Logic
1.  **Vectorization:** The raw text is converted into a matrix of token counts. We filter out common English stop words (like 'and', 'the', 'is') to focus on the words that actually define "spam" behavior.
2.  **Training:** The data is split into an 80/20 ratio. The model learns from the 80% and validates its accuracy on the remaining 20%.
3.  **Prediction:** The user input is transformed using the same vocabulary as the training set and then passed through the classifier to generate a result.

---
*Developed as part of an AI and ML Project.*
