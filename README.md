# graph-papers

Graph Neural Network, Self-Supervised Learning, Contrastive Learning, RecSys, Transformer Papers Reading Notes.

Updating~



## 1. Survey or Benchmark

- [ ] TKDE'22 Self-Supervised Learning for Recommender Systems: A Survey [[Paper](https://arxiv.org/abs/2203.15876)] [Code] [Link]
- [x] TKDE'22 Graph Self-Supervised Learning: A Survey [[Paper](https://arxiv.org/abs/2103.00111)] [Code] [Link]
- [x] TKDE'21 Self-supervised Learning on Graphs: Contrastive, Generative,or Predictive [[Paper](https://arxiv.org/abs/2105.07342)] [Code] [Link]
- [x] TKDE'21 Self-supervised Learning: Generative or Contrastive [[Paper](https://arxiv.org/abs/2006.08218)] [Code] [Link]
- [x] Dataset@NIPS'21 An Empirical Study of Graph Contrastive Learning [[Paper](https://arxiv.org/abs/2109.01116)] [Code] [Link]
- [ ] arXiv'21 A Survey of Transformers [[Paper](https://arxiv.org/abs/2106.04554)] [Code] [[Link](https://www.bilibili.com/video/BV1sU4y1G7CN/)]

[Paper] [Code] [Link]



## 2. Graph Embedding

- [ ] KDD'17 **metapath2vec**: Scalable Representation Learning for Heterogeneous Networks [[Paper](https://dl.acm.org/doi/pdf/10.1145/3097983.3098036)] [[Code](https://github.com/linbang/Metapath2vec)] [Link] 
- [ ] KDD'16 **SDNE**: Structural Deep Network Embedding [[Paper](http://www.kdd.org/kdd2016/papers/files/rfp0191-wangAemb.pdf)] [[Code](https://github.com/suanrong/SDNE)] [[Link](https://zhuanlan.zhihu.com/p/413468532)]
- [ ] KDD'16 **node2vec**: Scalable Feature Learning for Networks [[Paper](https://arxiv.org/abs/1607.00653)] [[Code](https://github.com/eliorc/node2vec)] [[Link](https://zhuanlan.zhihu.com/p/413046898)]
- [ ] WWW'15 **LINE**: Large-scale Information Network Embedding [[Paper](https://arxiv.org/abs/1503.03578)] [[Code](https://github.com/snowkylin/line)] [[Link](https://zhuanlan.zhihu.com/p/412787557)]
- [x] KDD'14 **DeepWalk**: Online Learning of Social Representations [[Paper](https://arxiv.org/abs/1403.6652)] [[Code](https://github.com/phanein/deepwalk)] [[Link](https://zhuanlan.zhihu.com/p/412713441)]
- [x] NeurIPS'13  **word2vec**: Distributed Representations of Words and Phrases and their Compositionality [[Paper](https://arxiv.org/abs/1310.4546)] [[Code](https://github.com/brijml/mikolov_word2vec)] [[Link](https://zhuanlan.zhihu.com/p/413169135)]

[Paper] [Code] [Link]



## 3. Data Augment

- [ ] WWW'22 Augmentations in Graph Contrastive Learning: Current Methodological Flaws & Towards Better Practices [[Paper](https://arxiv.org/abs/2111.03220)] [Code] [Link]
- [ ] arXiv'22 Data Augmentation for Deep Graph Learning: A Survey [[Paper](https://arxiv.org/abs/2202.08235.pdf)] [No Code] [[Link](https://zhuanlan.zhihu.com/p/492146847)]
- [ ] WWW'21 Mixup for Node and Graph Classification [[Paper]](https://wangywust.github.io/Paper/2021mix.pdf) [[Code](https://github.com/vanoracai/MixupForGraph)] [[Link](https://zhuanlan.zhihu.com/p/377635385)]
- [x] WSDM'21 **GraphSMOTE**: Imbalanced Node Classification on Graphs with Graph Neural Networks [[Paper](https://arxiv.org/abs/2103.08826)] [[Code](https://github.com/TianxiangZhao/GraphSmote)] [[Link](https://zhuanlan.zhihu.com/p/463233535)]

[Paper] [Code] [Link]



