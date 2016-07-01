#### word2vec is quite famous by now. I explored the reasons why it works well

Sources- 

[Distributed Representations of Words and Phrases and their Compositionality](https://papers.nips.cc/paper/5021-distributed-representations-of-words-and-phrases-and-their-compositionality.pdf) ,
[Efficient Estimation of Word Representations in Vector Space](http://arxiv.org/pdf/1301.3781.pdf) ,
[word2vec Explained: Deriving Mikolov et al.’s Negative-Sampling Word-Embedding Method](http://arxiv.org/pdf/1402.3722v1.pdf) ,
[Neural Word Embedding as Implicit Matrix Factorization](https://papers.nips.cc/paper/5477-neural-word-embedding-as-implicit-matrix-factorization.pdf)

* 2 variants- Continous Bag of Words(CBOW) and skip-gram model with negative sampling(SGNS). CBOW is trained to predict the target word from the contextual words that surround it, while the skip-gram model predicts the neighboring words given the current word.

* Skip gram model was introduced by Mikolov in http://arxiv.org/pdf/1301.3781.pdf

* Skip gram model defined using softmax is impractical; computationally expensive because of summation term in denominator

* Practical alternatives are hierarchical softmax and Noise Contrastive Estimation (NCE). The model proposed in this paper further simplifies NCE by defining Negative sampling (NEG). One way to think of it is NCE proposes a much stronger claim, something we don't need. We can simplify it and only learn high quality vector representations. 

* Negative-sampling is based on the skip-gram model, but is optimizing a different objective.

* The objective function in SGNS tries to increase the product of word vectors for good word-context pairs, and decrease it for bad ones. Intuitively, this means that words that share many contexts will be similar to each other. 

* The above hypothesis is very hand-wavy. More formal work on this needs to be done

* Derivation of negative sampling explained very well in -> http://arxiv.org/pdf/1402.3722v1.pdf

* Another idea is to extend from word based to phrase based model. Mikolov's model uses subsampling of frequent words. 

* To learn phrases, model first finds words that appear frequently together, and infrequently in other contexts. This way it is able to capture phrases like "New York Times", without greatly increasing the size of vocabulary

* Quoting Omer Levy- " word2vec through SGNS is doing something very similar to what the NLP community has been doing for about 20 years, it's just doing it really well."

* More on it at- [Neural Word Embedding as Implicit Matrix Factorization](https://papers.nips.cc/paper/5477-neural-word-embedding-as-implicit-matrix-factorization.pdf)

