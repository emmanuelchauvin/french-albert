# French-ALBERT

Introduction
============

ALBERT is "A Lite" version of BERT, a popular unsupervised language representation learning algorithm. ALBERT uses parameter-reduction techniques that allow for large-scale configurations, overcome previous memory limitations, and achieve better behavior with respect to model degradation.

For a technical description of the algorithm, see the paper:  
[ALBERT: A Lite BERT for Self-supervised Learning of Language Representations](https://arxiv.org/abs/1909.11942)

It outperform BERT and even Roberta on some tasks with 18x fewer parameters and can be trained about 1.7x faster.

| Models            | MNLI     | QNLI     | QQP      | RTE      | SST      | MRPC     | CoLA     | STS      |
|-------------------|----------|----------|----------|----------|----------|----------|----------|----------|
| BERT-large        | 86.6     | 92.3     | 91.3     | 70.4     | 93.2     | 88.0     | 60.6     | 90.0     |
| XLNet-large       | 89.8     | 93.9     | 91.8     | 83.8     | 95.6     | 89.2     | 63.6     | 91.8     |
| RoBERTa-large     | 90.2     | 94.7     | **92.2** | 86.6     | 96.4     | **90.9** | 68.0     | 92.4     |
| ALBERT (1M)       | 90.4     | 95.2     | 92.0     | 88.1     | 96.8     | 90.2     | 68.7     | 92.7     |
| ALBERT (1.5M)     | **90.8** | **95.3** | **92.2** | **89.2** | **96.9** | **90.9** | **71.4** | **93.0** |

And for "Question & answering" (SQUAD and RACE benchmarks) :

|Models                    | SQuAD1.1 dev  | SQuAD2.0 dev  | SQuAD2.0 test | RACE test (Middle/High) |
|--------------------------|---------------|---------------|---------------|-------------------------|
|BERT-large                | 90.9/84.1     | 81.8/79.0     | 89.1/86.3     | 72.0 (76.6/70.1)        |
|XLNet                     | 94.5/89.0     | 88.8/86.1     | 89.1/86.3     | 81.8 (85.5/80.2)        |
|RoBERTa                   | 94.6/88.9     | 89.4/86.5     | 89.8/86.8     | 83.2 (86.5/81.3)        |
|UPM                       | -             | -             | 89.9/87.2     | -                       |
|XLNet + SG-Net Verifier++ | -             | -             | 90.1/87.2     | -                       |
|ALBERT (1M)               | 94.8/89.2     | 89.9/87.2     | -             | 86.0 (88.2/85.1)        |
|ALBERT (1.5M)             | **94.8/89.3** | **90.2/87.4** | **90.9/88.1** | **86.5 (89.0/85.5)**    |

The complete performances of ALBERT are showed on Github from this link : [results](https://github.com/google-research/albert#results)

All that results have been established on English and Chinese Datasets. 

Our work
========

So, we built a French ALBERT base model from a complete Wikipedia French Dataset. This base model is composed of 12M parameters (instead of 108M for BERT base).

The model has been trained for 1.5M steps during 4 days on a [TPU v3-256](https://cloud.google.com/tpu/docs/types-zones) on Google Cloud. So, thank you to Google and the [TensorFlow Research Cloud (TFRC)](https://www.tensorflow.org/tfrc) for their support during this project.

You can download the model here : [French Albert Base model](https://storage.cloud.google.com/french_albert_base/french_albert_base.zip?authuser=1&hl=fr).

The results
===========
ttt
toto 

Based on this model we did 2 fine-tunings : on a classifier and on a "Question Answering" benchmark named FQuAD. 

#### 1) Classifier

We trained our own Dataset (Insurance complains associated with contract type) and improve the result compare to BERT of 2.5%.


Of course the "Question & Answering" SQUAD Dataset constists only of English texts. Fortunatelly recently a French "Question & Answering" Dataset has been built by the Illuin Technology company named FQuAD. You can download here for [Training Dataset](https://storage.googleapis.com/illuin/fquad/train.json.zip) and [Validation Dataset](https://storage.googleapis.com/illuin/fquad/valid.json.zip). These Dataset are under this licence [CC BY-NC-SA 3.0](https://creativecommons.org/licenses/by-nc-sa/3.0/fr/#).

[id]: http://example.com/  "Optional Title Here"

Thank you to [TensorFlow Research Cloud (TFRC)](https://www.tensorflow.org/tfrc) for their support and help during this project.


Performance of ALBERT on GLUE benchmark results using a single-model setup on
dev:

# This is an <h1> tag
## This is an <h2> tag
###### This is an <h6> tag
