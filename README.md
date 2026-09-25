# IMDb-Sentimental-Analysis-RNN

A Deep Learning project using Recurrent Neural Networks (RNN) with LSTM to classify IMDb movie reviews as Positive or Negative.

# IMDb Movie Review Sentiment Analysis using RNN

## Project Overview

This project applies Deep Learning techniques to classify IMDb movie reviews using a Recurrent Neural Network (RNN) with an LSTM layer.

The model is built using TensorFlow/Keras to learn the sequential relationships between words in movie reviews and classify them into two categories:

- Positive
- Negative

The project includes data preprocessing, sequence padding, LSTM model development, model training, evaluation, and prediction on new movie reviews.

## Project Objective

The objective of this project is to develop an LSTM-based sentiment analysis model that can automatically identify whether a movie review expresses a positive or negative sentiment.

The model learns patterns and relationships between words in the reviews during training.

## Dataset

The project uses the IMDb Movie Review Dataset.

The dataset contains:

- 25,000 training reviews
- 25,000 testing reviews
- Two classes:
  - Positive
  - Negative

The IMDb dataset is loaded using TensorFlow/Keras.

The dataset is already converted into numerical sequences, where each number represents a word.

## Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the IMDb dataset.
2. Limited the vocabulary to 10,000 words.
3. Converted reviews into numerical sequences.
4. Padded the sequences to a fixed length of 250.
5. Used padding and truncation to make all reviews the same size.
6. Prepared the data for LSTM model training.

## Sequence Padding

Since movie reviews have different lengths, padding was applied to make all input sequences have the same length.

The maximum sequence length was set to 250.

Padding was added to shorter reviews, while longer reviews were truncated.

This allows the LSTM model to process all reviews with the same input size.

## Recurrent Neural Network

An LSTM-based Recurrent Neural Network was developed using TensorFlow/Keras.

The model architecture includes:

- Input Layer
- Embedding Layer
- LSTM Layer
- Dropout Layer
- Dense Output Layer

The final sigmoid output layer produces a probability used to classify the review as either Positive or Negative.

## Model Architecture

The model follows the structure:

Input
↓
Embedding
↓
LSTM
↓
Dropout
↓
Dense
↓
Positive / Negative

The Embedding layer converts word indexes into dense vector representations.

The LSTM layer learns the sequential relationships between words in the review.

The Dropout layer helps reduce overfitting.

The final Dense layer with sigmoid activation performs binary classification.

## Model Training

The LSTM model was trained using the prepared IMDb training dataset.

The model was compiled using:

- Optimizer: Adam
- Loss Function: Binary Crossentropy
- Evaluation Metric: Accuracy
- Epochs: 5
- Batch Size: 64

During training, a validation set was used to monitor the model's performance.

## Model Evaluation

The trained model was evaluated using the IMDb test dataset.

### Test Performance

- Test Accuracy: 80%
- Test Loss: 0.5

The training and validation accuracy and loss were also visualized using graphs to understand the learning behavior of the model.

## Accuracy Visualization

The training and validation accuracy were plotted to observe how the model performance changed during training.

The accuracy graph helps to compare the model's performance on training and validation data.

## Loss Visualization

The training and validation loss were plotted to understand how the prediction error changed during training.

The loss graph helps to identify the learning behavior of the model.

## Prediction

The trained LSTM model can be used to classify a new movie review.

A new review is:

1. Converted into lowercase text.
2. Converted into numerical word indexes.
3. Padded to the required sequence length.
4. Passed to the trained LSTM model.
5. Classified as either Positive or Negative.

Example:

"This movie was amazing and I really enjoyed it."

Output:

Positive

## Classification Metrics

The model performance was evaluated using standard classification metrics:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

These metrics provide a better understanding of how well the model classifies positive and negative reviews.

## Results

The LSTM model successfully learned the sequential patterns in IMDb movie reviews.

The model achieved approximately **80% accuracy on the test dataset**.

The results show that LSTM-based Recurrent Neural Networks can be used effectively for binary sentiment classification of text data.

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## Conclusion

This project demonstrates how Recurrent Neural Networks with LSTM can be used for text classification and sentiment analysis.
The LSTM model learned the sequential relationships between words in IMDb movie reviews and classified them as positive or negative.
The model achieved approximately 80% test accuracy and was evaluated using accuracy, precision, recall, F1-score, and confusion matrix.
Overall, the project shows how deep learning can be applied to automatically understand the sentiment of movie reviews.
