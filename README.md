# Wasserstein-K-means-for-clustering-probability-distributions

This repository contains Python and MATLAB codes generated by ourselves.

The codes are sourced from the following paper:

- Yubo Zhuang, Xiaohui Chen, and Yun Yang. *Wasserstein K-means for clustering probability distributions.* 2022. arXiv:2209.06975 [stat.ML].\
  https://arxiv.org/abs/2209.06975
  
  
The benchmark clustering data set and codes for calculating Sinkhorn divergence are sourced from the following resource:

- https://github.com/GiulsLu/Sinkhorn-Barycenters


# Background
Yubo Zhuang, Xiaohui Chen, and Yun Yang. *Wasserstein K-means for clustering probability distributions.* 
## The abstract of the paper
Clustering is an important exploratory data analysis technique to group objects based on their similarity. The widely used K-means clustering method relies on some notion of distance to partition data into a fewer number of groups. In the Euclidean space, centroid-based and distance-based formulations of the K-means are equivalent. In modern machine learning applications, data often arise as probability distributions and a natural generalization to handle measure-valued data is to use the optimal transport metric. Due to non-negative Alexandrov curvature of the Wasserstein space, barycenters suffer from regularity and non-robustness issues. The peculiar behaviors of Wasserstein barycenters may make the centroid-based formulation fail to represent the within-cluster data points, while the more direct distance-based K-means approach and its semidefinite program (SDP) relaxation are capable of recovering the true cluster labels. In the special case of clustering Gaussian distributions, we show that the SDP relaxed Wasserstein K-means can achieve exact recovery given the clusters are well-separated under the 2-Wasserstein metric. Our simulation and real data examples also demonstrate that distance-based K-means can achieve better classification performance over the standard centroid-based K-means for clustering probability distributions and images.


# This repository
## Purpose
The codes are considered for one case on dataset MNIST. The codes for other datasets are similar. We give the codes for two methods we proposed: Wasserstein SDP (W-SDP) and Distance-based Wasserstein K-means (D-WKM).

## Dependencies for Python
The core dependencies are:
 - PyTorch
 - NumPy

## Steps
 - On Python: download the codes from:\
   https://github.com/GiulsLu/Sinkhorn-Barycenters
 - Next run Main.py and get the results for D-WKM and the distance matrix for W-SDP  
 
 - On MATLAB: download and install the optimization toolbox SDPNAL+ from the following website:\
    https://blog.nus.edu.sg/mattohkc/softwares/sdpnalplus/ \
   Please download and install SDPNAL+ correctly following the instructions in the website. (Run SDPNALplus_Demo.m in toolbox SDPNAL+ to properly install it.)
 - Next run WSDP.m to get the results for WSDP based on the distance matrix obtained from Main.py.

## Contents
The files in this repository are:

- Main.py: The main Python code to get the results for D-WKM and the distance matrix for W-SDP.
- DWKM_utils.py: Provides the functions needed to calculate Bregman Wasserstein barycenter and related algorithms for D-WKM.
- WSDP.m: The MATLAB code to run SDP on the distance matrix and get results for W-SDP.
- kmeans_sdp_2.m: The MATLAB code for SDP.
- kmeansplus.m: The MATLAB code to run K-means+.
