# Svevo Letters Analysis

## News

* The project was presented at [2019 AILC Lectures on Computational Linguistics](http://www.ai-lc.it/lectures-2019-it/)! The poster created for the presentation is available [here](https://github.com/gsarti/svevo-letters-analysis/blob/master/svevo_poster.pdf).

## Description

The purpose of this research project is to analyze the epistolary corpus of [Italo Svevo](https://en.wikipedia.org/wiki/Italo_Svevo), one of the great italian novelists of the twentieth century and a pioneer of the psychological novel in Italy. The analysis were performed on the corpus created by Cristina Fenu as final project work for the [Masters in Digital Humanities](https://www.unive.it/pag/9180/) of Università Ca' Foscari of Venice during academic year 2015-2016.

Results of the first analysis were published in the proceedings of the [2017 AIUCD Conference](http://amsacta.unibo.it/5885/1/AIUCD_2017_BoA.pdf) and are available on the website of the [Svevian Museum of Trieste](http://www.museosveviano.it/ar/progetto/archivio-digitale/ ).

The analysis was structured in two parts:

- __Topic modeling__ of the italian corpus using latent Dirichlet allocation to extract the main topics contained in the corpus and estimate their association with interlocutors in time.

- __Sentiment analysis__ of the whole corpus using the Word-Emotion Association Lexicon (EmoLex) by [Mohammad & al.](https://aclanthology.info/pdf/W/W10/W10-0204.pdf) to highlight relations between emotive states, topics and interlocutors through time.

This repository is structured as follows:

- The `datasets` folder contains the original letter corpus, and is the location where all subsequent datasets used for our purposes are saved. **New:** Added positive/negative sentiment italian wordlist for recurrent words connotation analysis.

- The `results` folder contain plots describing our findings and evaluating the performance of our LDA model in svg and png format.

- The `topic_modeling` notebook contains all the code I used to perform my topic modeling analysis. In the end, it produces a `svevo_with_topics.csv` file containing topics assigned to each letter. Only the 500 italian letters with most separated topics are taken into account.

- The `sentiment_analysis_extraction` notebook generates a `sentiment.csv` file containing the sentiment intensity percentage for all the letters in the original corpus.

- The `sentiment_analysis_evaluation` notebook creates many additional datasets used to evaluate and plot our results.

- **New:** The `recurrent_words_connotation_analysis` notebook is used to inspect which words are the cause of most positive/negative sentiment over Svevo lifespan.

- The `future_perspectives` notebook contains approaches that were tested for the analysis and finally disregarded for their complexity or their results, but definitely deserve a second look for future utilization.

## Requirements

In order for all the notebooks to work properly, the following requirements should be met.

**Warning:** The last part of future perspective notebook will not function out-of-the-box. See additional requirements below and notebook for more information on this topic.

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

Simply run `pip install -r requirements.txt` inside this folder to automatically install all dependencies.

For the spacy package, the languages should be installed as follows:

`python -m spacy download en`

`python -m spacy download fr`

`python -m spacy download it`

`python -m spacy download de`

### R packages

- `syuzhet`
- `dplyr`
- `pander`

Run `install.packages("syuzhet", "dplyr", "pander")` inside a R shell.

### Additional requirements for Future Perspectives notebook

The set of italian embeddings necessary to test the Word2Vec approach in `future_perspectives` is available on the [Italian NLP Lab](http://www.italianlp.it/resources/italian-word-embeddings/) website.

## Results

A short report of the research project has been updated and is available! The last section contains a textual description of our findings. For a visual understanding, please refer to the results folder.
