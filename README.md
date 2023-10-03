# word2vec_skipgram_ns
word2vec_skipgram_ns


Word2Vec (Skip-Gram + Negative Sampling)

Word2Vec is a popular natural language processing (NLP) technique that is used for representing the word in multiple dimensions, which are vector representations of words in a continuous vector space. These vectors are called embeddings, and these are not explainable. Embeddings are widely used in various NLP tasks such as text classification, machine translation, and sentiment analysis.
There are two main approaches to train Word2Vec models: 
1.	CBOW (Continuous Bag of Words) – predicting a target word based on the context (neighboring) words.
2.	Skip-Gram – predicting context words based on target word.

Problem! 
The above representation has been defined by Neural Network with all the vocabulary in both Input layer and output layer with a hidden layer. Due to this representation, the final network size (#of weights) is significantly large. 
Say, vocabulary size = 10000 & #hidden units = 100. The total number weight becomes 10000 X 100 + 100 X 10000 + 10000 = 2010000.

Solution!
Negative Sampling – It is a technique that addresses the above issue by first change the structure target (input) and context (output) into all target + context (paired one) called positive samples and a sample of target + non-context (non-paired one) called negative samples.
This eventually transforms the above problem into a binary logistic regression.

Links for further reading –

https://jalammar.github.io/illustrated-word2vec/
https://www.baeldung.com/cs/nlps-word2vec-negative-sampling
https://zhuanlan.zhihu.com/p/42651829
https://arxiv.org/pdf/1301.3781.pdf
https://proceedings.neurips.cc/paper/2013/file/9aa42b31882ec039965f3c4923ce901b-Paper.pdf
http://mccormickml.com/2017/01/11/word2vec-tutorial-part-2-negative-sampling/#:~:text=Word2Vec%20implements%20a%20%E2%80%9Csubsampling%E2%80%9D%20scheme,related%20to%20the%20word's%20frequency


