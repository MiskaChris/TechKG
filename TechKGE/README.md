# TechKGE
In our Tech_KGE, we select [ConvE(Dettmers, 2018)](https://arxiv.org/abs/1707.01476), one of the latest state-of-the-art KGE methods as baseline.The [source codes](https://github.com/TimDettmers/ConvE) for this paper is available.
## Installation
1. Install [PyTorch](https://github.com/pytorch/pytorch) using [Anaconda](https://www.continuum.io/downloads). 
2. Install the requirements `pip install -r requirements`
3. Download the default English model used by [spaCy](https://github.com/explosion/spaCy), which is installed in the previous step `python -m spacy download en`
## Running a model
Parameters need to be specified by white-space tuples for example:
```
CUDA_VISIBLE_DEVICES=0 python main.py model ConvE dataset Electric_original \
                                      input_drop 0.2 hidden_drop 0.3 feat_drop 0.2 \
                                      lr 0.003 process True
```
will run a ConvE model on Electric_original.
## Notes
Because GitHub has limitations on the size of uploaded files, we can't upload the whole datasets used in our experimens. If you want to get the entire data set, please contact renfeiliang@cse.neu.edu.cn or 284165389@qq.com


