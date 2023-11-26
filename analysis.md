# Analysis

## Layer 5, Head 3

<img src="https://i.imgur.com/KTA8wCT.png">

## Layer 8, Head 11 Analysis

For Layer 8, Head 11, the attention diagram displays a particular interest in the relationship between the subject "cat" and the masked verb. The attention is distributed across the sentence, but there are noticeable concentrations on the tokens immediately surrounding the masked token, which in this case represents the action of the cat. Interestingly, there's also a significant amount of attention on the tokens "despite the noise and distractions," suggesting that this head may be sensitive to contextual modifiers affecting the action. This could indicate a pattern where the attention head is looking to resolve the action of the subject in the presence of intervening descriptive phrases.

**Example Sentences:**
- "The cat, despite the noise and distractions, [MASK] gracefully."
  - ![cat](https://im2.ezgif.com/tmp/ezgif-2-4187aa0eca.gif)
  - <img src="https://im2.ezgif.com/tmp/ezgif-2-4187aa0eca.gif" width= "300">
- "The dog, even with all the chaos, [MASK] quickly."

In both examples, Layer 8, Head 11 would be expected to highlight the tokens that describe the conditions under which the action is taking place ("despite the noise and distractions" and "even with all the chaos") and relate them to the masked verb, thus paying attention to the part of the sentence that provides context for the subject's action.