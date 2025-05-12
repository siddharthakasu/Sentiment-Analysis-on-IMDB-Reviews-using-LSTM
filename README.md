# 🎬 Sentiment Analysis on IMDB Movie Reviews using LSTM

A deep learning-based Natural Language Processing (NLP) project that uses a Long Short-Term Memory (LSTM) network to perform binary sentiment classification on IMDB movie reviews.

## 📁 Dataset
- Source: [Kaggle – IMDB Dataset of 50K Movie Reviews](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews)
- Total Reviews: 50,000 (25k positive, 25k negative)

## 🚀 Technologies Used
- Python
- TensorFlow & Keras
- NumPy, Pandas
- Scikit-learn
- Natural Language Processing (NLP)

## 🛠️ Features
- Downloaded dataset using Kaggle API and extracted for use.
- Preprocessing pipeline includes:
  - Label encoding (positive → 1, negative → 0)
  - Tokenization of text using Keras Tokenizer
  - Padding sequences for LSTM input compatibility
- LSTM-based model:
  - Embedding Layer: Transforms words into 128-dimensional vectors
  - LSTM Layer: Learns sequential patterns with dropout regularization
  - Dense Output: Sigmoid activation for binary sentiment prediction

## 🧠 Model Architecture
- `Embedding(5000, 128, input_length=200)`
- `LSTM(128, dropout=0.2, recurrent_dropout=0.2)`
- `Dense(1, activation='sigmoid')`

## 📊 Results
- **Test Accuracy**: High accuracy on unseen IMDB reviews after 5 epochs
- Loss and accuracy metrics evaluated on test data

## 💬 Real-Time Prediction
You can input any custom review and get an instant sentiment classification:

```python
"This movie was fantastic. I loved it."
# Output: positive

"This movie was not that good."
# Output: negative
