# Lyrics Classification With BERT

## Introduction

This project classifies song lyrics into different genres using BERT (Bidirectional Encoder Representations from Transformers). BERT is a transformer-based model that has achieved state-of-the-art results in a wide range of NLP tasks.

## Dataset

The dataset for this classfication task has been obtained from [kaggle](https://www.kaggle.com/datasets/nikhilnayak123/5-million-song-lyrics-dataset/data). It consists of a vast collection of songs' lyrics and one of 6 unique genre for each song.

## Installation

Make sure to have [python-poetry](https://python-poetry.org/) installed. A computer with adequate GPU is recommended.

```shell
poetry install
```

## Usage

Each of the notebooks represent a specific checkpoint in the process. Before running the model, make sure to store the dataset in the following folder structure :

```
lyrics_classification/
├── datasets/
│   ├── test-lyrics/
│   └── ds2.csv
└── pickles/
```

Notebooks :

1. **Dataset Exploration** - Consists of simple explorations of the dataset.
1. **Dataset Preprecessing** - Producing a sampled subset and pre-processing.
1. **Model Training** - Training the model on preprocessed sample for 3 epochs using BERT base
1. **Model Inference** - Place a text file containing lyrics of a song in the `test_lyrics` folder for testing on any song of your choice.

## Results

After 3 epochs of training the model on approximately 50,000 instances per label, the following results were achieved :

```
              precision    recall  f1-score   support

     country       0.90      0.98      0.94       974
        misc       0.99      0.92      0.95      1075
         pop       0.90      0.77      0.83       994
         rap       0.96      0.93      0.95       956
          rb       0.79      0.93      0.85       972
        rock       0.91      0.90      0.91      1029

    accuracy                           0.91      6000
   macro avg       0.91      0.91      0.90      6000
weighted avg       0.91      0.91      0.91      6000
```
