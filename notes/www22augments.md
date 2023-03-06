**论文名称：Augmentations in Graph Contrastive Learning: Current
Methodological Flaws & Towards Better Practices**

**论文地址：**

**论文简介：**

## Abstract

视觉对比学习的成功归因于使用与任务相关的增强和大型、多样化的数据集。但图对比学习尽管使用了数量级较小的数据集，并使用了领域不确定图增强，也取得了强大的性能。

#### 1. Introduction

通过使用适当的数据扩充，视觉对比学习框架学习了与下游任务性能无关的属性不变的高质量表示;从而保留任务相关的属性。大型、多样化的数据集是必要的，因为VCL框架通常在批处理中使用1K-8K样本，以确保有足够的负面视图可用于稳定的训练。

但GCL框架经常偏离这些关键原则。此外，由于图的非欧离散性质，很难设计与任务相关的图数据扩充，也很难知道哪些不变性对下游任务有用。因此，框架通常依赖于领域不可知图增强(DAGAs)[87]。然而，daga会破坏任务相关的信息产生无效/假阳性样本(见图1)。对于下游任务，daga是否诱导有用或语义上有意义的不变性也不清楚。

#### 2. Related Work



#### 3. Method



#### 4. Experiments



#### 5. Discussion and Conclusion


