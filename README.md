# Propaganda Detection using BERT and Bag-of-Words

This project explores two subtasks in the field of propaganda detection in news articles:
1. Binary Sentence Classification – Classifying whether a given sentence contains propaganda.
2. Snippet Technique Classification – Identifying the technique of propaganda used in a snippet already known to contain propaganda.

The task design and data are inspired by the 2020 SemEval Workshop on Semantic Evaluation, as described by Da San Martino et al. [[1]](#1). My approach compares the performance of a fine-tuned BERT [[2]](#2) model against a traditional Bag-of-Words (BoW) classifier for each of the two subtasks.

The full implementation is available in the form of a Jupyter Notebook, with accompanying data files in TSV format.

## Project Summary
In the original SemEval task, the goals were:
- **Span Identification** - Detecting specific text fragments containing propaganda.
- **Technique Classification** - Identifying the technique used in a given span.
This project adapts these into a simplified and more practical form:
- **Binary classification** at the sentence level.
- **Multi-class classification** at the snippet level, assuming the span is already identified.
I assess:
- **BERT**, a state-of-the-art pretrained transformer model.
- **Bag-of-Words + Logistic Regression**, a classical NLP appraoch.

## Running the Project
To run the notebook:
1. Clone the repository
    git clone https://github.com/brice1101/propaganda-detection.git
2. Open the notebook:
    jupyter notebook propaganda_detection.ipynb
3. Run all cells sequentially.

## References
<a id="1">[1]</a>
G. Da San Martino, A. Barrón-Cedeño, H. Wachsmuth and P. Nakov, “SemEval-2020 Task 11: Detection of Propaganda Techniques in News Articles,” Proceedings of the Fourteenth Workshop on Semantic Evaluation, 2020.
<a id="2">[2]</a>
J. Devlin, M.-W. Chang, K. Lee and K. Toutanova, “BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding,” Arxiv, 2018. 
