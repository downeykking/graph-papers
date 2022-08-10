**论文名称：A Simple Framework for Contrastive Learning of Visual Representations**

**论文地址：**https://arxiv.org/pdf/2002.05709.pdf

这篇SimCLR工作，数据增强更复杂；在encoder后再加了一层projector，（单纯的encoder保留了和数据增强变换相关的信息，非线性层的作用就是去掉这些信息，让表示回归数据的本质）；batch设置大，增加更多负样本

![image-20220729141201124](.\typoraimg\image-20220729141201124.png)

**SimCLR细节**

假设现在有**1张**任意的图片 ![[公式]](https://www.zhihu.com/equation?tex=x) ，叫做Original Image，先对它做数据增强，得到2张增强以后的图片 ![[公式]](https://www.zhihu.com/equation?tex=x_i%2Cx_j) 。数据增强的方式有以下3种：

- 随机裁剪之后再resize成原来的大小 (Random cropping followed by resize back to the original size)。
- 随机色彩失真 (Random color distortions)。
- 随机高斯模糊 (Random Gaussian Deblur)。

接下来把增强后的图片 ![[公式]](https://www.zhihu.com/equation?tex=x_i%2Cx_j) 输入到Encoder里面，注意这2个Encoder是共享参数的，得到representation ![[公式]](https://www.zhihu.com/equation?tex=h_i%2Ch_j) ，再把 ![[公式]](https://www.zhihu.com/equation?tex=h_i%2Ch_j) 继续通过 Projection head 得到 representation ![[公式]](https://www.zhihu.com/equation?tex=z_i%2Cz_j) ，这里的2个 Projection head 依旧是共享参数的。

![img](https://pic4.zhimg.com/80/v2-a64b94ff65e2c03598ddfc5fe41dd57f_720w.jpg)

即此时对于小batch N，生成2N*2N的相似度矩阵，对于一个样本有一个正样本和2N-2个负样本。

![image-20220729151246879](.\typoraimg\image-20220729151246879.png)

![image-20220729150947417](.\typoraimg\image-20220729150947417.png)

![image-20220729151046803](.\typoraimg\image-20220729151046803.png)

因此可行的优化方向为：增加view难度、增加更多负例、提升encoder表现等





**论文名称：GraphCL: Graph Contrastive Learning with Augmentations**

**论文地址：**https://arxiv.org/pdf/2010.13902.pdf

### Intro：

为什么要做自监督？1.图数据很大，标签不够，2.自监督泛化性更好

GAE：过分强调邻接性，可能损害结构信息

为什么要对比学习？手工设计的前置任务依赖启发式设计，丧失了泛化性。

相比之下，对比学习的目的是通过在不同的增强视图下最大化特征一致性来学习表示，这些增强视图利用数据或任务特定的增强[33]来注入所需的特征不变性。

### Methodology：

图数据不同于图片，其可能来自不同领域，生化分子(例如化合物、蛋白质)，社交网络，图像super-pixel图

四种增强方式

![image-20220718204506993](.\typoraimg\image-20220718204506993.png)

图对比学习四大步骤：图数据增强，图编码器，映射头，对比损失函数

在训练完成后使用图编码器完成下游任务

### Experiments：

![image-20220724211351044](.\typoraimg\image-20220724211351044.png)

图对比学习中数据增强的必要性：

1. 如果没有任何数据增强图，对比学习是没有帮助的，从图2右上角的准确性损失来看，对比学习往往比从零开始的训练更糟糕。相比之下，构建一个原始的图并对其进行适当的扩展可以有利于下游的性能。从图2最上面的行或最右边的列来看，使用单一最佳增强的图对比学习在没有彻底超参数调优的情况下取得了相当大的改进:NCI1为1.62%，PROTEINS为3.15%，COLLAB为6.27%，RDT-B为1.66%。

![image-20220724211522532](.\typoraimg\image-20220724211522532.png)

2. 组合不同的增强功能会带来更多好处（如图2）

  对比不同类型的同质图对对于图表示学习来说是一个更困难但更有用的任务

  在优化过程不变的情况下，对于不同类型的增强对，对比损失的下降速度始终比相同类型的增强对慢。这一结果表明，组合不同类型的增强对确实对应一个“更难”的对比预测任务。

![image-20220724211447518](.\typoraimg\image-20220724211447518.png)

3. 组合增强方法有益实验效果；对于领域特定的任务，不同的增强模式会带来相应的提升或损失，符合先验认知

   Edge perturbation benefits social networks but hurts some biochemical molecules；

   Applying attribute masking achieves better performance in denser graphs.

   ![image-20220724211224953](.\typoraimg\image-20220724211224953.png)

4. 节点删除和子图通常在各个数据集上都比较有效

   ![image-20220724211432139](.\typoraimg\image-20220724211432139.png)

##### 和SOTA的比较

半监督学习对比：GAE, InfoMax

![image-20220724211835699](.\typoraimg\image-20220724211835699.png)

无监督学习对比：生成图嵌入，并将其输入到下游SVM分类器中。除了graphlet核(GL)、Weisfeiler-Lehman子树核(WL)和深度图核(DGK)等SOTA图核方法外，还比较了node2vec、sub2vec、graph2vec和InfoGraph这四种无监督图级表示学习方法。

![image-20220724212003241](.\typoraimg\image-20220724212003241.png)

迁移学习：化学中的分子性质预测和生物学中的蛋白质功能预测进行迁移学习，在不同的数据集上对模型进行预训练和微调，以评估预训练方案的可迁移性。

![image-20220724212045662](.\typoraimg\image-20220724212045662.png)

提升了鲁棒性：面对RandSampling、GradArgmax和RL-S2V的攻击，GraphCL相比从头训练提高了GNN的鲁棒性。

![image-20220724212148062](.\typoraimg\image-20220724212148062.png)

![image-20220729143842327](.\typoraimg\image-20220729143842327.png)

![image-20220729143755230](.\typoraimg\image-20220729143755230.png)
