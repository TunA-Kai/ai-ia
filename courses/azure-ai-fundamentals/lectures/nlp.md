---
title: "Introduction to NLP"
course: "Azure AI Fundamentals"
date: 2026-02-22
topic: "Natural Language Processing"
tags: [NLP, AI, Azure]
---

# Lecture: Introduction to NLP

## Detailed Notes

### Tokenization

Tokenization is the process of breaking down text into smaller units called tokens, which can be words, subwords, or characters. This is a fundamental step in NLP as it allows models to process and understand text data.

Pre-processing techniques:

- Text normalization (lowercasing, removing punctuation). For analysis that relies purely on word frequency, this approach improves overall performance but some semantic meaning could be lost. For example, "Apple" (the company) and "apple" (the fruit) would be treated as the same token.
- Stop word removal (removing common words that may not add much meaning, such as "the", "is", "and").
- N-gram extraction (finding multi-term phrases). For example, "New York" would be treated as a single token rather than two separate tokens "New" and "York".
- Stemming (reducing words to their root form). For example, "running", "runner", and "ran" would all be reduced to the root form "run".
- Lemmatization (reducing words to their base or dictionary form). For example, "better" would be reduced to "good", and "running" would be reduced to "run".
- Part-of-speech tagging (identifying the grammatical role of each token). For example, in the sentence "The cat sat on the mat", "cat" would be tagged as a noun, "sat" as a verb, and "mat" as a noun.

### Statistical text analysis

#### Frequency Analysis

- Count the number of times each normalized token appears with the assumption that terms that appear more frequently are more important.

- Term Frequency (TF): Measures how frequently a term appears in a document. For example, if the word "agent" appears 6 times in a document then `tf("agent") = 6`.
- Inverse Document Frequency (IDF): Measures how important a term is across a collection of documents. It is calculated as `idf(t) = log(N / df(t))`, where N is the total number of documents and df(t) is the number of documents containing the term t. For example, if there are 1000 documents and the word "agent" appears in 10 of them, then `idf("agent") = log(1000 / 10) = log(100) = 2`.
- TF-IDF: Combines TF and IDF to give a weight to each term in a document. It is calculated as `tf-idf(t) = tf(t) * idf(t)`. For example, if `tf("agent") = 6` and `idf("agent") = 2`, then `tf-idf("agent") = 6 * 2 = 12`. A hight TF-IDF score indicates that a word appears often in one document but rarely in others. A low score indicates that word is common in many documents and may not be as important for distinguishing between them.

#### "Bag-of-words" machine learning technique

The "bag-of-words" technique represents text as a collection of individual words, disregarding grammar and word order. Each unique word in the text is treated as a feature, and the frequency of each word is used to create a vector representation of the text.

#### TextRank

TextRank is an unsupervised graph-based algorithm that models text as a network of connected nodes. For example, each sentence in a document could be considered a node, and the connections (edges) between them are scored based on the similarity of the words they contain. TextRank is commonly used to summarize text based on identifying a subset of sentences within a document that best represent its overall subject.

The TextRank algorithm works as follows:

1. Build a graph: Each sentence in the document is represented as a node in the graph. Edges that connect them are weighted by similarity (often measured using word overlap or cosine similarity between sentence vectors).
2. Calculate ranks iteratively: Each node's score is calculated based on the scores of the nodes connected to it. The formular is:

```
TextRank(Sᵢ) = (1-d) + d * Σ(wⱼᵢ / Σwⱼₖ) * TextRank(Sⱼ)
```

Where:

- Sᵢ is the sentence being scored.
- d is a damping factor (usually set to 0.85).
- wⱼᵢ is the weight of the edge from sentence j to sentence i.
- Σwⱼₖ is the sum of the weights of the edges from sentence j to all other sentences.

3. Extract top-ranked sentences: After several iterations, the sentences with the highest TextRank scores are selected as the most important sentences in the document, which can be used for summarization or other NLP tasks.

### Semantic language models

Text tokens are often represented as vectors in a high-dimensional space, where the distance between vectors reflects the semantic similarity between the corresponding words. This allows models to capture relationships between words based on their context and usage in language.

Calculate the cosine similarity between pairs of vectors:

```
cosine_similarity(A, B) = (A · B) / (||A|| * ||B||)
```

Where:

- A and B are the vector representations of two words or sentences.
- A · B is the dot product of the two vectors.
- ||A|| and ||B|| are the magnitudes (lengths) of the vectors

## Resources

- [Lecture](https://learn.microsoft.com/en-us/training/modules/introduction-language/)
