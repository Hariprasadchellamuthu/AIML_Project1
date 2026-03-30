# SMS Spam Detector 📩 🚨

## Project Overview
This project is an end-to-end Machine Learning text classification model. It uses Natural Language Processing (NLP) to read the text of an SMS message and predict whether it is "Spam" (junk/malicious) or "Ham" (a legitimate message). 

This is a fantastic beginner project for understanding how machines process human language, extract features from text, and apply probabilistic algorithms to make predictions.

## 🛠️ Tech Stack & Tools
* **Language:** Python
* **Data Manipulation:** Pandas
* **Machine Learning Library:** Scikit-Learn (`sklearn`)
* **Environment:** Google Colab / Jupyter Notebook

## 📊 The Dataset
The model is trained on the famous **SMS Spam Collection Dataset**, which contains over 5,500 real, labelled text messages. 
* **Ham (Safe):** ~86% of the dataset.
* **Spam:** ~14% of the dataset.
* The data is formatted with two columns: the label (`spam` or `ham`) and the raw `message` text.

## 🧠 How It Works (The Pipeline)

This project follows a standard Machine Learning pipeline:

1. **Data Loading & Preprocessing:** * The text labels ("ham" and "spam") are converted into binary numbers (0 for ham, 1 for spam) because machine learning models require numerical inputs.
   * The data is split into a **Training Set (80%)** to teach the model and a **Testing Set (20%)** to evaluate its performance on unseen data.
2. **Text Vectorization (TF-IDF):**
   * Computers cannot understand raw English text. We use **TF-IDF (Term Frequency-Inverse Document Frequency)** to convert sentences into a matrix of numbers.
   * TF-IDF highlights words that are frequent in a specific message but rare across the entire dataset (e.g., "WINNER", "URGENT"), which are strong indicators of spam. It also automatically removes common English "stop words" (like *the, is, and*).
3. **Model Training:**
   * The project uses the **Multinomial Naive Bayes** algorithm. This is a highly efficient, probability-based classifier that is widely considered the industry standard for baseline text classification tasks.
4. **Evaluation:**
   * The model predicts the labels for the 20% testing data, achieving high accuracy, precision, and recall.

## 🚀 How to Run the Project

### Option 1: Run in Google Colab (Recommended for Beginners)
1. Open [Google Colab](https://colab.research.google.com/).
2. Create a "New Notebook".
3. Copy the Python code provided in this repository into the cells.
4. Run the cells sequentially (Shift + Enter). No installation is required!

### Option 2: Run Locally
If you want to run this on your own machine, ensure you have Python installed, then install the required libraries:

```bash
pip install pandas scikit-learn
