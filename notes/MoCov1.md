**论文名称：Momentum Contrast for Unsupervised Visual Representation Learning**

**论文地址：https://arxiv.org/abs/1911.05722**

**论文简介：CV领域中利用对比方法实现自监督学习**

前置知识

Self-Supervised Learning的目的一般是使用大量的无 label 的资料去 Pre-train 一个模型，这么做的原因是无 label 的资料获取比较容易，且数量一般相当庞大，我们希望先用这些廉价的资料获得一个预训练的模型，接着根据下游任务的不同在不同的有 label 数据集上进行 Fine-tune 即可。

无监督表示学习的第一种做法：生成式自监督学习。比如还原句子中被mask的字，或者还原图像中被mask的像素。（也称为代理任务）

区分于BERT做填空题：给一个句子随机盖住 (mask掉) 一个token，输入这个BERT，期望它输出盖住的部分。这就是BERT进行自监督学习的做法，那么在 MoCo等论文中是如何做的呢？一个核心的词汇叫做：**Contrastive**。**即试图教机器区分相似和不相似的事物**

![image-20220726213750149](/typoraimg/image-20220726213750149.png)



#### 1. Introduction

#### 2. Related Work

#### 3. Method

#### 4. Experiments

#### 5. Discussion and Conclusion

## Related Work

![image-20220729141220757](/typoraimg/image-20220729141220757.png)

第一种：end to end

query 和 key 表示的 encoder 通过反向传播进行端到端更新

这种方式 query 和 key 用两个 encoder，参数都需要进行更新的，负样本大小就是 batch 的大小

- 使用当前 batch 中的样本作为字典，共享一套参数
- 负样本数量取决于 batch 大小，受GPU显存大小限制

第二种：memory bank

维护一个字典，里面存储所有样本经过encoder离线算好的值，计算后对字典进行实时更新

这种方式存在不一致性：假设t1采样k个负样本，计算好q与k的loss对q的encoder进行了更新，将这个新的编码器对原来抽样出来的样本k进行重新的编码，生成新的特征，将原来的特征替换掉。理解：1.如果字典的 key 是由不同的编码器得到的，需要一整个epoch才更新所有的k，k和k之间存在差异，因此q对k进行查询时，不同的q,k之间的特征差的非常远；2.如果不对k进行更新，那么q，k之间又存在gap

## Method

因此，文章提出了使用了**基于队列**的动态字典来存储样本，同时又结合了**动量更新编码器**的方式，解决了编码器的快速变化降低了键的表征一致性问题。

将字典作为队列主要就是为了能将字典的大小和 mini-batch 分离开来，允许重用来自前面的 key ； 字典大小可以比典型的小批量大小大得多； 字典中的样本被逐步替换。最旧的key最新的query最不一致。（4096）

![image-20220729141236661](/typoraimg/image-20220729141236661.png)

动量参数 m 较大时，$\theta_k$ 的更新缓慢，不过多的依赖于 $\theta_q$ 当前时刻的编码器，即不随着当前时刻的编码器快速改变，尽可能保证 字典里的 key 都是由相似的编码器生成的特征，保证特征的 consistent


基于 large + consistent dynamic dictionary，MoCo 可以很好的无监督学习视觉特征。 

![image-20220729141243606](/typoraimg/image-20220729141243606.png)

![image-20220729141249015](/typoraimg/image-20220729141249015.png)

## Experiments

确定代理任务：moco使用的预训练任务是instance discrimination任务。一张图片经过不同的数据增强为正例，和其他图片的不同数据增强为负例。

![image-20220729141214706](/typoraimg/image-20220729141214706.png)

数据增强设置遵循的方法是：从一个随机调整大小的图像中提取224×224像素的裁剪，然后进行随机颜色抖动、随机水平翻转和随机灰度转换， 编码器可以是任意的卷积神经网络，fq和fk可以是完全相同的，也看可以是部分相同或不同的。本文用的是ResNet，其最后一个全连接层具有固定维数的输出——128维，这个输出由L2-范数进行归一化。

作者对比了三种对比机制的方式，实验结果发现MoCo不仅能支持更大的字典大小，而且也能带来更优的效果：

![image-20220729141257559](/typoraimg/image-20220729141257559.png)

同时对动量参数m进行消融实验，证明了动量更新的有效性。

![image-20220729141303379](/typoraimg/image-20220729141303379.png)

同时对比了其他有监督自监督方法，成为了SOTA，说明了之间的有监督和自监督的GAP已经极为微小

![image-20220729141310308](/typoraimg/image-20220729141310308.png)

## Discussion and Conclusion

![image-20220729141037188](/typoraimg/image-20220729141037188.png)

![image-20220729144219853](/typoraimg/image-20220729144219853.png)
