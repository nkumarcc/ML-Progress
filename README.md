# Github ML Resume

### To Read

Articles
- https://www.inverse.com/health/best-health-breakthrough-2023-gene-editing-crispr?utm_source=tldrnewsletter

Papers
- Stable Diffusion - Lmfao ResearchGPT really gave some terrible suggestions
  - [High-Resolution Image Synthesis with Latent Diffusion Models](https://arxiv.org/pdf/2112.10752.pdf)
  - [Asymptotic Exponential Stability for Diffusion Processes Driven by Stochastic Differential Equations in Duals of Nuclear Spaces](https://ems.press/content/serial-article-files/2648)
  - [Double diffusive convection in a horizontal sparcely packed porous layer](https://www.sciencedirect.com/science/article/abs/pii/0735193386900357?via%3Dihub)
  - [Stability of traveling wavefronts for time-delayed reaction-diffusion equations](https://www.aimsciences.org/article/doi/10.3934/proc.2009.2009.526)
  - [Choices and pitfalls concerning mixture-of-experts modeling](https://www.scielo.br/j/pope/a/b8kfZkrkhG6ndHwLHDn4DjS/?lang=en)
  - [Mixed Methods Research: A Research Paradigm Whose Time Has Come](https://journals.sagepub.com/doi/10.3102/0013189X033007014)
  - [Investigation of Mixture of Experts Applied to Residential Premises Valuation](https://link.springer.com/chapter/10.1007/978-3-642-36543-0_24)

Repos
- [LLMs and Kernels](https://charlesfrye.github.io/programming/2023/11/10/llms-systems.html)

### Courses Taken

Andrew Ng DL Specialization:
- Neural Networks and Deep Learning
- Improving Deep Neural Networks: Hyperparameter Tuning, Regularization, and Optimization
- Structuring Machine Learning Projects
- Convolutional Neural Networks

In Progress:

- Sequence Models Andrew Ng Course - Read enough papers about RNN + LLM history, don't think I'm going to do this one.
- https://github.com/jacobhilton/deep_learning_curriculum/tree/master
- https://projecteuler.net/

### Papers Read

LLMs


- [Neural Machine Translation by Jointly Learning to Align and Translate](https://arxiv.org/abs/1409.0473)
- [Attention is All You Need](https://arxiv.org/abs/1706.03762)
- GPT 1, 2, and 3
- [BERT](https://arxiv.org/abs/1810.04805) and [BART](https://arxiv.org/abs/1910.13461)
- [ROME](https://rome.baulab.info/?ref=blog.mithrilsecurity.io)
- [Mixture of Experts](https://arxiv.org/abs/1701.06538)
- To read:
  - [ToxiGen](https://arxiv.org/abs/2203.09509?ref=blog.mithrilsecurity.io)
  - [Inside Transformers](https://transformer-circuits.pub/2021/framework/index.html)
  - [LLaMa-2](https://medium.com/towards-generative-ai/understanding-llama-2-architecture-its-ginormous-impact-on-genai-e278cb81bd5c)
- [Dolma release post](https://blog.allenai.org/dolma-3-trillion-tokens-open-llm-corpus-9a0ff4b8da64)

RL

- [Temporal Difference Learning of N-Tuple Networks for the Game 2048](http://www.cs.put.poznan.pl/wjaskowski/pub/papers/Szubert2014_2048.pdf)

Misc:
- [AlphaFold](https://www.nature.com/articles/s41586-021-03819-2)
- [High Fidelity Neural Audio Compression](https://arxiv.org/abs/2210.13438)
- [ByteDance Monolith](https://arxiv.org/pdf/2209.07663.pdf)

### Implemented Projects

- [Attention is All You Need - building a transformer from scratch:](https://github.com/nkumarcc/tf-attention-is-all-you-need)
  - **Incomplete:** Ran into issues when building masking in the Decoder layer from scratch.
  - **Lessons learned:** Read the README in the repo. A lot of lessons learned.
- [2048 NN, using a version of n-tuple learning generalized to a neural network](https://github.com/nkumarcc/2048-NN):
  - **Incomplete**
  - **Method:** 1-ply n-tuple learning, where instead of using pure n-tuple learning as described in the [N-Tuples w/ 2048](http://www.cs.put.poznan.pl/wjaskowski/pub/papers/Szubert2014_2048.pdf) paper, used convolution layers to represent n-tuples and used a neural network. Based the network
  - **Lessons Learned:**
    - How to change CUDA + cudNN drivers on Google Colab. Also that `theano` and `lasagne` really aren't compatible with much of anything anymore lmfao.
    - Reinforcement learning, in particular temporal difference learning, 1-ply n-tuple based learning.
- [Kaggle 'I'm Something of a Painter Myself'](https://www.kaggle.com/code/nkumarcc3000/notebook33fea62f8e)
