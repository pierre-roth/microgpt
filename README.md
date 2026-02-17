# The Annotated Transformer: microgpt

This repository is an educational, annotated presentation of Andrej Karpathy's `microgpt.py`: a dependency-free, single-file GPT implementation introduced on **February 12, 2026**.

The goal of this project is to keep the algorithmic core intact while making the Transformer mechanics explicit and readable. Think of it as an "Annotated Transformer" edition of microgpt.

## What's in this repo

- `microgpt.py`: the compact pure-Python implementation (dataset, tokenizer, autograd, GPT-2-like model, Adam, training loop, inference loop).
- `index.html`: a dark-mode walkthrough of the code with section-by-section explanations and rewritten snippets for clarity.

## Why microgpt matters

Karpathy's key framing is:

> "This file is the complete algorithm. Everything else is just efficiency."

`microgpt.py` strips LLMs down to essentials:

1. Dataset of documents (names by default)
2. Character tokenizer + BOS token
3. Scalar autograd engine (`Value`)
4. GPT-style Transformer forward pass (attention + MLP + residual stream)
5. Cross-entropy training objective + Adam optimization
6. Autoregressive sampling for inference

## Quick start

Run training and sampling:

```bash
python3 microgpt.py
```

Notes:

- No external dependencies are required.
- `input.txt` is downloaded automatically on first run if missing.
- The script prints training loss and then generates sampled names.

## Website

The annotated website entrypoint is:

- `index.html`

You can open it directly in a browser locally, or publish it via GitHub Pages from the repository root.

## Context and references

- Karpathy's microgpt page: [https://karpathy.ai/microgpt.html](https://karpathy.ai/microgpt.html)
- Dataset source used by default (`names.txt`): [https://github.com/karpathy/makemore](https://github.com/karpathy/makemore)
- Related progression of ideas: `micrograd`, `makemore`, `nanoGPT`
