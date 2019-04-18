# Results

The folder contains all the plots and graphs produced during my analysis. A brief explanation of each will follow:

* The `coherence` folder contains three plots of the coherence scores for the LDA model with different number of topics, respectively for the 10 topics version (filtered and unfiltered dictionary) and for the 40 topics version.

* The `silhouette` folder contains three plots of the silhouette scores for the LDA model with different number of topics, respectively for the 10 topics version (filtered and unfiltered dictionary) and for the 40 topics version. The plots of the progressive silhouette with different number of topics are also presented.

* The `svg` folder contains the svg version of some images presented in the main folder.

* `posneg_year.png` shows the variation of positive and negative sentiment over time in the corpus. We see a positive peak in years of literary success (after 1922) and a negative one when many familly members die (end of 1800).

* `sentiment_topic.png` shows relations between sentiment and topics. Interesting to note how positive-negative distance is highest in literature topic, lowest in health topic.

* `sentiment_year.png` is a more elaborated version of `posneg_year.png`, containing the variation of all sentiment classes over time.

* `svevo_corpus_sentiment_posneg.png` shows relations between positive-negative sentiment and top receivers in the corpus. Evident how family members are associated to higher negativity in general, while conversation with literary collaborators is mostly positive.

* `svevo_corpus_sentiment_all.png` is a more elaborated version of `svevo_corpus_sentiment_posneg.png` in which all sentiment classes are taken into account.

* `svevo_corpus_topics.png` is an alluvional graph produced with [RAWGraphs](http://app.rawgraphs.io/) to show the relation between topics, years and interlocutors. Each line represents a letter: on the left side of the graphs, lines are colored with respect to the prevalent topic included in each letter (e.g. a letter which talks mostly about family will be colored in orange), while on the right side we colored the letters based on different periods in Svevo's life: in `red`, the years where many of his family members die from various illnesses, in `purple` the years where Svevo starts working for the Veneziani family, in `green` the years where Svevo travels abroad (mostly to London) for work and in `blue` the years of literary success. We see a coherent matching between the two sides of the graph, which suggests the effectiveness of this approach.

* `svevo_corpus_topics_square.png` is a square, more compressed version of the previous graph.

* `svevo_word_vectors.png` is a low-dimensional depicting of word embeddings provided by ItaliaNLP Lab associated to words contained in the corpus dictionary, with topical words highlighted in different colors.