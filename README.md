# Svevo Letters Analysis

## Description

The purpose of this research project is to analyze the epistolary corpus of [Italo Svevo](https://en.wikipedia.org/wiki/Italo_Svevo), one of the great italian novelists of the twentieth century and a pioneer of the psychological novel in Italy. The analysis were performed on the corpus created by Cristina Fenu for her paper __"Sentiment Analysis d'autore: l'epistolario di Italo Svevo"__, published in the proceedings of the 2017 AIUCD Conference.

The analysis was structured in two parts:

- __Topic modeling__ of the italian corpus using latent Dirichlet allocation to extract the main topics contained in the corpus and estimate their association with interlocutors in time.

- __Sentiment analysis__ of the whole corpus using the Word-Emotion Association Lexicon (EmoLex) by [Mohammad & al.](https://aclanthology.info/pdf/W/W10/W10-0204.pdf) to highlight relations between emotive states, topics and interlocutors through time.

This repository is structured as follows:

- The `datasets` folder contains the original letter corpus, and is the location where all subsequent datasets used for our purposes are saved.

- The `results` folder contain plots describing our findings and evaluating the performance of our LDA model in svg and png format.

- The `topic_modeling` notebook contains all the code I used to perform my topic modeling analysis. In the end, it produces a `svevo_with_topics.csv` file containing topics assigned to each letter. Only the 500 italian letters with most separated topics are taken into account.

- The `sentiment_analysis_extraction` notebook generates a `sentiment.csv` file containing the sentiment intensity percentage for all the letters in the original corpus.

- The `sentiment_analysis_evaluation` notebook creates many additional datasets used to evaluate and plot our results.

- The `future_perspectives` notebook contains approaches that were tested for the analysis and finally disregarded for their complexity or their results, but definitely deserve a second look for future utilization.

## Requirements

In order for all the notebooks to work properly, the following requirements should be met.

**Warning:** The code of future_perspectives used to follow the one inside the topic_modeling notebook and was separated later. Because of this, the code won't compile unless it is provided with the right variables and imports. To test it, simply put it back at the end of the topic_modeling notebook.

### Python packages

- `numpy`
- `pandas`
- `gensim`
- `spacy`
- `sklearn`
- `pyLDAvis`
- `matplotlib`
- `seaborn`
- `tqdm`

For the spacy package, the languages should be installed as follows:

`python -m spacy download en`

`python -m spacy download fr`

`python -m spacy download it`

`python -m spacy download de`

### R packages

- `syuzhet`
- `dplyr`
- `pander`

## Results

A short report of the research project will be updated soon, containing some insights about my results.