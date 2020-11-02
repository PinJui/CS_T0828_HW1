# CS_T0828_HW1

Stanford Cars Dataset(Brand classification challenge)

## Contents

- [Reference](#reference)
- [Data Preparation](#data-preparation)
- [Training](#training)
- [Inferencing](#inferencing)

## Reference

Using the ECCV'20 paper

**Fine-Grained Visual Classification via Progressive Multi-Granularity Training of Jigsaw Patches**'s method

```
@InProceedings{du2020fine,
  title={Fine-Grained Visual Classification via Progressive Multi-Granularity Training of Jigsaw Patches},
  author={Du, Ruoyi and Chang, Dongliang and Bhunia, Ayan Kumar and Xie, Jiyang and Song, Yi-Zhe and Ma, Zhanyu and Guo, Jun},
  booktitle = {European Conference on Computer Vision},
  year={2020}
 } 
 ```

## Data Preparation
Download the given dataset and split the training data into 9:1 for train and valid, and reorganize the train and valid data structure as below:
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
***Be careful with the class name with / inside***

## Training
1. create your working directory and put the organized training dataset in to the directory and run command ```git clone https://github.com/PRIS-CV/PMG-Progressive-Multi-Granularity-Training.git```
2. change the store_name in train.py to your dataset directory name and the desired number of epochs
3. run command ```cd your_working_dir```
4. run command ```python train.py```

Here you can check the training accuracy,loss and testing accuracy,loss in output and also in the file writtern in dataset folder(results_train.txt,results_test.txt) which will be generated after the training starts

## Inferencing
1. build the class index map(using dataset.class_to_idx method), or u can directly use the file classes.txt for mapping the model's output to real car brand name
2. load the model ```model.pth```, the attached file has been pre-trained for 19 epochs and reaches 99.8% acc in training and 93.47% in validation
3. batchly feed the testing data in given dataset to model and map the model's output to corresponding class name mentioned in step1 and write into prediction.csv file
4. upload the predicted file to kaggle!

