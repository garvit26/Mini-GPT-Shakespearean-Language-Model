# Mini-GPT: Shakespearean Language Model 🎭

A lightweight, decoder-only Transformer model built from scratch in PyTorch. This project is based on Andrej Karpathy's "Let's Build GPT" tutorial and demonstrates the core architecture behind modern Large Language Models (LLMs), trained on the Tiny Shakespeare dataset.

## 🚀 Project Overview

This repository contains an implementation of a character-level Generative Pre-trained Transformer (GPT). It learns to generate text in the style of Shakespeare by predicting the next character in a sequence. Despite its small size (~0.21M parameters), it successfully captures the structure of play scripts, including character names and dialogue formatting.

## 🧠 Architecture

The model is a **Decoder-only Transformer** consisting of the following components:

* **Tokenization:** Character-level encoding (Vocab size: 65).
* **Embeddings:** Learned token embeddings + Positional embeddings.
* **Self-Attention:** Multi-Head Causal Self-Attention allows the model to attend to past tokens while masking future ones.
* **Transformer Blocks:** A stack of 4 blocks, each containing:
    * Layer Normalization (Pre-Norm)
    * Multi-Head Attention
    * Feed-Forward Network (MLP) with Residual Connections
* **Optimization:** Trained using the AdamW optimizer with cross-entropy loss.

### Model Stats
* **Parameters:** ~210,000
* **Context Length:** 32 characters
* **Embedding Dimension:** 64
* **Layers:** 4
* **Heads:** 4

