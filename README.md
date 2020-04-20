# French-ALBERT
We built a french ALBERT model.

ALBERT is "A Lite" version of BERT, a popular unsupervised language representation learning algorithm. ALBERT uses parameter-reduction techniques that allow for large-scale configurations, overcome previous memory limitations, and achieve better behavior with respect to model degradation.

For a technical description of the algorithm, see the paper:  
[ALBERT: A Lite BERT for Self-supervised Learning of Language Representations](https://arxiv.org/abs/1909.11942)

The performance of ALBERT on GLUE benchmark are showed on Github from this link : [results](https://github.com/google-research/albert#results) 

So, we built from a complete Wikipedia French Dataset a ALBERT Base model.

[id]: http://example.com/  "Optional Title Here"

Thank you to [TensorFlow Research Cloud (TFRC)](https://www.tensorflow.org/tfrc) for their support and help during this project.


Performance of ALBERT on GLUE benchmark results using a single-model setup on
dev:

| Models            | MNLI     | QNLI     | QQP      | RTE      | SST      | MRPC     | CoLA     | STS      |
|-------------------|----------|----------|----------|----------|----------|----------|----------|----------|
| BERT-large        | 86.6     | 92.3     | 91.3     | 70.4     | 93.2     | 88.0     | 60.6     | 90.0     |
| XLNet-large       | 89.8     | 93.9     | 91.8     | 83.8     | 95.6     | 89.2     | 63.6     | 91.8     |
| RoBERTa-large     | 90.2     | 94.7     | **92.2** | 86.6     | 96.4     | **90.9** | 68.0     | 92.4     |
| ALBERT (1M)       | 90.4     | 95.2     | 92.0     | 88.1     | 96.8     | 90.2     | 68.7     | 92.7     |
| ALBERT (1.5M)     | **90.8** | **95.3** | **92.2** | **89.2** | **96.9** | **90.9** | **71.4** | **93.0** |
