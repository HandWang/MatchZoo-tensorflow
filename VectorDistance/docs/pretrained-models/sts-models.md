# STS Models
The models were first trained on [NLI data](nli-models.md), then we fine-tuned them on the  [STS benchmark dataset](http://ixa2.si.ehu.es/stswiki/index.php/STSbenchmark). This generate sentence embeddings that are especially suitable to measure the semantic similarity between sentence pairs.

# Datasets
We use the training file from the  [STS benchmark dataset](http://ixa2.si.ehu.es/stswiki/index.php/STSbenchmark).

For a training example, see [examples/training_stsbenchmark.py](../../examples/training_stsbenchmark.py). 

# Pre-trained models
 We provide the following pre-trained models:
 - **bert-base-nli-stsb-mean-tokens**: First fine-tuned on AllNLI, then on STS benchmark training set. Performance: STSbenchmark: 85.14
- **bert-large-nli-stsb-mean-tokens**: First fine-tuned on AllNLI, then on STS benchmark training set. Performance: STSbenchmark: 85.29

# Performance Comparison
Here are the performances on the STS benchmark for other sentence embeddings methods. They were also computed by using cosine-similarity and Spearman rank correlation. Note, these models were not-fined on the STS benchmark.

- Avg. GloVe embeddings:  58.02 
- BERT-as-a-service avg. embeddings:  46.35 
- BERT-as-a-service CLS-vector: 16.50 
- InferSent - GloVe: 68.03 
- Universal Sentence Encoder: 74.92