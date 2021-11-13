# Named Entity Recognition BiLSTM


### Problem Statement

Recognize the Named Entity in a text.

### Dataset 

The dataset used can be found here: https://www.kaggle.com/bradbolliger/gmb-v220


### Model

The model has 4 layers.

1. An Embedding layer. (Embedding dimension of 64)
2. Bidirectional LSTM layer. (100 units)
3. TimeDistrubited Dense Layer. (100 units)
4. Classification Dense Layer. (Length of NER Vocab)


### Steps

1. I begin by loading and cleaning the data.
2. Next, was to bring the NER data in IOB format.
3. Tokenized the text and saved the tokenizer.
4. Padded the sequence to a fixed of 50.
5. OneHotEncoded the NER tags.
6. Created the model.
7. Next, was training the model for 15 epochs, with EarlyStopping, if the model dosn't improve for the next 3 iterations.


### Training

Beginning of the training:

The training accuracy began at 87% and loss was at around 0.1834.
The validation accuracy began at 95% and loss was at around 0.0713.

End of the training (At 6th epochs due to early stopping):

The training accuracy ended at 98% and loss was at around 0.0231.
The validation accuracy ended at 96% and loss was at around 0.0571.

##### Loss: 



<img src="https://github.com/mahesh863/Named-entity-recognition-BiLSTM/blob/main/Graphs/Loss.png" width="500px">



#### Accuracy:

<img src="https://github.com/mahesh863/Named-entity-recognition-BiLSTM/blob/main/Graphs/Acc.png" width="500px">

### Output

The model was able to Differentiate between different entities. Below are the results.

<img src="https://github.com/mahesh863/Named-entity-recognition-BiLSTM/blob/main/Graphs/Results.png" width="800px">


### Conclusion

This is not the best technique. A better model could be built with Conditional random fields (CRF).






