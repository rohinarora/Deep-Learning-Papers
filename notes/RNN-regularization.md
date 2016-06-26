###Source- https://arxiv.org/pdf/1409.2329v5.pdf

* Dropout is a very successful technique for regularizing NN.  
* But it doesn't work well with RNN's. This paper shows how to apply dropout to LSTMs
* The main idea is to apply the dropout operator only to the non-recurrent connections.
* By not using dropout on the recurrent connections, the LSTM can benefit from dropout regularization without sacrificing its valuable memorization ability

###Data Sets and model performance

* PTB Language Modeling Perplexity: 78.4
* Google Icelandic Speech Dataset WER Accuracy: 70.5
* WMT'14 English to French Machine Translation BLEU: 29.03
* MS COCO Image Caption Generation BLEU: 24.3

* Dropout helps relative to not using dropout, but using an ensemble eliminates the gains attained by dropout.  * Thus,the main effect of dropout is to **produce a single model that is as good as an  ensemble**, which is a reasonable improvement given the simplicity of the technique.

The code for this paper is at - https://github.com/wojzaremba/lstm
 *Requires GPU to run