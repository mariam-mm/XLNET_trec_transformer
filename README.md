XLNET Text Classification
================
Mariam Oluwatobi Abubakar
April 11, 2021

## Challenge

Applying XLNET transformer to perform Text classification on TREC-50
dataset.

<hr>

</hr>

## Dataset

The data given can be accessed via the following link
<http://search.r-project.org/library/textdata/html/dataset_trec.html#>:~:text=The%20TREC%20dataset%20is%20dataset,50%20has%20finer%2Dgrained%20labels
.The TREC dataset for classification consists of open-domain, fact-based
questions divided into broad semantic categories. It has both a
six-class (TREC-6) and a fifty-class (TREC-50) version. Both have 5,452
training examples and 500 test examples, but the dataset used for this
text classification TREC-50 has finer-grained labels. A 50 labels
dataset is created using labels in
<https://cogcomp.seas.upenn.edu/Data/QA/QC/definition.html> and data in
<https://cogcomp.seas.upenn.edu/Data/QA/QC/>

## Background and Model Choice

In order to achieve Text classification using TREC-50 dataset, which is
an arm of Natural Language Processing. A state of the art text
classification deep learning algorithm called XLNET is used. \> Why Deep
Learning? Compared to other machine learning models, deep learning
enables us to attain higher model accuracy in classification, as well as
a faster output considering the data size. \> Why XLNET? XLNET is is an
auto-regressive language model which outputs the joint probability of a
sequence of tokens based on the transformer architecture with
recurrence. Its training objective calculates the probability of a word
token conditioned on all permutations of word tokens in a sentence, as
opposed to just those to the left or just those to the right of the
target token. In order to achieve effective text classification with
deep learning. This pre-trained model enables us to achieve transfer
learning.

## Pre-processing techniques

In order to effectively fine-tune XLNET transformer language model to
pre-process and extract matrix embedding of the Trec-50 text
classification, we make use of an abstract NLP transformer library built
on the popular huggingface NLP library called ![Simpler
Transformers](https://github.com/ThilinaRajapakse/simpletransformers).
Data split is done at a ratio of 0.1 to get test set from the Trec-50 so
as to evaluate the training efficiently.

## Training and Evaluation techniques

The training phase relies on a classification layer added to the
embedded matrix, because we have effectively pre-process our text data.
The evaluation dataset is used to get our classification model accuracy
metric results.

## Results and Metrics

Model Accuracy - 72%

## Usage

Model Training can be seen from ![xlnet\_runner.ipynb](/xlnet\_runner.ipynb)

## Limitations

  - Require more data to pretrain model for improved accuracy as
    hyperparameters depends on data volume

## References

  - <http://jalammar.github.io/illustrated-transformer/>
  - <https://github.com/ThilinaRajapakse/simpletransformers>
