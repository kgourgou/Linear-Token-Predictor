# Linear Token Predictor

This is a reproduction of the model used in Malach, E., 2023. Auto-regressive next-token predictors are universal learners. arXiv preprint arXiv:2309.06979, Section 4.1.

You can also find this in [Colab](https://colab.research.google.com/drive/1RVAlbA2CfKH662_N9UibG5uIQJiAcDUX?usp=sharing).

The model is:

1. An embedding layer from the token space to a d-dimensional vector space.
2. A linear layer of size (d*T)x(d*T), where T is the context window size.
3. A linear layer mapping to logits over the token space.

I also added a LayerNorm in there after the second layer.

This toy model is a good exercise in understanding next token prediction as it does not require positional encodings, self-attention, etc.
