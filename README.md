# Fuzzy Cycle Generative Advesarial Network
This page shows some results of supplementary experiments in rebuttal period of IJCAI2019. Detail description can be seen in rebuttal content.

## The list of experiments is as below:
> 1 cross-domain image generation

> 2 feature map visualization
  
> 3 t-SNE and PCA plots for different source objects
  
> 4 Occlution Test
  
> 5.Evaluation criteria and updated F1-scores

> 6.Settings of supervised methods in Section 4.2

> 7.Formula of V_S and V_T

> 8.Updated Algorithm 1

## Details of the experiments:
### 1. cross-domain image generation
>> image translation between (banana) source and (toxo and cell) target images in FCGAN and Cycle GAN. The red marker A in images denotes *T.gondii* parasite and B denotes host cell.

>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/generation.jpg)

>> FCGAN makes tranlated images remaining shape and texture information, and following the same background of the domain from where they generated. However, Cycle GAN make source and target images only follow mutual style translation. It demonstrates that our FCGAN can create texture and shape relationship between microscopic object and macroscopic object with wselecitivity of associated information.

### 2. feature map visualization
>> Take a 400X cell image as an example to show the feature map visualization.


>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/2671y_1.png)

>> Feture maps on 1-2 convolutional layers

>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/conv13.png)
>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/conv14.png)

>> Feture maps on last two convolutional layers

>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/conv24.png)
>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/conv25.png)


> From feature map visualization, it can be seen that shallow layers extract texture information and produce clear feature maps for these information, while deeper layer extract abstract features for clustering.

### 3. t-SNE and PCA plots for different source objects
>> We randomly select 1000 400X samples to extract features and do t-SNE and PCA plot for different source. The plot on left is t-SNE and the right is PCA plot.

>>> Plots for Toxo40 source

>>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/toxo_toxo40.png)

>>> Plots for Banana source

>>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/banana_40x.png)


>>> Plots for Crescent source

>>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/crescent_40X.png)

>>> Plots for Cat source
>>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/cat_toxo40.png)

### 4. Occlusion Test
>> We take a toxo and a cell under 400X microscope as examples to conduct occlusion Test. The image is obscured by a 64x64 mask step by step. 
>> If the obscured predicted probability is lower 0.35 than orginal image's, we note a -0.350 below the obscured image. If the probability is higher than original image, we note a +0.35 below the obscured image.

>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/banana_occlusion.jpg)

From the results of occlusion test, it can be seen that the outline is more important than internal area because the images which outline masked achieves a larger predicted probability loss than other area.

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

>> Updated results on T400 dataset

>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/T400.jpg)

>> Updated results on T1000 dataset

>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/T1000.jpg)

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

### 8. Updated Algorithm 1
>> We update specific initialization of parameters in Algorithm 1. As described in 7, V_S and V_T is an average value in network, so it meets the condition of back-progagation algorithm. Detail is as below:
>> ![Image text](https://github.com/fcgan/Rebuttal/blob/master/imgs/Algorithm.jpg)

## Thanks for your patient to visit this page observing our supplymentary experimental results. Thanks for your comments again.
