# Emojify
Used word vector representations to build an Emojifier.
# Intro
Have you ever wanted to make your text messages more expressive? Your emojifier app will help you do that. So rather than writing "Congratulations on the promotion! Lets get coffee and talk. Love you!" the emojifier can automatically turn this into "Congratulations on the promotion! 👍 Lets get coffee and talk. ☕️ Love you! ❤️"
# Implementation
I'll start with a baseline model (Emojifier-V1) using word embeddings, then build a more sophisticated model (Emojifier-V2) that further incorporates an LSTM.
# Conclusions
If you have an NLP task where the training set is small, using word embeddings can help your algorithm significantly. Word embeddings allow your model to work on words in the test set that may not even have appeared in your training set.


Training sequence models in Keras (and in most other deep learning frameworks) requires a few important details:


- To use mini-batches, the sequences need to be padded so that all the examples in a mini-batch have the same length.


- An Embedding() layer can be initialized with pretrained values. These values can be either fixed or trained further on your dataset. If however your labeled dataset is small, it's usually not worth trying to train a large pre-trained set of embeddings.


- LSTM() has a flag called return_sequences to decide if you would like to return every hidden states or only the last one.


- You can use Dropout() right after LSTM() to regularize your network.
