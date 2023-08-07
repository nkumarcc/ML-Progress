Implement a decoder-only transformer language model.

- Here are some first principle questions to answer:
    - **What is different architecturally from the Transformer, vs a normal RNN, like an LSTM? (Specifically, how are recurrence and time managed?)**
      The biggest difference is that positions in transformers use encodings, rather than relying on hidden state neurons like in RNNs. This allows for more information in a sequence to be used in token generation and more parallelization.
    - **Attention is defined as, Attention(Q,K,V) = softmax(QK^T/sqrt(d_k))V. What are the dimensions for Q, K, and V? Why do we use this setup? What other combinations could we do with (Q,K) that also output weights?**
      Q = queries, K = keys, V = values, 
    - Are the dense layers different at each multi-head attention block? Why or why not? 
    - Why do we have so many skip connections, especially connecting the input of an attention function to the output? Intuitively, what if we didn't? 


- Now we'll actually implement the code. Make sure each of these is completely correct - it's very easy to get the small details wrong.
    - Implement the positional embedding function first. 
    - Then implement the function which calculates attention, given (Q,K,V) as arguments. 
    - Now implement the masking function. 
    - Put it all together to form an entire attention block. 
    - Finish the whole architecture.
- If you get stuck, [The Annotated Transformer](http://nlp.seas.harvard.edu/2018/04/03/attention.html) may help, but don't just copy-paste the code.
- To check you have the attention mask set up correctly, train your model on a toy task, such as reversing a random sequence of tokens. The model should be able to predict the second half of the sequence, but not the first.
- Finally, train your model on [the complete works of William Shakespeare](https://www.gutenberg.org/files/100/100-0.txt). Tokenize the corpus by splitting at word boundaries (`re.split(r"\b", ...)`). Make sure you don't use overlapping sequences as this can lead to overfitting.
