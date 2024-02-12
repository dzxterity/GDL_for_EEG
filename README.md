# Geometric Deep Learning for EEG Data
Overview
This repository is dedicated to exploring the application of Geometric Deep Learning on EEG data, focusing on its implications for Brain-Computer Interfaces (BCI). Our project delves into two main areas:

Graph Neural Networks (GNNs): Investigating the performance of GNNs on the BCI Competition IV dataset.
Spherical Convolutional Neural Networks (Spherical CNNs): Comparing their effectiveness against traditional Convolutional Neural Networks (CNNs) in handling EEG data.
Objectives
Our research aims to achieve two primary goals:

Graph Neural Networks on BCI Data
Examine manually constructed graphs for EEG data analysis, including:
Random graphs.
Coherence-based graphs.
Physical distance-based graphs.
Explore dynamically constructed graphs using a separate GNN, enhancing the adaptability and accuracy of EEG data interpretation.
Spherical CNNs vs. Traditional CNNs
Investigate the advantages of spherical convolutions over periodic element-wise convolutions in conventional CNNs. Spherical convolutions consider the curvature of the surface where data points (electrodes in the EEG cap) are located, potentially improving model performance by leveraging the geometric properties of EEG data.
Methodology
Dataset: Utilize the BCI Competition IV dataset, a benchmark for evaluating the effectiveness of various neural network architectures on EEG data.
Modeling Approach:
Design and implement various graph structures for EEG data representation.
Compare spherical CNNs with traditional CNNs to assess the impact of incorporating surface curvature into neural network models.
