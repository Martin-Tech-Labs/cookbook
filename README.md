# cookbook

An educational, hands-on repository about how mathematical systems shape computation and interpretation, especially for language models and probability.

## Overview

This repository explores:
- logits, probabilities, and log probabilities
- softmax and sigmoid
- cross-entropy and perplexity
- log-space arithmetic and joint probability
- the log semiring on graphs
- logarithmic scales such as decibels
- custom algebra systems and how changing the rules changes behavior
- practical use of logprobs in LLM workflows, including RAG-style comparisons

The emphasis is on intuition, small runnable examples, and visualizations.

## Tech stack

- Python
- Jupyter notebooks
- PyTorch
- Hugging Face Transformers
- matplotlib

The notebooks use a small CPU-friendly causal language model from Hugging Face.

## Repository structure

- `README.md`
- `requirements.txt`
- `notebooks/`

Each notebook is designed to:
- run independently
- explain ideas in markdown before code
- include visualizations where useful
- stay simple and direct

## Notebooks

1. `01_logits_logprobs_softmax.ipynb`
   - logits
   - softmax
   - sigmoid
   - probabilities vs log probabilities
   - converting logprob to probability with `exp`
   - token-level examples from a small language model

2. `02_cross_entropy_perplexity.ipynb`
   - negative log likelihood
   - cross-entropy loss
   - average logprob per token
   - perplexity
   - manual examples and good vs bad predictions

3. `03_logprobs_for_llm_confidence.ipynb`
   - token logprobs as a confidence signal
   - thresholding logic
   - limitations of logprobs
   - examples with and without retrieved context
   - careful distinction between confidence and correctness

4. `04_log_space_joint_probability.ipynb`
   - probability underflow
   - multiplication vs addition in log space
   - joint probability of sequences
   - comparing candidate sequences via summed logprob

5. `05_log_semiring_graphs.ipynb`
   - the log semiring
   - graph/path interpretation
   - path probabilities and log accumulation
   - most likely path visualizations

6. `06_decibels_log_scale.ipynb`
   - logarithmic scales
   - decibel formulas for power and amplitude ratios
   - linear vs log vs decibel plots

7. `07_custom_algebra.ipynb`
   - custom algebra defined by `a ⊕ b = a + b + (ab / 4)`
   - commutativity
   - associativity testing
   - identity element
   - repeated composition
   - nonlinear growth visualization
   - conceptual comparison with log-space arithmetic

## Setup

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Running the notebooks

```bash
jupyter notebook
```

Then open the notebook you want inside `notebooks/`.

## Notes

- The model is intentionally small and CPU-friendly.
- The code favors clarity over abstraction.
- Notation is kept consistent across notebooks.
