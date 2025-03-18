# Next-word-predictor

# LSTM Next Word Predictor

A neural language model that predicts the next word in a sequence using Long Short-Term Memory (LSTM) networks.

## Overview

This project implements a text generation model using LSTM architecture to predict the next word in a sequence. The model is trained on a dataset about artificial intelligence and can generate coherent text completions based on a given prompt.

## Features

- LSTM-based language model for next word prediction
- Text preprocessing and tokenization pipeline
- Sequence padding for consistent input dimensions
- Word-level prediction with categorical outputs
- Interactive text generation demonstration

## Implementation Details

### Data Processing

The model uses a text corpus about artificial intelligence as training data. The preprocessing pipeline includes:
1. Tokenizing the text using Keras' Tokenizer
2. Creating input sequences from the tokenized text
3. Padding sequences to a uniform length
4. Preparing X (input) and y (target) data with one-hot encoded outputs

### Model Architecture

```
Model: "sequential"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
embedding (Embedding)        (None, 86, 100)           39600     
_________________________________________________________________
lstm (LSTM)                  (None, 150)               150600    
_________________________________________________________________
dense (Dense)                (None, 396)               59796     
=================================================================
Total params: 249,996
Trainable params: 249,996
Non-trainable params: 0
_________________________________________________________________
```

The model consists of:
- An embedding layer that converts tokenized words into 100-dimensional vectors
- An LSTM layer with 150 units to capture sequential patterns
- A dense output layer with softmax activation for predicting the next word

## Usage



## Requirements

- Python 3.x
- TensorFlow 2.x
- NumPy
- Keras

## Dataset

The model is trained on a 600-word article about artificial intelligence that covers:
- The history and evolution of AI
- Early AI developments
- The AI winter
- Machine learning and deep learning revolution
- Current applications and future trends

## Future Improvements

- Implement larger and more diverse training datasets
- Add temperature parameter for controlling randomness in predictions
- Create a web interface for interactive text generation
- Support for saving and loading trained models
- Implement bidirectional LSTM for improved context understanding

