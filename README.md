# POC AI Projects

## Medical text classification (NLP, Natural Language Processing)

Dataset used: [PubMed 200k RCT](https://github.com/Franck-Dernoncourt/pubmed-rct)

Total 200k and 20k data available in dataset, 20k dataset used for this project

With feature engineering required data extracted from text, as a target, text, line number, total lines and converted into dictionary and data frame
Data are converted to numpy with one hot encoding, with different depth size

"Universal Sentence Encoder" used as a embedding layer, downloaded from the tensorflow hub

Character vectorization used with TextVectorization

Multiple input created with model and concatenate for final input, (Inputs are Sentence embedding, Char embeddings, Line number of sentence, Total line number of the text)

Data used as a tensor slices as a Prefetch Dataset (tf.data.Dataset)

Only 10% data used to fit and validate the model

Evaluation of the model is as below,
- Accuracy = 0.83
- Precision = 0.83
- Recall = 0.83
- F1-score = 0.83

Above accuracy can be increase. by using all 20k data (as only 10% used for the project) or using full data set with 200k data, also by adding some more layers to the model

