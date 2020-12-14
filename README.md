# PointNet_UseTest

This is a short try out with the PointNet architecture. Developed as part of my doctoral research, PointNet is an important part of my research. The application allows the use of raw PointCloud, and represents many advantages, especially in the use of depth data from an RGB-D camera.

## Orginal paper 

Here is the link to the original PoinNet paper, [https://arxiv.org/abs/1612.00593]. This paper is a reference in the use of 3D data. In a more global way and how often underlined in abstracts, modern methods aiming to find the position in space of an object use more and more often the depth image provided by the RGB-D camera. Methods based on e.g. key points or dense parameter fusion seem to be much more robust than more traditional methods and regularly use PointNet. Thus PointNet represents an important part and a key document in the understanding of many of the methods to be studied.

## Quick Talk about the architecture 

The classification network takes n points as input, applies input and feature transformations, and then aggregates the features of the points by maximum pooling. The result is a classification score for k classes. The segmentation network is an extension of the classification network. It concatenates global and local characteristics and point results. "mlp" stands for multi-layer perceptron, the numbers in brackets correspond to the size of the layers. Batchnorm is used for all layers with ReLU.

One of the main characteristics of this network is the input data provided to it. In net point effects unlike many networks created so far uses not meshes or complex 3D representations, but raw point clouds.

One of the first strong points of the cloud point compared to the mesh is its lightness, and also that it represents much less complex data than meshes.
This not only greatly improves the computational speed of the network, but also simplifies the complexity of learning (by simplifying the input data).

