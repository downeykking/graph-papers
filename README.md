# graph-papers
关于graph，recsys，contrastive learning等论文笔记

updating~

## 1. Graph Embedding

- [ ] KDD'16 Structural Deep Network Embedding [[Paper](http://www.kdd.org/kdd2016/papers/files/rfp0191-wangAemb.pdf)] [[Code](https://github.com/suanrong/SDNE)] [[Link](https://zhuanlan.zhihu.com/p/413468532)]
- [ ] KDD'16 node2vec: Scalable Feature Learning for Networks [[Paper](https://arxiv.org/abs/1607.00653)] [[Code](https://github.com/eliorc/node2vec)] [[Link](https://zhuanlan.zhihu.com/p/413046898)]
- [ ] WWW'15 LINE: Large-scale Information Network Embedding [[Paper](https://arxiv.org/abs/1503.03578)] [[Code](https://github.com/snowkylin/line)] [[Link](https://zhuanlan.zhihu.com/p/412787557)]
- [x] KDD'14 DeepWalk: Online Learning of Social Representations [[Paper](https://arxiv.org/abs/1403.6652)] [[Code](https://github.com/phanein/deepwalk)] [[Link](https://zhuanlan.zhihu.com/p/412713441)]
- [x] NeurIPS'13  Distributed Representations of Words and Phrases and their Compositionality [[Paper](https://arxiv.org/abs/1310.4546)] [[Code](https://github.com/brijml/mikolov_word2vec)] [[Link](https://zhuanlan.zhihu.com/p/413169135)]

## 2. Data augment

- [ ] ArXiv'22 Data Augmentation for Deep Graph Learning: A Survey [[Paper](https://arxiv.org/abs/2202.08235.pdf)] [No Code] [[Link](https://zhuanlan.zhihu.com/p/492146847)]
- [ ] WWW'21 Mixup for Node and Graph Classification [[Paper]](https://wangywust.github.io/Paper/2021mix.pdf) [[Code](https://github.com/vanoracai/MixupForGraph)] [[Link](https://zhuanlan.zhihu.com/p/377635385)]

把mixup方法引进graph，通过two branch聚合pair节点的属性和邻居节点信息（融合无法插值的拓扑结构的信息），通过two stage解决 conflicts between the Mixup on different node pairs，对graph-level的embedding进行插值以实现图分类

- [ ] WSDM'21 GraphSMOTE: Imbalanced Node Classification on Graphs with Graph Neural Networks [[Paper](https://arxiv.org/abs/2103.08826)] [[Code](https://github.com/TianxiangZhao/GraphSmote)] [[Link](https://zhuanlan.zhihu.com/p/463233535)]

## 3.Self-Supervised Learning -- Contrastive

- [ ] WWW'21 GCA: Graph Contrastive Learning with Adaptive Augmentation [[Paper](https://arxiv.org/abs/2010.14945.pdf)] [[Code](https://github.com/CRIPAC-DIG/GCA)] [Link]

- [ ] ICML'20 GRACE: Deep Graph Contrastive Representation Learning [[Paper](https://arxiv.org/abs/2006.04131.pdf)] [[Code](https://github.com/CRIPAC-DIG/GRACE)] [Link]

- [ ] ICLR'20 InfoGraph: Unsupervised and Semi-Supervised Graph-level Representation Learning via Mutual Information Maximization [[Paper](https://arxiv.org/abs/1908.01000.pdf)] [[Code](https://github.com/fanyun-sun/InfoGraph)] [Link]

- [ ] ICLR'20 Strategies for Pre-training Graph Neural Networks [[Paper](https://arxiv.org/abs/1905.12265.pdf)] [[Code](https://github.com/snap-stanford/pretrain-gnns/)] [Link]

- [ ] KDD'20 GCC: Graph Contrastive Coding for Graph Neural Network Pre-training [[Paper](https://arxiv.org/abs/2006.09963)] [[Code](https://github.com/THUDM/GCC)] [Link]

- [x] NIPS'20 GraphCL: Graph Contrastive Learning with Augmentations [[Paper](https://arxiv.org/abs/2010.13902.pdf)] [[Code](https://github.com/Shen-Lab/GraphCL)] [[Link](./notes/SimCLRv1+GraphCL.md)]

- [ ] ICLR'19 DGI: Deep Graph Infomax [[Paper](https://arxiv.org/abs/1809.10341)] [[Code](https://github.com/PetarV-/DGI)] [Link]



## 4. Self-Supervised Learning -- Generative

- [ ] Arxiv'22 MaskGAE: Masked Graph Modeling Meets Graph Autoencoders [[Paper](https://arxiv.org/abs/2205.10053)] [[Code](https://github.com/EdisonLeeeee/MaskGAE)] [Link]
- [ ] KDD'22 GraphMAE: Self-Supervised Masked Graph Autoencoders [[Paper](https://arxiv.org/abs/2205.10803)] [[Code](https://github.com/thudm/graphmae)] [Link]



## 5. Heterogeneous Graph

- [ ] WWW'20 Heterogeneous Graph Transformer [[Paper](https://arxiv.org/abs/2003.01332)] [[Code](https://github.com/acbull/pyHGT)] [Link]

## 6. NLP AND CV

- [x] MoCo v1: Momentum Contrast for Unsupervised Visual Representation Learning [[Paper](https://arxiv.org/abs/1911.05722)] [[Code](https://github.com/facebookresearch/moco)] [[Link](./notes/MoCov1.md)]

- [x] SimCLR v1: A Simple Framework for Contrastive Learning of Visual Representations [[Paper](https://arxiv.org/abs/2002.05709)] [[Code](https://github.com/google-research/simclr)] [[Link](./notes/SimCLRv1+GraphCL.md)]

- [x] MoCo v2: Improved Baselines with Momentum Contrastive Learning [[Paper](https://arxiv.org/abs/2003.04297)] [[Code](https://github.com/facebookresearch/moco)] [Link]

- [x] SimCLR v2: Big Self-Supervised Models are Strong Semi-Supervised Learners [[Paper](https://arxiv.org/abs/2006.10029)] [[Code](https://github.com/google-research/simclr)] [Link]
- [ ] SWaV
- [ ] BYOL
- [ ] SimSiam

- [ ] MoCo v3: An Empirical Study of Training Self-Supervised Vision Transformers [[Paper](https://arxiv.org/abs/2104.02057)] [[Code](https://github.com/facebookresearch/moco-v3)] [Link]







[Paper] [Code] [Link]

