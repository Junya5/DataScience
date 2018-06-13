## 文献情况

### Deep learning approach to bacterial colony classification
```
2017-9-14,PLOS ONE
```
* 目的：识别细菌的属和种类可以通过计算机辅助方法实现，使得识别过程更加自动化
* 方法：应用了纹理分析的方法（利用深度卷积神经网络获取图像描述符，然后用支持向量机或随机森林进行编码和分类），对细菌的属和种类进行分类
* 数据库：DIBaS数据集（细菌种类的数字图像）包含660个图像，有33个不同的属和种类的细菌

* Local image descriptors：1.SIFT descriptors；2.CNN descriptors
* Pooling encoder：Gaussian Mixture Model (GMM)
* Classifier：SVM（Linear SVM, Polynomial SVM and RBF SVM），Random Forest（with
AdaBoost）

* 结果

![image](https://github.com/Junya5/DataScience/blob/master/ColonyDetection-Junya5/IMG/paperimg/paper1-1.png)


### Bacterial Colony Counting by Convolutional Neural Networks
```
January 1, 2017；Pattern Recognition
```
* 背景：固体琼脂上的细菌菌落计数是实验室自动化中必不可少但具有挑战性的计算机视觉任务。（数字微生物学影像应用领域）
* 比较两种方法：手动提取的形态和辐射特性+支持向量机；用卷积神经网络结构框架
* 数据集：（数字微生物学影像应用领域）28.5k
    - 图像采集
    - 图像标注：切割成包含不同菌落数量的小图（专用标注工具）
    - 数据增强：扩增（水平翻转、人工颜色失真、空间尺度改变）；标准化（CLAHE+方向校准）
* 分类任务
    - CNN classification
    - Handcrafted features classification
* 结果对比（多图）
    - 不同数据集的学习曲线（原始数据，经不同增强后的数据）
    - 不同比例训练集学习曲线和错误率
    - CNN方法和手动提取特征方法结果对比：confusion matrix, precision and recall，original percolony error metric


### Imaging, quantification and visualization of spatio-temporal patterning in mESC colonies under different culture conditions
```
2012-9-15；Bioinformatics
```
内容：开发了一种自动化的图像分析和群体跟踪框架，以获得对细胞群在空间和时间上的进化过程中结构特性的客观和可再生的量化，并为整个实验提供了一个基于流的可视化的个体菌落结构特征，便于对实验条件之间的差异进行视觉理解。
方法：用流体图像配准和图像分割来量化群体形状他和（内部）运动变化，可在一系列图像上动态地跟踪运动、分裂和合并。


## 预处理步骤

