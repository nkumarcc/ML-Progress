# Github ML Resume

### Courses Taken

Andrew Ng DL Specialization:
- Neural Networks and Deep Learning
- Improving Deep Neural Networks: Hyperparameter Tuning, Regularization, and Optimization
- Structuring Machine Learning Projects

In Progress:
- Convolutional Neural Networks
- Sequence Models

### Papers Read

LLMs


- [Neural Machine Translation by Jointly Learning to Align and Translate](https://arxiv.org/abs/1409.0473)
- [Attention is All You Need](https://arxiv.org/abs/1706.03762)
- GPT 1, 2, and 3
- [BERT](https://arxiv.org/abs/1810.04805) and [BART](https://arxiv.org/abs/1910.13461)

RL

- [Temporal Difference Learning of N-Tuple Networks for the Game 2048](http://www.cs.put.poznan.pl/wjaskowski/pub/papers/Szubert2014_2048.pdf)

Misc:
- [AlphaFold](https://www.nature.com/articles/s41586-021-03819-2)
- [High Fidelity Neural Audio Compression](https://arxiv.org/abs/2210.13438)
- [ByteDance Monolith](https://arxiv.org/pdf/2209.07663.pdf)

### Implemented Projects

- [Attention is All You Need - building a transformer from scratch:](https://github.com/nkumarcc/tf-attention-is-all-you-need)
  - **Incomplete:** Ran into issues when building masking in the Decoder layer from scratch.
  - **Lessons learned:**
- [2048 NN, using a version of n-tuple learning generalized to a neural network](https://github.com/nkumarcc/2048-NN):
  - **Incomplete**
  - **Method:** 1-ply n-tuple learning, where instead of using pure n-tuple learning as described in the [N-Tuples w/ 2048](http://www.cs.put.poznan.pl/wjaskowski/pub/papers/Szubert2014_2048.pdf) paper, used convolution layers to represent n-tuples and used a neural network. Based the network
  - **Lessons Learned:**
    - How to change CUDA + cudNN drivers on Google Colab. Also that `theano` and `lasagne` really aren't compatible with much of anything anymore lmfao.
    - Reinforcement learning, in particular temporal difference learning, 1-ply n-tuple based learning.
- [Kaggle 'I'm Something of a Painter Myself'](https://www.kaggle.com/code/nkumarcc3000/notebook33fea62f8e)
