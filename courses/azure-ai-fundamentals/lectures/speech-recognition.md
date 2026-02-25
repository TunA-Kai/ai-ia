---
title: 'Speech Recognition'
course: 'Azure AI Fundamentals'
date: 2026-02-23
topic: 'Introduction to AI speech concepts'
tags: [AI, Speech Recognition, Foundry]
---

# Lecture: Speech Recognition

## Overview

Speech recognition, also called speech-to-text, enables applications to convert spoken language into written text. The journey from sound wave to text involves six coordinated stages: capturing audio, preparing features, modeling acoustic patterns, applying language rules, decoding the most likely words, and refining the final output.

## Detailed Notes

### Audio capture: Convert analog audio to digital

System samples the analog audio signal at a high frequency (e.g., 16 kHz) and stores each measurement as a numerical value, creating a digital representation of the sound wave.

System applies noise reduction techniques to filter out background sounds and enhance the clarity of the speech signal.

### Pre-processing: Extract meaningful features

Raw audio = too much information.
Transform waveform into a more compact representation that captures important characteristics of the sound.

MFCCs (Mel-Frequency Cepstral Coefficients) are commonly used features that represent the short-term power spectrum of sound, mimicking human auditory perception.

- Divide audio into frames
- Apply Fourier transform
- Map to mel scale
- Extract coefficients

The result is a sequence of feature vectors -one per frame- that serve as input to the acoustic model.

### Acoustic modeling: Recognize phonemes

The acoustic model learns to associate patterns in the feature vectors with phonemes, which are the basic units of sound in a language.

Modern acoustic models often use deep neural networks (DNNs) to capture complex relationships between features and phonemes, improving recognition accuracy.

### Language modeling: Predict word sequences

Language models resolve ambiguity by applying knowledge of vocabulary, grammar and common word patterns. It guides word sequences by apply:

- Statistical patterns
- Context awareness
- Domain adaptation

### Decoding: Select the best text hypothesis

Decoding algorithms search through possible combinations of phonemes and words to find the most likely transcription based on the acoustic and language model outputs.

_Beam search_ is a common decoding technique that maintains a set of the most promising hypotheses at each step, balancing accuracy and computational efficiency.

### Post-processing: Refine the output

Post-processing applies formatting rules and corrections.

- Capitalization
- Punctuation
- Number formatting
- Profanity filtering
- Inverse text normalization
- Confidence scoring

## Example

When you say "Call Mom at five":

- Audio capture provides the raw signal.
- Pre-processing extracts MFCC features that highlight speech patterns.
- Acoustic modeling predicts phoneme probabilities using transformer networks.
- Language modeling applies vocabulary and grammar knowledge.
- Decoding searches for the best word sequence.
- Post-processing formats the text for human readers.

## Resources

- [Lecture](https://learn.microsoft.com/en-us/training/modules/introduction-ai-speech/3-speech-recognition?pivots=text)
