**论文名称：Spectral Graph Neural Network**

**论文地址：https://arxiv.org/abs/1905.12265**

**论文简介：谱图神经网络**

## Abstract

图神经网络的核心工作是对空间域(Spatial Domain)中节点的Embedding进行卷积操作(即聚合邻居Embedding信息)，然而图数据和图像数据的差别在于节点邻居个数、次序都是不定的，因此传统用于图像上的CNN模型中的卷积操作(Convolution Operator)不能直接用在图上，因此需要从频谱域(Spectral Domain)上重新定义这样的卷积操作再通过卷积定理转换回空间域上。

为了在频谱域和空间域中转换，我们借助了傅里叶公式，并且定义了图上傅里叶变换(从空间域变换到频谱域)和图上傅里叶逆变换(从频谱域回到空间域)的变换公式。具体操作是我们将节点的Embedding $f(i), i\in (1, \cdots, N)$通过傅里叶正变换从空间域变换到了频谱域，$\hat{f}$在频谱域上和卷积核$h$进行卷积操作，再将变换后的节点Embedding通过傅里叶逆变换回到空间域，参与后续的分类等任务。



图在频谱域上的表示：**谱图理论**，谱图理论主要研究的是图的拉普拉斯(Lapalacian)矩阵的特征值和所对应的特征向量对于图拓扑性质的影响

#### 



### 定义

对于**无向图** G=(V,E)G=(V,E)，其Laplacian矩阵定义为L=D−AL=D−A，其中DD是节点的度矩阵(只在对角线上有元素)，AA是图的邻接矩阵。拉普拉斯矩阵还有几种扩展定义：

- Lsys==D−1/2LD−1/2Lsys==D−1/2LD−1/2 称为对称正规拉普拉斯矩阵(Symmetric Normalized Laplacian)，论文中一般用的是这种Laplacian的定义。
- Lrw=D−1LLrw=D−1L 称为随机游走正规拉普拉斯矩阵(Random Walk Normalized Laplacian)。

由于L=D−AL=D−A，且无向图中DD为对称矩阵，因此拉普拉斯矩阵是对称矩阵，可以进行特征分解(谱分解)，谱分解对于图从空间域到频谱域的变换至关重要，因为我们用来变换的工具傅里叶变换(Fourier Transform)需要利用Laplacian矩阵的特征值和特征向量，通过变换，从**拓扑结构的图**(spatial domain)到**拉普拉斯矩阵**再到**谱图**(spectral domain)这条链路就形成了。下面就先来介绍拉普拉斯矩阵的谱分解。


