---
title: 'Large Language Models (LLMs)'
course: 'Azure AI Fundamentals'
date: 2026-02-10
topic: 'Generative AI and agents'
tags: ['LLM', 'Generative AI', 'Azure AI']
---

# Lecture: Large Language Models (LLMs)

## Overview

Fundamentally, LLMs are trained to generate _completions_ based on _prompts_. Think of them as being super-powerful examples of the predictive text feature on many cellphones. A prompt starts a sequence of text predictions that results in a semantically correct completion. The trick is that the model understands the relationships between words and it can identify which words in the sequence so far are most likely to influence the next one; and use that to predict the most probable continuation of the sequence.

## Detailed Notes

### Tokenization

Tokenization is the process of breaking down text into smaller units called tokens. Tokens can be as small as characters or as large as words or subwords. LLMs use tokenization to process and understand text input. Then each token is mapped to a unique numerical identifier, which the model uses during training and inference.

Example: "Hello, world!" => ["Hello", ",", "world", "!"] => [9906, 11, 1917, 0]

### Transforming tokens with a transformer

- Assign each token a vector (initially random). Each vector has multiple numeric _elements_ or _dimensions_ eg. [1,23,46].
- Need to transform initial vectors into new vectors with linguistic and semantic characteristics embedded in them, based on the contexts in which they appear in the training data. New vectors are called _embeddings_.
- Use a transformer model to do this transformation. Consists 2 main components:
  - An _encoder_ that processes the input tokens and generates embeddings by applying technique called _attention_. Multi-head attention evaluate multiple elements of the input vectors in parallel and assign weights to them based on their relevance to the current token being processed.
  - A _decoder_ that takes the embeddings from the encoder and generates the output sequence by predicting the next token based on the context provided by the embeddings.
- The input of transformer also includes _positional encoding_ that provide information about the position of each token in the sequence, helping the model understand the order of words.

## Resources

- [Lecture](https://learn.microsoft.com/en-us/training/modules/fundamentals-generative-ai/3-language-models?pivots=text)
- [Is LLMs just fancy autocomplete?](https://www.reddit.com/r/ArtificialSentience/comments/1nm8hof/just_fancy_autocomplete_can_we_talk_emergent/)
- [Video explaination](https://www.youtube.com/watch?v=LPZh9BOjkQs&list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi&index=5)
