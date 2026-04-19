# Seq2seq Model

A sequence-to-sequence deep learning model implementation.

## Overview

This project implements a sequence-to-sequence (seq2seq) model, which is commonly used for tasks such as machine translation, text summarization, and question answering.

## Features

- Encoder-decoder architecture
- Attention mechanism support
- Customizable model parameters

## Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/MohitKhetan10/Seq2seq_model.git
cd Seq2seq_model
pip install -r requirements.txt
```

Seq2Seq with Attention – Assignment 6
📘 Overview
This project demonstrates the Sequence‑to‑Sequence (Seq2Seq) model with Attention mechanism using Python and NumPy. The goal is to show how encoder–decoder architectures work in practice, and how attention improves translation quality by allowing the decoder to dynamically focus on relevant parts of the input sequence.

The code simulates a real‑life use case: translating English sentences and paragraphs into French. Outputs are explained in detail so that even non‑technical readers can understand what is happening step by step.

⚙️ Components
1. Encoder
Processes the input sequence (English words).

Produces hidden state vectors for each word.

Each vector captures semantic meaning and context.

2. Decoder
Generates the output sequence (French words).

Maintains its own evolving hidden state.

Uses encoder information + context to predict words.

3. Attention Mechanism
Calculates alignment scores (dot product similarity between decoder state and encoder states).

Applies softmax to convert scores into probabilities (focus percentages).

Builds a dynamic context vector (weighted sum of encoder states).

Concatenates decoder state + context vector → predicts next word.

🧩 Code Structure
softmax(x): Helper function to normalize scores into probabilities.

encoder_states: Array of vectors representing input words.

decoder_state: Current hidden state of the decoder.

raw_scores: Alignment scores between decoder and encoder states.

attention_weights: Focus percentages for each input word.

dynamic_context_vector: Weighted summary of input tailored to decoder needs.

final_input: Combined vector used for prediction.

interpretation section: Human‑readable explanation of outputs.

📖 Real‑Life Use Case
The project simulates translation of:

Sentence: “I love machine learning” → “J’aime l’apprentissage automatique”

Paragraph: “Artificial Intelligence is transforming the world…” → French equivalent.

At each step:

The decoder calculates which English words are most relevant.

Attention weights show focus distribution (e.g., 46% on “love”).

The context vector emphasizes those words.

The decoder predicts the correct French word or phrase.

📝 Example Output (Layman’s Explanation)
Code
Step 1: Calculating similarity between Decoder and each Encoder word...
Similarity with 'I': 0.19
Similarity with 'love': 1.30
Similarity with 'machine': 0.04
Similarity with 'learning': 0.70

Attention Weights (%):
[I: 15.2%, love: 46.3%, machine: 13.1%, learning: 25.4%]

Dynamic Context Vector: [0.56, 0.12, 0.42]

Interpretation:
The decoder focused most on 'love' and 'learning'.
It predicted the French word: "J’aime".
✅ Conclusion
This project provides:

A clear implementation of Seq2Seq with Attention.

Step‑by‑step outputs with technical and layman explanations.

A real‑life translation use case demonstrating how modern NLP systems work.

## Contributing

Contributions are welcome! Please feel free to submit a pull request.
