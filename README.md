# ToxicCommentDetection
A deep learning attempt to identify toxic comments (multi-label classification)

The original problem was taken from this [Kaggle competition](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge).
The competition supllies the train and test files that included in this repository in zip format.

The challenge is to build a multi-headed model that’s capable of detecting different types of of toxicity like threats, obscenity, insults, and identity-based hate.

The summry of the pre-processing steps:

- Tokenize each document and remove stopwords
- Get index for each word (this is done via combining train and test documents)
- Convert each document to word vector
- Prpare training data considering first k number of words from each document

After that, I used Keras (with TensorFlow backend) and tried several models like:

- Simple single hidden layer ANN
- ANN with an embedding layer that is learnt during the process
- ANN with a pre-trained Embedding layer GLOVE. The source of the embedding files are not included in this repo since the file sizes are too big, but you can download them from [here](https://nlp.stanford.edu/projects/glove/).
- Recurrent neural network (RNN) 
- RNN with embedding
- RNN with embedding and LSTM/GRU