## 4. Self-supervised Learning -- Contrastive

#### Methods

- [ ] ICLR'23 Link Prediction with Non-Contrastive Learning [[Paper](https://arxiv.org/abs/2211.14394)] [[Code](https://github.com/snap-research/non-contrastive-link-prediction)] [Link]
- [ ] AAAI'23 Beyond Smoothing: Unsupervised Graph Representation Learning with Edge Heterophily Discriminating [[Paper](https://arxiv.org/pdf/2211.14065.pdf)] [[Code](https://github.com/yixinliu233/GREET)] [Link]
- [ ] AAAI'23 **MA-GCL**: Model Augmentation Tricks for Graph Contrastive Learning [[Paper](https://arxiv.org/pdf/2212.07035.pdf)] [[Code](https://github.com/GXM1141/MA-GCL)] [Link]
- [ ] AAAI'23 **SFA**: Spectral Feature Augmentation for Graph Contrastive Learning and Beyond [[Paper](https://arxiv.org/abs/2212.01026)] [Code] [[Link](https://zhuanlan.zhihu.com/p/589174216)]
- [x] AAAI'22 **AFGRL**: Augmentation-Free Self-Supervised Learning on Graphs [[Paper](https://arxiv.org/abs/2112.02472)] [[Code](https://github.com/Namkyeong/AFGRL)] [[Link](./notes/afgrl.md)]
- [x] NIPS'22 **GGD**: Rethinking and Scaling Up Graph Contrastive Learning: An Extremely Efficient Approach with Group Discrimination [[Paper](https://arxiv.org/abs/2206.01535)] [[Code](https://github.com/zyzisastudyreallyhardguy/Graph-Group-Discrimination)] [[Link](./notes/GGD.md)]
- [x] AAAA'22 **SUGRL**: Simple Unsupervised Graph Representation Learning [[Paper](https://www.aaai.org/AAAI22Papers/AAAI-3999.MoY.pdf)] [[Code](https://github.com/YujieMo/SUGRL)] [[Link1](./notes/SUGRL.md)] [[Link2](https://zhuanlan.zhihu.com/p/493269474)]
- [ ] TNNLS'22 Prototypical Graph Contrastive Learning [[Paper](https://arxiv.org/abs/2106.09645)] [[Code](https://github.com/ha-lins/PGCL)] [Link] 
- [ ] ICML'21 **JOAO**: Graph Contrastive Learning Automated [[Paper](https://arxiv.org/abs/2106.07594)] [[Code](https://github.com/Shen-Lab/GraphCL_Automated)] [Link]
- [ ] IJCAI'21 Multi-Scale Contrastive Siamese Networks for Self-Supervised Graph Representation Learning [[Paper](https://arxiv.org/abs/2105.05682)] [[Code](https://github.com/GRAND-Lab/MERIT)] [Link]
- [x] Workshop@ICLR'21 **BRGL**: Bootstrapped Representation Learning on Graphs [[Paper](https://arxiv.org/abs/2102.06514v1)] [[Code](https://github.com/nerdslab/bgrl)] [[Link](./notes/BGRL.md)]
- [x] NIPS'21 **CCA-SSG**: From Canonical Correlation Analysis to Self-supervised Graph Neural Networks [[Paper](https://arxiv.org/abs/2106.12484)] [[Code](https://github.com/hengruizhang98/CCA-SSG)] [[Link](./notes/ccassg.md)]
- [x] WWW'21 **GCA**: Graph Contrastive Learning with Adaptive Augmentation [[Paper](https://arxiv.org/abs/2010.14945.pdf)] [[Code](https://github.com/CRIPAC-DIG/GCA)] [[Link](./notes/GCA.md)]
- [x] ICML'20 **MVGRL**: Contrastive Multi-View Representation Learning on Graphs [[Paper]](https://arxiv.org/abs/2006.05582) [[Code](https://github.com/kavehhassani/mvgrl)] [[Link](./notes/MVGRL.md)]
- [x] Workshop@ICML'20 **GRACE**: Deep Graph Contrastive Representation Learning [[Paper](https://arxiv.org/abs/2006.04131.pdf)] [[Code](https://github.com/CRIPAC-DIG/GRACE)] [[Link](./notes/GRACE.md)]
- [x] ICLR'20 **InfoGraph**: Unsupervised and Semi-Supervised Graph-level Representation Learning via Mutual Information Maximization [[Paper](https://arxiv.org/abs/1908.01000.pdf)] [[Code](https://github.com/fanyun-sun/InfoGraph)] [[Link](./notes/InfoGraph.md)]
- [x] NIPS'20 **GraphCL**: Graph Contrastive Learning with Augmentations [[Paper](https://arxiv.org/abs/2010.13902.pdf)] [[Code](https://github.com/Shen-Lab/GraphCL)] [[Link](./notes/SimCLRv1+GraphCL.md)]
- [x] NIPS'20 Supervised Contrastive Learning [[Paper](https://arxiv.org/pdf/2004.11362.pdf)] [[Code](https://github.com/HobbitLong/SupContrast)] [[Link1](https://zhuanlan.zhihu.com/p/136332151)] [[Link2](https://zhuanlan.zhihu.com/p/265529937)]
- [x] WWW'20 **GMI**: Graph Representation Learning via Graphical Mutual Information Maximization [[Paper](https://arxiv.org/abs/2002.01169)] [[Code](https://github.com/zpeng27/GMI)] [[Link](./notes/GMI.md)]
- [x] ICLR'19 **DGI**: Deep Graph Infomax [[Paper](https://arxiv.org/abs/1809.10341)] [[Code](https://github.com/PetarV-/DGI)] [[Link](./notes/DGI.md)]

