# Text Emotion Detection

A Streamlit web application that predicts the underlying emotion of a given text. This project uses a pre-trained natural language processing (NLP) model to classify text into various emotional categories and provides a confidence score alongside a breakdown of all prediction probabilities.

---

## Project Overview

This application takes raw text input from the user and passes it through a machine learning pipeline (saved as a `.pkl` file) to classify the dominant emotion. 

**Supported Emotions:**
* Anger 😠
* Disgust 🤮
* Fear 😨
* Happy/Joy 🤗 / 😂
* Neutral 😐
* Sad/Sadness 😔
* Shame 😳
* Surprise 😮

---

## File Structure

* `app.py`: The main Streamlit application script containing the frontend UI and prediction logic.
* `emotion_dataset.csv`: The dataset containing raw text examples and their corresponding emotion labels, used for training the model.
* `text_emotion.pkl`: The serialized scikit-learn machine learning pipeline (CountVectorizer + Classifier) used to make the predictions.

---

## Prerequisites

To run this application locally, you will need Python installed on your machine along with the following libraries:

* `streamlit`
* `pandas`
* `numpy`
* `altair`
* `joblib`
* `scikit-learn`

---

## Installation and Setup

**1. Clone or download the repository**
Ensure all three files (`app.py`, `emotion_dataset.csv`, `text_emotion.pkl`) are in the same directory. Note: `app.py` expects the model to be in a `model/` folder by default based on the code (`open("model/text_emotion.pkl", "rb")`). You may need to create a `model` directory and place the `.pkl` file inside it, or update the path in `app.py` to `open("text_emotion.pkl", "rb")`.

**2. Install dependencies**
Open your terminal or command prompt and install the required packages:
```bash
pip install streamlit pandas numpy altair joblib scikit-learn
