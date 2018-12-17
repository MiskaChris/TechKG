# TechRE
To evaluate the adaptability of TechKG on the task of distantly supervised RE, we select the "*PCNN*+*ATT*" [(Lin et al., 2016)](http://aclweb.org/anthology/P/P16/P16-1200.pdf) model as the baseline method. The source codes of this paper is available at: https://github.com/thunlp/NRE.
## Dataset
We utilize distant supervision to automatically generate relation extraction dataset [TechRE](http://www.techkg.cn/). In the TechRE there are 2 relationships including *hierarchical* relation and NA relation.The dataset of TechRE can be obtained from http://www.techkg.cn/.
## Requirements

- Python (>=2.7)
- TensorFlow (>=1.4.1)
	- CUDA (>=8.0) if you are using gpu
- Matplotlib (>=2.0.0)
- scikit-learn (>=0.18)
## Installation
1. Install TensorFlow
2. Download the 0penNRE-master 
3. Download TechRE dataset from `http://www.techkg.cn/`
4. Extract dataset to `./origin_data`
## Running 
### Process Data 

```bash
python gen_data_python3.py
```
The processed data will be stored in `./data`
### Train Model
```
python train.py --model_name pcnn_att --gpu 0
```
### Test Model
```bash
python test.py --model_name pcnn_att
```
### Plot
```bash
python draw_plot.py pcnn_att
```

