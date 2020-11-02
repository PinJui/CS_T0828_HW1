- [CS_T0828_HW1](#cs-t0828-hw1)
  * [Data Preparation](#data-preparation)
  
# CS_T0828_HW1
Stanford Cars Dataset(Brand classification)
Using the ECCV'20 paper
**Fine-Grained Visual Classification via Progressive Multi-Granularity Training of Jigsaw Patches**'s method

> Referencing the paper
```
@InProceedings{du2020fine,
  title={Fine-Grained Visual Classification via Progressive Multi-Granularity Training of Jigsaw Patches},
  author={Du, Ruoyi and Chang, Dongliang and Bhunia, Ayan Kumar and Xie, Jiyang and Song, Yi-Zhe and Ma, Zhanyu and Guo, Jun},
  booktitle = {European Conference on Computer Vision},
  year={2020}
 } 
 ```

## Data Preparation
Download the given dataset and reorganize the structure as below:
```
dataset
├── train
│   ├── Acura Integra Type R 2001
|   |      ├── 000406.jpg
|   |      ├── 000xxx.jpg
|   |      └── ...
│   ├── Acura RL Sedan 2012
|   |      ├── 000091.jpg
|   |      ├── 000xxx.jpg
|   |      └── ...
│   └── ...
└── test
    ├── Acura Integra Type R 2001
    |      ├── 000416.jpg
    |      ├── 000xxx.jpg
    |      └── ...
    ├── Acura RL Sedan 2012
    |      ├── 000101.jpg
    |      ├── 000xxx.jpg
    |      └── ...
    └── ...
```


