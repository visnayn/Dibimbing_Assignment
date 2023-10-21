# Knowledge Graph Embedding with TransR Embedding

    References
    ----------
    * Yankai Lin, Zhiyuan Liu, Maosong Sun, Yang Liu, and Xuan Zhu.
      Learning Entity and Relation Embeddings for Knowledge Graph Completion. <https://www.aaai.org/ocs/index.php/AAAI/AAAI15/paper/view/9571/9523>
      In Twenty-Ninth AAAI Conference on Artificial Intelligence, February 2015

<hr>

## 0 Background Problem

Graph embedding is surely a challenge in machine learning field nowadays. With this embedding we can get the information of the nodes represented in the vector space based on its properties i.e. edges. 

There are some properties in knowledge graph that we need to take into account i.e. they are built from various entities that each of them has different type and attribute, and their edges is representeing different type of relation. 

From this problem, we suggest a research in TransR for KG Embedding. 
<hr>

## 1 Simple Explanation

The basic idea of TransR is illustrated in Fig. 1. For each
triple $(h, r, t)$ entities, which is representation of *(head, relation, tail)*, in the entity space are first projected into $r$-relation space as $h_r$ and $t_r$ with operation $M_r$, and then $\vec{h}_r + \vec{r} ≈ \vec{t}_r$. The relation-specific projection can make the head/tail entities that actually hold the relation (denoted
as colored circles) close with each other, and also get far
away from those that do not hold the relation (denoted as
colored triangles). The score function is defined as

$${f_r(h,t)} = ||\vec{h}_r + \vec{r} - \vec{t}_r||^{2}_{2}$$

Which we can tell that the function $f_r$ is euclidian distance of the difference between translation of $\vec{h}_r$ by $r$ with the vector $\vec{t}_r$.

Besides embedding, this method is known to be used for link prediction between two nodes.

<hr>

## 2 Goals

The goal of this experiment is to get complementary of job function in KitaLulus' dataset.

<hr>

## 3 Experiment Setup

The experiment consists of two which the one using example FB15K dataset and the one with Kitalulus' dataset. For further explanation of dependencies and result explanation of each experiment, you can get it directly in experiment directory. 
