---
title: "Transformers — Architecture Overview"
date: 2026-04-20
description: Consolidated notes on the transformer architecture, key variants, and where each is used.
categories: topics
tags: transformers architecture deep-learning
---

## Core architecture

A transformer consists of stacked encoder and/or decoder blocks. Each block has two sub-layers:

1. **Multi-head self-attention** — allows each token to attend to all others.
2. **Feed-forward network** — applied independently to each position.

Residual connections and layer normalization wrap each sub-layer.

## Key variants

| Model | Type | Notes |
|---|---|---|
| BERT | Encoder-only | Pre-training via MLM + NSP |
| GPT | Decoder-only | Autoregressive language modelling |
| T5 | Encoder-decoder | Text-to-text framing for all tasks |
| ViT | Encoder-only | Patches as tokens for vision |

## Things still to understand

- Efficient attention variants (Linformer, Performer, Flash Attention).
- How positional encodings differ across models (learned vs. sinusoidal vs. RoPE).
