# Solution of Team Sribd-med for NeurIPS-CellSeg Challenge
This repository provides the solution of team Sribd-med for [NeurIPS-CellSeg](https://neurips22-cellseg.grand-challenge.org/) Challenge. The details of our method are described in our paper [Multi-stream Cell Segmentation with Low-level Cues for Multi-modality Images]. Some parts of the codes are from the baseline codes of the [NeurIPS-CellSeg-Baseline](https://github.com/JunMa11/NeurIPS-CellSeg) repository,

You can reproduce our method as follows step by step:

## Environments and Requirements:
Install requirements by

```shell
python -m pip install -r requirements.txt
```

## Dataset
The competition training and tuning data can be downloaded from https://neurips22-cellseg.grand-challenge.org/dataset/
Besides, you can download three publiced data from the following link: 
Cellpose: https://www.cellpose.org/dataset 
Omnipose: http://www.cellpose.org/dataset_omnipose
Sartorius: https://www.kaggle.com/competitions/sartorius-cell-instance-segmentation/overview 

## Automatic cell classification
You can classify the cells into four classes in this step.
Put all the images (competition + Cellpose + Omnipose + Sartorius) in one folder (/data/allimages).
```Run classification code```
python unsup_classification.py
```


Preprocess dataset with

```shell
python pre_process_3class.py
```

## Training
We divide the whole training process into two parts: 1. Cell classification; 2. Cell segmentation


