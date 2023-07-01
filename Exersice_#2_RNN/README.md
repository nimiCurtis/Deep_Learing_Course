# Exercise Overview

The report provides an overview of Exercise 2 in the Deep Learning course. The exercise focuses on Recurrent Neural Networks (RNNs) and covers theoretical concepts as well as practical training sessions. The theoretical section addresses topics such as sequence truncation and padding, advantages of Gated Recurrent Units (GRU) over Long Short-Term Memory (LSTM), parameter calculation for GRU, and gradients of GRU for backpropagation. In the practical section, a regularized LSTM neural network was trained and compared different configurations, including LSTM with and without dropout, and GRU with and without dropout. The experiments were evaluated using convergence graphs and a final loss table. The results showed that regularized configurations generally performed better, with LSTM achieving lower loss values compared to GRU. Adjusting the learning rate improved the performance of GRU. Overall, the exercise provides a comprehensive exploration of RNNs and their applications in deep learning.

---

# Practical Part - RNN for Next Word Prediction

This repository contains an implementation of LSTM and GRU architectures by Zaremba for predicting the next word using the Penn Tree Bank dataset in natural language processing.

## Dataset
The Penn Tree Bank dataset consists of annotated sentences from the Wall Street Journal and is widely used in the field of natural language processing.

## Model
The implemented model utilizes the LSTM architecture by Zaremba for predicting the next word in the Penn Tree Bank dataset. The model consists of an embedding layer, followed by two LSTM blocks, and finally fully connected layers.

## Usage
To run the code, follow these steps:

1. Set the relevant paths:
   - Models directory.
   - Plots directory (optional, if you want to visualize convergence graphs).
   - Data directory.

2. Choose whether to train or load a pre-trained model:
   - To load a trained model and test it, set the flag to 1.
   - To train a new model, set the flag to 0.

3. Select the desired method from the following options:
   - 'LSTM_without_dropout'
   - 'LSTM_with_dropout'
   - 'GRU_without_dropout'
   - 'GRU_with_dropout'

   Modify the code in the 'For the Instructor' cell accordingly.

4. Click on 'Run all' or press ctrl+F9 to execute the code.

## Results
The model's final accuracy on the training and test datasets is printed below each graph. The perplexity values for each model variant are as follows:

- LSTM without dropout:   train perplexity: 39.25 | validation perplexity: 119.85 | test perplexity: 115.73
- LSTM with dropout:      train perplexity: 43.80 | validation perplexity: 96.59  | test perplexity: 92.67
- GRU without dropout:    train perplexity: 34.40 | validation perplexity: 134.39 | test perplexity: 129.95
- GRU with dropout:       train perplexity: 42.22 | validation perplexity: 101.53 | test perplexity: 97.452

## Inference
At the end of the code, there are additional cells that display the data and the transition to the tensor. An example is provided where a trained model predicts the next word in a given sentence.
