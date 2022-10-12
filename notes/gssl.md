Furthermore, the data examples (nodes) in graph data are correlated with the topological structure naturally, while the examples in CV (image) and NLP (text) are often independent. Hence, how to deal with such dependency in graph SSL becomes a challenge for pretext task designs.

对于CV和NLP任务，数据之间都是独立的，如果把类似的方法应用在graph上，有效吗？

节点丢弃，特征重建，这些都是有效的吗？





自建督学习任务的历史：

节点嵌入

These methods learn node representations by maximizing the agreement between contextual nodes within truncated random walks.

图自编码器

learns to rebuild the graph structure



文章贡献：

1. 通用框架和系统分类

   generation-based, auxiliary property-based, contrast-based, and hybrid methods.

2. 全面和实时的综述

3. 大量的资源和应用

4. 未来方向的前景

generation-based

feature and structure.  focus on the node/edge features or/and graph adjacency reconstructions.

Auxiliary property-based

Contrast-based graph SSL methods

Hybrid graph SSL methods