### Theories:

- [ ] ICLR'23 A theoretical study of inductive biases in contrastive learning [[Paper](https://openreview.net/forum?id=AuEgNlEAmed)] [Code] [Link] [[OpenReview](https://openreview.net/forum?id=AuEgNlEAmed)]
- [ ] ICLR'23 Towards the Generalization of Contrastive Self-Supervised Learning [[Paper](https://arxiv.org/abs/2111.00743)] [[Code](https://github.com/huang-research-group/contrastive2021)] [[Link](https://zhuanlan.zhihu.com/p/435175976)] [[OpenReview](https://openreview.net/forum?id=XDJwuEYHhme)]
- [ ] CVPR'22 Node Representation Learning in Graph via Node-to-Neighbourhood Mutual Information Maximization [[Paper](https://arxiv.org/abs/2203.12265)] [[Code](https://github.com/dongwei156/n2n)] [Link]
- [x] ECCV'22 Decoupled Contrastive Learning [[Paper](https://arxiv.org/abs/2110.06848)] [Code] [[Link](https://zhuanlan.zhihu.com/p/435349353)]
- [ ] ICLR'22 Equivariant Contrastive Learning [[Paper](https://arxiv.org/abs/2111.00899)] [[Code](https://github.com/rdangovs/essl)] [[Link](https://zhuanlan.zhihu.com/p/431302624)]
- [ ] ICLR'21 What Should Not Be Contrastive in Contrastive Learning [[Paper](https://arxiv.org/abs/2008.05659)] [Code] [Link]
- [ ] ICML'21 Understanding Self-Supervised Learning Dynamics without Contrastive Pairs [[Paper](https://arxiv.org/abs/2102.06810)] [[Code](https://github.com/facebookresearch/luckmatters/tree/master/ssl)] [[Link](https://zhuanlan.zhihu.com/p/384818506)]
- [ ] CVPR'21 Understanding the Behaviour of Contrastive Loss [[Paper](https://arxiv.org/pdf/2012.09740.pdf)] [Code] [[Link](https://zhuanlan.zhihu.com/p/357071960)]
- [x] ICML'20 Understanding Contrastive Representation Learning through Alignment and Uniformity on the Hypersphere [[Paper](https://arxiv.org/abs/2005.10242)] [[Code](https://github.com/SsnL/align_uniform)] [[Link1](https://mp.weixin.qq.com/s/MteoquDoks4kuVPA9jzT_Q)] [[Link2](https://blog.csdn.net/c2a2o2/article/details/117898108)]

[Paper] [Code] [Link]



## 5. Self-Supervised Learning -- Generative

