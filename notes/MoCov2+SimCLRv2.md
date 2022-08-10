**MoCov2: Improved Baselines with Momentum Contrastive Learning**

添加了SimCLR中提到的数据增强，projector层等trick，维持MoCov1提到了queue和动量更新，在小batch下（256）得到了新的SOTA。



**SimCLRv2: Big Self-Supervised Models are Strong Semi-Supervised Learners**

总结了自监督学习的步骤：**Unsupervised Pre-train, Supervised Fine-tune.**

task-agnostic-》task-specific

半监督方法的步骤。任务未知无监督预训练，有监督微调，使用无标签样例进行蒸馏（与下游任务有关）

[Distilling the Knowledge in a Neural Network]

#### Contributions：

pre-train的模型deep和wide很重要，越大精度越高；

确定了下游任务就不需要大模型了

映射层很重要

![image-20220810172211175](/typoraimg/image-20220810172211175.png)

1.自监督预训练

具体做法：Encoder变deep和wide

projection变深（2FC+激活--->3FC，而且fine-tune的时候从FC第一层开始）

加入MoCo的queue和动量更新机制

2.有监督微调

保留部分projection层，和前面的encoder一起做微调

3.使用无标签数据进行蒸馏（就是算交叉熵）

第一部分蒸馏的交叉熵用soft-target来算

![image-20220810172912580](/typoraimg/image-20220810172912580.png)

![image-20220810173002784](/typoraimg/image-20220810173002784.png)

结合有监督标签，Student模型在T=1的条件下的softmax输出和ground truth的cross entropy，

最终蒸馏的loss为：

![image-20220810173143948](/typoraimg/image-20220810173143948.png)

具体实现：仅仅采用无标签数据进行蒸馏。作者采用了两种类型的蒸馏：自蒸馏与`Big-to-small`蒸馏

labeld sets即使用hardtarget作为蒸馏交叉熵损失计算

![image-20220810210212654](/typoraimg/image-20220810210212654.png)