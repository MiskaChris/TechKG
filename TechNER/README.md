This is a Chinese NER system.

To use the tagger, you need Python 2.7, with Numpy and Theano installed. Training data includes two numbers of scales, 1.5w and 2.5w training sets. The data is included in the dataset folder. The Chinese data contains four types of fields, traffic,metal,computer and electronic.

If you want to train your own data, you need to use the train.py script and provide the location of the training, development and testing set:
./train.py --train train.txt --dev dev.txt --test test.txt
The training script will automatically give a name to the model and store it in ./models/
There are many parameters you can tune (CRF, dropout rate, embedding dimension, LSTM hidden layer size, etc).

Input files for the training script have to follow the same format as the CoNLL2003 sharing task: each word has to be on a separate line, and there must be an empty line after each sentence. A line must contain at least 2 columns, the first one being the word itself, the last one being the named entity. It does not matter if there are extra columns that contain tags or chunks in between. Tags have to be given in the IOB format (it can be IOB1 or IOB2).


