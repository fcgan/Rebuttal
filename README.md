# Fuzzy Cycle Generative Advesarial Network
This page shows some results of supplementary experiments in rebuttal period of IJCAI2019. Detail description can be seen in rebuttal content.

## The list of experiments is as below:
> 1 cross-domain image generation for different source objects

> 2 feature map visualization for different source objects
  
> 3 t-SNE and PCA plots for different source objects
  
> 4 Occlution Test for different source objects
  
> 5.Evaluation criteria and updated F1-scores

> 6.Settings of supervised methods in Section 4.2

> 7.Formula of V_S and V_T

> 8.Updated Algorithm 1

## Details of the experiments:
### 1. cross-domain image generation for different source objects

### 2. feature map visualization for different source objects

### 3. t-SNE and PCA plots for different source objects

### 4. Occlution Test for different source objects

### 5. Evaluation criteria and Updated F1-score
> * **Criterias**

>> TP (True Positive): predicting the correct answer  
>> FP (False Positive): wrong to predict other classes as this class  
>> FN (False Negative): This type of label is predicted to be other types of labels.  
>> Precision: refers to the proportion of positive samples in the positive case determined by the classifier:  
>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/precision.gif)  
>> Recall: refers to the proportion of the total positive case that is predicted to be positive:  
>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/recall.gif)  
>> Represents the classifier to determine the correct proportion of the entire sample:  
>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/acc.gif)  
>> F1-score under each category:  
>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/fi.gif)

> * **Updated F1-score**

>> 111111111

### 6. Settings of supervised methods in Section 4.2
> * ResNet Setting (batch size=50, learning rate=2e-6)
>> The following table is the structural parameters of the ResNet model.
>>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/ResNet.jpg)  
> * VggNet Setting (batch size=50, learning rate=2e-6)
>>> The following table is the structural parameters of the VggNet model.  
>>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/VggNet.jpg)  

> * GoogleNet Setting (batch size=50, learning rate=2e-6)
>>> The following table is the structural parameters of the GoogleNet model.
>>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/GoogleNet.jpg)  

### 7. Formula of V_S and V_T
>> Due to limited rebuttal space, the detail formulas please refer to:

>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/Vs.gif)
>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/Vt.gif)

>> where *n* is the batch size of a mini-batch.
