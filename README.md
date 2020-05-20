# Speech-Tagging-Pytorch
Using Recurrent Neural Network ( LSTM ) to predict part of speech tags using Pytorch

## What's Part of speech tagging?:

![GitHub Logo](/images/logo.png)
Format: ![ERROR](https://miro.medium.com/max/2340/1*CbZE2ZTBlmswW84Knjbqkg.png)


>> * part-of-speech tagging also called word-category disambiguation, is the process of marking up a word in a text  as corresponding to a particular part of speech,based on both its definition and its context—i.e., its relationship with adjacent and related words in a phrase, sentence, or paragraph. 

* This means that depending on the word itself and its context we can determine weither it's a Noun Verb or Determinant


## Steps for creating the Model:

1. Create or load a dataset that contains a tuple (sentense,tags for each word)
2. Create a function that creates a vocabulary which means each unique word with a unique key (index)
3. Define the structure of the Model in this cas a single layer LSTM is enough (small dataset)
4. train the Model using SGD optimizer and NLLLoss .

## The Model:

The Model contains is made of :

a. Embedding :This helps us embedd each sentense in a specific dimension in this notebook each word is encoded in a vector of 6 values

b. LSTM layer :This layer contains a number of hidden units equal to (hidden_size) 

c. Fully connected layer: This layer takes the output of the LSTM to 3 output units in order to make prediction for each tag using log softmax

**Note** : The size of the sequence (number of words in as sentense ) can be different ! The gradients won't be updated untill the end of the sequence .So having different sequence sizes is not a problem.
