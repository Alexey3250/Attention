# Attention Visualization with BERT

<img src="https://i.imgur.com/nWVIN3M.png">

## Introduction

Welcome to this guide on visualizing attention in language models! Specifically, we're delving into the fascinating realm of BERT (Bidirectional Encoder Representations from Transformers) and its ability to predict masked words in a given context. The focus of this project is two-fold: firstly, to predict masked words using a pre-trained BERT model; and secondly, to generate and analyze attention diagrams to understand the model's internal mechanisms.

## Setup

To get started, you'll need to set up your environment:

1. Ensure you have TensorFlow installed in your environment. If not, you can install it using `pip`:
   ```bash
   pip install tensorflow
   ```

2. Clone this repository to get access to the scripts and required files.

3. Install the necessary Python packages:
   ```bash
   pip install -r requirements.txt
   ```

4. The key scripts you'll be working with are `mask.py` for predictions and `visualize_attentions.py` for generating attention diagrams.

## Using the Masked Language Model

The `mask.py` script is your starting point. This script prompts you for a text input with a `[MASK]` token representing the word to predict. It utilizes a BERT model and outputs the top predictions for the masked word.

Here's how you can use it:
```bash
python mask.py
```

When prompted, enter a sentence with the `[MASK]` token, and the script will provide you with the model's predictions.

## Visualizing Attention

The attention mechanism is what sets BERT apart, and visualizing it can give us insights into how the model understands language. To see this in action, after you run the `mask.py` script, it will generate attention diagrams for each of BERT's attention heads.

The `visualize_attentions` function in the script is designed to produce these graphical representations, showing how each word in the input sequence attends to every other word.

## Understanding the Code

- `get_mask_token_index`: This function locates the `[MASK]` token within the input sequence and returns its index.

- `get_color_for_attention_score`: This function converts attention scores to a grayscale color, with higher scores resulting in lighter shades.

- `visualize_attentions`: This function creates and saves a visual diagram for each attention head in the BERT model.

- `generate_diagram`: It generates a single attention diagram per attention head, shading the grid based on the attention scores.

# Analysis

## Layer 8, Head 11 Analysis

Layer 8, Head 11 seems to be attuned to the context provided by adverbial clauses in relation to the actions of the subject. When examining sentences with adverbs and masked verbs, this attention head prominently focuses on conjunctions and context-establishing adverbs that precede the masked verb. This suggests that it plays a part in piecing together the overall scene described by the sentence to predict the action accurately.

**Example Sentences:**
- "The cat, despite the noise and distractions, [MASK] gracefully."
  - <img src="https://i.imgur.com/KTA8wCT.png" width = "450">
- "The cat, even with all the chaos, [MASK] quickly."
  - <img src="https://i.imgur.com/NSYB9E4.png"  width = "450">

These observations indicate that Layer 8, Head 11 may be involved in contextual verb prediction, focusing on how adverbial modifiers relate to the subject's actions within a sentence.

## Layer 10, Head 2 Analysis

Based on the findings from the attention diagrams, a conclusion can be drawn about the potential understanding BERT has of the word "AI" and it's relations to the qualities attached to this object in the sentence. This would involve summarizing the attention patterns and positing a theory on what BERT's Layer 10, Head 2 might have learned about "AI" in the context.

- "Oh great, another AI that claims it can pass the Turing test, but **[MASK]** as well as a toaster."
<img src="https://i.imgur.com/g5CaJ41.png"  width = "700">
    - Oh great, another AI that claims it can pass the Turing test, but **not** as well as a toaster.
    - Oh great, another AI that claims it can pass the Turing test, but **fails** as well as a toaster.
    - Oh great, another AI that claims it can pass the Turing test, but **only** as well as a toaster.


- "Sure, the AI has 'learned' from its mistakes, now it **[MASK]** errors with twice the confidence."
<img src="https://i.imgur.com/xezBmur.png"  width = "700">
    - Sure, the AI has 'learned' from its mistakes, now it **commits** errors with twice the confidence.
    - Sure, the AI has 'learned' from its mistakes, now it **makes** errors with twice the confidence.
    - Sure, the AI has 'learned' from its mistakes, now it **corrected** errors with twice the confidence.
