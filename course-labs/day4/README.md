# Day 4 — Course Lab

**Course 5 · Fine-tune Your Model**
**Lab:** Fine-Tuning a Layer with LoRA
*(Kenya Workshop 2 copy)*

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aims-ai-research-foundations/Kenya-workshop-2/blob/main/course-labs/day4/day4-course5-student.ipynb)

## About

Take one frozen 4×8 layer and adapt it, by hand and in code. You start by
watching a pre-trained model give a reasonable but wrong-for-your-purpose
answer, then count exactly how many parameters full fine-tuning moves. From
there you build a LoRA update entry by entry as the outer product of a
down-projection and an up-projection, compute its gradient, and train a real
adapter on a small set of praise and complaint phrases. The last part of the
core lab merges the adapter into the weights — showing it costs nothing at
inference — and swaps in a second adapter over the same frozen model.

Parts 1–4 are the lab and fit the hour. Parts 5 and 6 are optional extensions,
about twelve minutes together: how to choose the rank, and what the saving
looks like on a real model. Everything runs on NumPy and Matplotlib — no GPU,
no downloads, no tokens.

## How to work through it

- Click **Open in Colab** above to launch the notebook.
- **Before running or editing anything, save your own copy: File → Save a copy
  in Drive.** The badge opens the notebook in read-only playground mode;
  without your own copy, all your work is lost when the tab closes.
- Follow the **Predict → Run → Explain** protocol for every code cell: predict
  what will happen (shapes, numbers), run it, then explain any surprises.
- Three `YOUR CODE HERE` cells carry the work: one full fine-tuning step, one
  LoRA gradient step, and an evaluation loop over held-out phrases. Each has
  commented check-yourself lines directly beneath it.
- Stop at **⏸️ The core lab ends here** if you are working in the session slot.
  You will have met all four learning outcomes by that point.
