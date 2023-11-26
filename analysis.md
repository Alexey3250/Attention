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
- "Oh great, another AI that claims it can pass the Turing test, but [MASK] as well as a toaster."
<img src="https://i.imgur.com/g5CaJ41.png"  width = "700">
```python
Oh great, another AI that claims it can pass the Turing test, but not as well as a toaster.
Oh great, another AI that claims it can pass the Turing test, but fails as well as a toaster.
Oh great, another AI that claims it can pass the Turing test, but only as well as a toaster.
```

- "Sure, the AI has 'learned' from its mistakes, now it [MASK] errors with twice the confidence."
<img src="https://i.imgur.com/xezBmur.png"  width = "700">
```
Sure, the AI has 'learned' from its mistakes, now it makes errors with twice the confidence.
Sure, the AI has 'learned' from its mistakes, now it corrected errors with twice the confidence.
Sure, the AI has 'learned' from its mistakes, now it commits errors with twice the confidence.
```