- [x] KDD'22 **GraphMAE**: Self-Supervised Masked Graph Autoencoders [[Paper](https://arxiv.org/abs/2205.10803)] [[Code](https://github.com/thudm/graphmae)] [[Link](./notes/graphmae.md)]
- [ ] arXiv'22 **MaskGAE**: Masked Graph Modeling Meets Graph Autoencoders [[Paper](https://arxiv.org/abs/2205.10053)] [[Code](https://github.com/EdisonLeeeee/MaskGAE)] [Link]

[Paper] [Code] [Link]



## 6. Self-supervised Learning -- Pretrain

- [x] ICLR'20 Strategies for Pre-training Graph Neural Networks [[Paper](https://arxiv.org/abs/1905.12265.pdf)] [[Code](https://github.com/snap-stanford/pretrain-gnns/)] [[Link](./notes/PretrainICLR20.md)]
- [x] KDD'20 **GCC**: Graph Contrastive Coding for Graph Neural Network Pre-training [[Paper](https://arxiv.org/abs/2006.09963)] [[Code](https://github.com/THUDM/GCC)] [[Link](./notes/GCC.md)]

[Paper] [Code] [Link]



## 7. Heterogeneous Graph

- [ ] WWW'20 Heterogeneous Graph Transformer [[Paper](https://arxiv.org/abs/2003.01332)] [[Code](https://github.com/acbull/pyHGT)] [Link]

[Paper] [Code] [Link]



## 8. Graph Anomaly Detection

- [ ] ICML'22 Rethinking Graph Neural Networks for Anomaly Detection [[Paper](https://arxiv.org/abs/2205.15508)] [[Code](https://github.com/squareroot3/rethinking-anomaly-detection)] [Link]

[Paper] [Code] [Link]



## 9. NLP And CV And RecSys In Contrastive Learning

#### Computer Vision：

