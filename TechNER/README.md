# TechNER
To evaluate the adaptability of TechKG on the task of distantly supervised NER, we select the "BiLSTM+CRF" [(Guillaume et al., 2016)](https://arxiv.org/pdf/1603.01360.pdf) model as the baseline method. The source codes of this paper is available at: https://github.com/glample/tagger.

## Dataset

We utilize distant supervision to automatically generate Chinese NER dataset[TechNER](http://www.techkg.cn/).Ｉn the TechNER, we have go on serval experiments.It includes four areas in two different numbers of training sets. The four aeras are computer,traffic,electronic and metal. The number of training sets are 1.5w and 2.5w.The [TechNER](http://www.techkg.cn/) also provide other areas datasets can be downloaded.If you want to train your own data,Input files for the training script have to follow the same format as the CoNLL2003 sharing task: each word has to be on a separate line, and there must be an empty line after each sentence. A line must contain at least 2 columns, the first one being the word itself, the last one being the named entity. It does not matter if there are extra columns that contain tags or chunks in between. Tags have to be given in the IOB format (it can be IOB1 or IOB2).     

## Requirements

- Python (>=2.7)
- Theano (>=1.0)
- Numpy 

## Running 

If you want to train your own data, you need to use the train.py script and provide the location of the training, development and testing set:
./train.py --train train.txt --dev dev.txt --test test.txt
The training script will automatically give a name to the model and store it in ./models/
There are many parameters you can tune (CRF, dropout rate, embedding dimension, LSTM hidden layer size, etc).
































