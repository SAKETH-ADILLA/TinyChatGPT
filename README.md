# TinyChatGPT 🤖

**TinyChatGPT** is a lightweight conversational language model built from scratch using **Python and PyTorch**. The project explores the core architecture and training workflow behind modern autoregressive language models by implementing a decoder-only Transformer and training it on conversational data.

## 🚀 Project Overview

TinyChatGPT implements a custom Transformer-based language model with **multi-head self-attention, causal masking, token embeddings, positional embeddings, feed-forward networks, layer normalization, dropout, and autoregressive text generation**.

The model was trained using the **Persona-Chat dataset** with GPT-2 tokenization. The training pipeline processes conversational data into User/Bot dialogue pairs and trains the model using next-token prediction with the AdamW optimizer.

The implemented configuration uses 4 Transformer layers, 8 attention heads, a 256-dimensional embedding size, and a context length of 128 tokens. The resulting model contains approximately **28.97 million parameters**.

## ✨ Features

* Custom decoder-only Transformer architecture
* Multi-head causal self-attention
* Token and positional embeddings
* Autoregressive text generation
* Persona-Chat conversational training
* GPU and multi-GPU training support
* GPT-2 tokenizer integration
* Hugging Face GPT-2 format conversion
* GGUF export for lightweight inference experiments
* Model validation through logit comparison and top-1 agreement

## 📊 Training Results

The model was trained for **3,000 iterations**. Training loss decreased from **10.9852 to 2.8229**, while validation loss decreased from **10.9875 to 2.8180**.

A sample generation produced:

```text
User: hi im Inshadh
Bot: hi how are you today ?
```

## 🧠 Model Architecture

```text
Input Text
    ↓
GPT-2 Tokenizer
    ↓
Token + Positional Embeddings
    ↓
Transformer Blocks × 4
    ├── Multi-Head Self-Attention
    ├── Layer Normalization
    └── Feed-Forward Network
    ↓
Language Model Head
    ↓
Next-Token Prediction
    ↓
Generated Response
```

## 🛠️ Tech Stack

* Python
* PyTorch
* Hugging Face Transformers
* Hugging Face Datasets
* GPT-2 Tokenizer
* CUDA
* GGUF / llama.cpp

## 📦 Model Export

The trained model was converted into **Hugging Face GPT-2 format** and validated against the original PyTorch implementation. The conversion achieved **1.0 top-1 logit agreement** in the validation test.

The model was also exported to **GGUF F16 format** for lightweight deployment and inference experimentation.

## 🎯 Learning Objectives

This project was developed to gain practical experience with:

* Transformer architecture
* Attention mechanisms
* Language-model training
* Tokenization and data preparation
* Autoregressive generation
* Model conversion and deployment
* Hugging Face model formats
* GPU-accelerated training

## ⚠️ Project Scope

TinyChatGPT is an educational and experimental language model designed to demonstrate the fundamentals of Transformer-based conversational AI. Its relatively small size and limited training steps mean it is not intended to compete with production-scale LLMs.

## 👨‍💻 Author

**Saketh Adilla**
