# MLBP
Identifying multi-functional bioactive peptide functions using multi-label deep learning
使用多标签深度学习识别多功能生物活性肽功能

## Introduction
Motivation: 

The bioactive peptide has wide functions, such as lowering blood glucose levels and reducing inflammation. Meanwhile, computational methods such as machine learning are becoming more and more important for peptide functions prediction. Most of the previous studies concentrate on the single-functional bioactive peptides prediction. However, the number of multi-functional peptides is on the increase, therefore novel computational methods are needed.

Results: 

In this study, we develop a method MLBP (Multi-Label deep learning approach for determining the multi-functionalities of Bioactive Peptides), which can predict multiple functions including anti-cancer, anti-diabetic, anti-hypertensive, anti-inflammatory and anti-microbial simultaneously. MLBP model takes the peptide sequence vector as input to replace the biological and physiochemical features used in other peptides predictors. Using the embedding layer, the dense continuous feature vector is learnt from the sequence vector. Then, we extract convolution features from the feature vector through the convolutional neural network layer, and combine with the bidirectional gated recurrent unit layer to improve the prediction performance. The 5-fold cross-validation experiments are conducted on the training dataset, and the results show that Accuracy and Absolute true are 0.695 and 0.685, respectively. On the test dataset, Accuracy and Absolute true of MLBP are 0.709 and 0.697, with 5.0% and 4.7% higher than those of the suboptimum method, respectively. The results indicate MLBP has superior prediction performance on the multi-functional peptides identification.

Note:

On the benchmark dataset, expect AMPs have the length > 45, the vast majority of ACPs, ADPs, AHPs and AIPs are with length < 45. Thus, for the peptides with length ≤ 45, the prediction results of MLBP are accurate. If the peptides with length > 45, the prediction results for ACP, ADP, AHP and AIP are less accurate.
动机：生物活性肽具有广泛的功能，例如降低血糖水平和减少炎症。同时，机器学习等计算方法对于肽功能预测越来越重要。
以前的大多数研究都集中在单功能生物活性肽的预测上。然而，多功能肽的数量正在增加，因此需要新的计算方法。
结果：在本研究中，我们开发了一种方法 MLBP（用于确定生物活性肽多功能性的多标签深度学习方法），该方法可以预测多种功能，包括抗癌、抗糖尿病、抗高血压、抗炎和抗菌
同时进行。 MLBP 模型将肽序列向量作为输入来替换其他肽预测器中使用的生物和物理化学特征。
使用嵌入层，从序列向量中学习密集的连续特征向量。然后，我们通过卷积神经网络层从特征向量中提取卷积特征，并结合双向门控循环单元层来提高预测性能。在训练数据集上进行了 5 折交叉验证实验，结果表明 Accuracy 和 Absolute true 分别为 0.695 和 0.685。在测试数据集上，MLBP 的 Accuracy 和 Absolute true 分别为 0.709 和 0.697，分别比次优方法高 5.0% 和 4.7%。结果表明MLBP对多功能肽的鉴定具有优越的预测性能。注意：在基准数据集上，期望 AMP 的长度 > 45，绝大多数 ACP、ADP、AHP 和 AIP 的长度 < 45。因此，对于长度 ≤ 45 的肽段，MLBP 的预测结果是准确的。如果肽段长度 > 45，则 ACP、ADP、AHP 和 AIP 的预测结果不太准确。
![draft](./figures/framework.jpg)


## Related Files

#### MLBP

| FILE NAME           | DESCRIPTION                                                  |
| :------------------ | :----------------------------------------------------------- |
| main.py             | the main file of MLBP predictor (include data reading, encoding, and data partitioning) |
| train.py            | train model |
| model.py            | model construction |
| test.py             | test model result |
| evaluation.py       | evaluation metrics (for evaluating prediction results) |
| data                | data         |
| BiGRU_base          | models of MLBP           |


## Installation
- Requirement
  
  OS：
  
  - `Windows` ：Windows7 or later
  
  - `Linux`：Ubuntu 16.04 LTS or later
  
  Python：
  
  - `Python` >= 3.6
  
- Download `MLBP`to your computer

  ```bash
  git clone https://github.com/xialab-ahu/MLBP.git
  ```

- open the dir and install `requirement.txt` with `pip`

  ```
  cd MLBP
  pip install -r requirement.txt
  ```


## Run MLBP on a new test fasta file
```shell
python predictor.py --file test.fasta --out_path result
```

- `--file` : input the test file with fasta format

- `--out_path`: the output path of the predicted results


## Contact
Please feel free to contact us if you need any help.


## Citation
Tang W, Dai R, Yan W, et al. Identifying multi-functional bioactive peptide functions using multi-label deep learning[J]. Briefings in Bioinformatics, 2021.