- [ ] **InsDis**: Unsupervised Feature Learning via Non-Parametric Instance-level Discrimination [[Paper](https://arxiv.org/abs/1805.01978)] [[Code](https://github.com/zhirongw/lemniscate.pytorch)] [Link]
- [x] **Deep Infomax**: Learning deep representations by mutual information estimation and maximization [[Paper](https://arxiv.org/abs/1808.06670)] [Code] [Link]
- [ ] **CPC**: Representation Learning with Contrastive Predictive Coding [[Paper](https://arxiv.org/pdf/1807.03748.pdf)] [Code] [Link]
- [x] **CMC**: Contrastive Multiview Coding [[Paper](https://arxiv.org/abs/1906.05849)] [[Code](https://github.com/HobbitLong/CMC)] [Link]
- [ ] **InfoMin**: What Makes for Good Views for Contrastive Learning? [[Paper](https://arxiv.org/abs/2005.10243)] [[Code](https://github.com/HobbitLong/PyContrast)] [[Link1](https://hobbitlong.github.io/InfoMin/)] [[Link2](https://zhuanlan.zhihu.com/p/150736322)]
- [ ] **PCL**: Prototypical Contrastive Learning of Unsupervised Representations [[Paper](https://arxiv.org/abs/2005.04966)] [[Code](https://github.com/salesforce/PCL)] [Link]
- [x] **MoCo v1**: Momentum Contrast for Unsupervised Visual Representation Learning [[Paper](https://arxiv.org/abs/1911.05722)] [[Code](https://github.com/facebookresearch/moco)] [[Link](./notes/MoCov1.md)]
- [x] **SimCLR v1**: A Simple Framework for Contrastive Learning of Visual Representations [[Paper](https://arxiv.org/abs/2002.05709)] [[Code](https://github.com/google-research/simclr)] [[Link](./notes/SimCLRv1+GraphCL.md)]
- [x] **MoCo v2**: Improved Baselines with Momentum Contrastive Learning [[Paper](https://arxiv.org/abs/2003.04297)] [[Code](https://github.com/facebookresearch/moco)] [[Link](./notes/MoCov2+SimCLRv2.md)]
- [x] **SimCLR v2**: Big Self-Supervised Models are Strong Semi-Supervised Learners [[Paper](https://arxiv.org/abs/2006.10029)] [[Code](https://github.com/google-research/simclr)] [[Link](./notes/MoCov2+SimCLRv2.md)]
- [x] **SwAV**: Unsupervised Learning of Visual Features by Contrasting Cluster Assignments [[Paper](https://arxiv.org/abs/2006.09882)] [[Code](https://github.com/facebookresearch/swav)] [[Link](./notes/SwAV.md)]
- [x] **BYOL**: Bootstrap your own latent: A new approach to self-supervised Learning [[Paper](https://arxiv.org/abs/2006.07733)] [[Code](https://github.com/lucidrains/byol-pytorch)] [[Link](./notes/byol.md)]
- [x] **SimSiam**: Exploring Simple Siamese Representation Learning [[Paper](https://arxiv.org/abs/2011.10566)] [[Code](https://github.com/facebookresearch/simsiam)] [[Link](https://zhuanlan.zhihu.com/p/308159909)]
- [ ] **MoCo v3**: An Empirical Study of Training Self-Supervised Vision Transformers [[Paper](https://arxiv.org/abs/2104.02057)] [[Code](https://github.com/facebookresearch/moco-v3)] [Link]
- [x] **Barlow Twins**: Self-Supervised Learning via Redundancy Reduction [[Paper](https://arxiv.org/abs/2103.03230)] [[Code](https://github.com/facebookresearch/barlowtwins)] [[Link](./notes/barlowtwins.md)] 
- [ ] **VICReg**: Variance-Invariance-Covariance Regularization for Self-Supervised Learning [[Paper](https://arxiv.org/abs/2105.04906)] [[Code](https://github.com/facebookresearch/vicreg)] [Link]
- [x] **MEC**: Self-Supervised Learning via Maximum Entropy Coding [[Paper](https://arxiv.org/abs/2210.11464)] [[Code](https://github.com/xinliu20/mec)] [[Link](./notes/MEC.md)]
- [ ] ICCV'21 Weakly Supervised Contrastive Learning [[Paper](https://arxiv.org/abs/2110.04770)] [[Code](https://github.com/kyle-1997/WCL)] [Link]
- [ ] PMLR'21 Dissecting Supervised Contrastive Learning [[Paper](https://arxiv.org/abs/2102.08817)] [[Code](https://github.com/plus-rkwitt/py_supcon_vs_ce)] [Link]
- [ ] CVPR'22 Targeted Supervised Contrastive Learning for Long-Tailed Recognition [[Paper](https://arxiv.org/abs/2111.13998)] [[Code](https://github.com/lth14/targeted-supcon)] [Link]

[Paper] [Code] [Link]

#### Natural Language Processing：

- [x] **SimCSE**: Simple Contrastive Learning of Sentence Embeddings [[Paper](https://arxiv.org/abs/2104.08821)] [[Code](https://github.com/princeton-nlp/SimCSE)] [[Link](https://zhuanlan.zhihu.com/p/368353121)]

[Paper] [Code] [Link]

#### Recommender System：

- [ ] SIGIR'22 Are Graph Augmentations Necessary? Simple Graph Contrastive Learning for Recommendation [[Paper](https://arxiv.org/abs/2112.08679)] [[Code](https://github.com/Coder-Yu/QRec)] [Link]
- [ ] WWW'22 **NCL**: Improving Graph Collaborative Filtering with Neighborhood-enriched Contrastive Learning [[Paper](https://arxiv.org/abs/2202.06200)] [[Code](https://github.com/rucaibox/ncl)] [Link]
- [ ] SIGRI'21 **SGL**: Self-supervised Graph Learning for Recommendation [[Paper](https://arxiv.org/abs/2010.10783)] [[Code](https://github.com/wujcan/SGL-Torch)] [[Link](./notes/sgl.md)]

[Paper] [Code] [Link]



## 10. RecSys

- [ ] SIGIR'20 **LightGCN**: Simplifying and Powering Graph Convolution Network for Recommendation [[Paper](https://arxiv.org/abs/2002.02126)] [[Code](https://github.com/gusye1234/LightGCN-PyTorch)] [Link]
- [ ] KDD'20 Embedding-based Retrieval in Facebook Search [[Paper](https://dl.acm.org/doi/pdf/10.1145/3394486.3403305)] [Code] [[Link](https://www.zhihu.com/question/315120636/answer/1687203383)]
- [ ] SIGIR‘19 **NGCF**: Neural Graph Collaborative Filtering [[Paper](https://arxiv.org/abs/1905.08108)] [[Code](https://github.com/huangtinglin/NGCF-PyTorch)] [Link]
- [ ] KDD'18 PinSAGE: Graph Convolutional Neural Networks for Web-Scale Recommender Systems [[Paper](https://arxiv.org/abs/1806.01973)] [Code] [[Link](https://zhuanlan.zhihu.com/p/275942839)]

[Paper] [Code] [Link]



## 11. Graph Model

References: https://pytorch-geometric.readthedocs.io/en/latest/modules/nn.html#convolutional-layers

- [ ] GCN
- [ ] Chebnet
- [ ] GraphSAGE
- [ ] GraphConv
- [ ] APPNP
- [ ] GAT
- [ ] Transformer

[Paper] [Code] [Link]



## 12. Transformer

#### nlp:

#### cv:

- [ ] TPAMI'22 Pyramid Pooling Transformer for Scene Understanding [[Paper](https://github.com/yuhuan-wu/P2T)] [[Code](https://github.com/yuhuan-wu/P2T)] [[Link](https://mp.weixin.qq.com/s/7qXtyFaIiYny0eUqBbPraQ)]
- [ ] AAAI'22 Less is More: Pay Less Attention in Vision Transformers [[Paper](https://arxiv.org/pdf/2105.14217.pdf)] [[Code](https://github.com/ziplab/LIT)] [Link]
- [ ] ICML'21 **ViLT**: Vision-and-Language Transformer Without Convolution or Region Supervision [[Paper](https://arxiv.org/abs/2102.03334)] [[Code](https://github.com/dandelin/vilt)] [Link]
- [ ] ICLR'21 **ViT**: An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale [[Paper](https://arxiv.org/abs/2010.11929)] [[Code](https://github.com/google-research/vision_transformer)] [Link] 
- [ ] ICCV'21 **Swin Transformer**: Hierarchical Vision Transformer using Shifted Windows [[Paper](https://arxiv.org/abs/2103.14030)] [[Code](https://github.com/microsoft/Swin-Transformer)] [Link]
- [ ] ICCV'20 **DETR**: End-to-End Object Detection with Transformers [[Paper](https://arxiv.org/abs/2005.12872v3)] [[Code](https://github.com/facebookresearch/detr)] [Link]

[Paper] [Code] [Link]

#### graph: 

Papers about graph transformers: [awesome-graph-transformer](https://github.com/ChandlerBang/awesome-graph-transformer)

- [ ] ICLR'23 **NAGphormer**: A Tokenized Graph Transformer for Node Classification in Large Graphs [[Paper](https://openreview.net/forum?id=8KYeilT3Ow)] [[Code](https://github.com/JHL-HUST/NAGphormer)] [Link]
- [ ] NIPS'22 Hierarchical Graph Transformer with Adaptive Node Sampling [[Paper](https://arxiv.org/abs/2210.03930)] [[Code](https://github.com/zaixizhang/ANS-GT)] [Link]
- [ ] NIPS'22 Recipe for a General, Powerful, Scalable Graph Transformer [[Paper](https://arxiv.org/pdf/2205.12454.pdf)] [Code] [Link]
- [x] NIPS'22 **NodeFormer**: A Scalable Graph Structure Learning Transformer for Node Classification [[Paper](https://openreview.net/forum?id=sMezXGG5So)] [[Code](https://github.com/qitianwu/NodeFormer)] [[Link](./notes/nodeformer.md)]
- [ ] WWW'22 Universal Graph Transformer Self-Attention Networks [[Paper](https://arxiv.org/abs/1909.11855)] [[Code](https://github.com/daiquocnguyen/Graph-Transformer)] [Link]
- [x] Workshop@AAAI'21 A Generalization of Transformer Networks to Graphs [[Paper](https://arxiv.org/abs/2012.09699)] [[Code](https://github.com/graphdeeplearning/graphtransformer)] [[Link](./notes/basegraphtransformer)]

[Paper] [Code] [Link]