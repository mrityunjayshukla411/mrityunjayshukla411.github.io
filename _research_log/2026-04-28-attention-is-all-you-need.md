---
title: "Attention Is All You Need"
date: 2026-04-28
description: Notes on the original transformer paper by Vaswani et al. (2017).
categories: papers
tags: transformers nlp attention
---

## Citation

Vaswani et al., "Attention Is All You Need", NeurIPS 2017.

## Key ideas

- Replaces recurrence and convolutions entirely with self-attention.
- Multi-head attention lets the model jointly attend to information from different representation subspaces.
- Positional encodings (sinusoidal) inject sequence order since there is no recurrence.
- Encoder-decoder architecture with cross-attention between the two.

## What I found interesting

The scaling factor $$\frac{1}{\sqrt{d_k}}$$ in the attention formula prevents dot products from growing too large in high dimensions, which would push softmax into low-gradient regions.

## Open questions

- How sensitive is performance to the specific positional encoding scheme?
- What breaks first as sequence length grows?
