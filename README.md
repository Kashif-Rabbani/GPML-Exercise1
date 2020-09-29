# Graph Powered Machine Learning Course 
## Exercise 1 
1.  Answers to all the three questions are available in the [RDFNotebook](https://github.com/Kashif-Rabbani/GPML-Exercises/blob/master/Exercise%201/1-RDFLib%20and%20Graphs.ipynb)
2.  Solution to PageRank question is available in the [PageRankNotebook](https://github.com/Kashif-Rabbani/GPML-Exercises/blob/master/Exercise%201/2-Pagerank.ipynb)

## Exercise 2 


### Part 1: A Comprehensive Survey on Graph Neural Networks

Read sections 1,2,3,6 of the [A Comprehensive Survey on Graph Neural Networks](https://arxiv.org/pdf/1901.00596v1.pdf) and discuss the following questions (roughly 1-2 paragraphs each):
1. **How are network embeddings and GCNs related?**
    
    Network embedding methods are closely related to GCNs, and both rely on the core assumption of homophily in the network. The former maps nodes to low-dimensional vector space embeddings without losing the network topology and node metadata while the later employs deep learning architectures/algorithms for graph-structured data. 

2. **What are the potential outputs of GCNs? Please describe one use-case for each potential output.**
    
    Since the specification of GCNs is unclear due to the description of the concept from the paper on page 3 (as shown in Figure below), therefore, we not only state the output of the different usages of Graph Convolutional Networks, but also the output and use cases of the different Graph Neural Network types.
    
    <img src="https://github.com/Kashif-Rabbani/GPML-Exercises/blob/master/Exercise%202/image.png" alt="drawing" width="400"/>
    
    GCNs have been used in multiple architectures, each with their own output. Multiple layers of GCN, with an intermediate step of applying a non-linear activation function to the convolutions, can be used to find the latent representation of nodes. This can be used for node classification. 
    
    GCNs can be used together with pooling, to find an overall representation of a graph, which can be used in graph classification.
    Using 	an Auto-encoder on the convolutions of a GCN, it is essentially possible to store an approximate representation of a graph using vectors. Using a decoder we can approximate the original graph. This can be used for storing large graphs.    

    **Graph Neural Network Output Types and Use Cases:**
    **Node classification** - Figuring out the label of an unclassified node. This can be done using general graph neural networks models. The general model aggregates information from its neighboring nodes. One use case could be genre classification on a network of movies, where some movies do not have a genre classified.
    
    **Graph embedding** - Finding a low dimensional representation of the graph which can be used for multiple purposes such as node prediction, link prediction, graph prediction, node similarity etc. One use case could be to find a low dimensional representation of a graph consisting of patients, disease and medication. The low dimensional representation could be used along with well established ML techniques, to find similarity between patients, whereby one could predict future disease for patients in the graph. Graph auto-encoders are used to create such a vector representation.
    
    **Graph generation** - From the structure and properties of one or several graphs, other similar graphs can be automatically generated using Graph Generative Networks. One application of this could be the discovery of new synthesizable molecules which possesses certain useful properties.
    Finding patterns from spatial-temporal graphs - Using graph spatial-temporal network models, we can extract spatial-temporal patterns. This could for example be used in road traffic forecasting.
    
    
3. **What are value is added by Graph Attention Networks over GCNs? What are potential disadvantage?**
    Overall, both are similar but the key difference is that graph attention networks employ attention mechanisms which assign larger weights to the more important nodes, walks, or models. We list down the following characteristics of GAN and GCN.
    1. GAN networks leverages self node features and neighbor features to train a model.
    2. GCN aggregates both self features and  the neighbor features.
    3. GCN  has a better way to represent neighbors aggregation.
    4. GCN can not handle unseen nodes while GAT can.

    As currently we are not sure about the intrinsics of the GAN, therefore stating any disadvantage can be subjective. 


4. **Why are GCNs relevant for Computer Vision?**
It explores the nearby relations embedded in a graph, as nearby pixels in a picture are more related to each other. Using large and small convolutions, we are able to find discriminative features in an image. By stacking convolutions, we are able to exploit inherent hierarchies in images. In the classification of a car, the windows will be a child of the car, the driver will be a child of the car, and the wheels will be a child of the car.
Also the convolutions does not depend on the dimensionality of an image (we can train the same model on a 56 x 56 image just as well as a 512 x 512 image).




### Part 2: Graph Learning Tasks

Pick one of the following Graph Learning Tasks from the DGL Guide and create a python tutorial (preferably as jupyter notebook) for that example. Feel free to choose another dataset [Kaggle](http://kaggle.com) is a good starting point.
1. Node Classification/Regression 
2. Edge Classification/Regression 
3. Link Prediction
4. Graph Classification


Solution to this task is available in the [Node classification with SAGE- Notebook](https://github.com/Kashif-Rabbani/GPML-Exercises/blob/master/Exercise%202/Node_classification_with_SAGE.ipynb) 
