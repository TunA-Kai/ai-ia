---
title: 'Speech Synthesis'
course: 'Azure AI Fundamentals'
date: 2026-02-23
topic: 'Introduction to AI speech concepts'
tags: [AI, Speech Synthesis, Foundry]
---

# Lecture: Speech Synthesis

## Overview

Speech synthesis—also called text-to-speech (TTS)—converts written text into spoken audio.

## Detailed Notes

### Text normalization: Standardize the text

Text normalization prepares raw text for pronunciation by expanding abbreviations, numbers, and symbols into spoken forms.

### Linguistic analysis: Map text to phonemes

Grapheme-to-phoneme (G2P) conversion maps written letters (graphemes) to pronunciation sounds (phonemes).

Modern G2P systems use neural networks trained on pronunciation dictionaries. These models learn patterns between spelling and sound, handling uncommon words, proper names, and regional variations more gracefully than rule-based systems.

### Prosody generation: Determine pronunciation

Prosody refers to the rhythm, stress, and intonation patterns that make speech sound natural. Prosody generation determines how to say words, not just which sounds to produce.

Transformer-based prosody prediction:

- Input encoding: The transformer receives the phoneme sequence with linguistic features (punctuation, part of speech, sentence structure)
- Contextual analysis: Self-attention mechanisms identify relationships between words
- Prosody prediction: The model outputs predicted values for pitch, duration, and energy at each phoneme
- Style factors: The system considers speaking style (neutral, expressive, conversational) and speaker characteristics

### Speech synthesis: Generate audio

Synthesis process:

- Acoustic feature generation: An acoustic model (often a transformer) converts phonemes and prosody targets into mel-spectrograms—visual representations of sound frequencies over time
- Vocoding: The neural vocoder converts mel-spectrograms into raw audio waveforms (sequences of amplitude values at 16,000-48,000 samples per second)
- Post-processing: The system applies filtering, normalization, or audio effects to match target output specifications

## Examples

When you request speech synthesis for "Dr. Chen's appointment is at 3:00 PM":

- Text normalization expands it to "Doctor Chen's appointment is at three o'clock P M"
- Linguistic analysis converts it to phonemes: /ˈdɑktər ˈtʃɛnz əˈpɔɪntmənt ɪz æt θri əˈklɑk pi ɛm/
- Prosody generation predicts pitch rising slightly on "appointment", a pause after "is", and emphasis on "three"
- Speech synthesis generates an audio waveform matching those specifications

## Resources

- Links to additional reading
- External references
- Relevant documentation
