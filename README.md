# Geometric Deep Learning for EEG Data

## Overview

This repository is dedicated to exploring the application of Geometric Deep Learning on EEG data, focusing on its implications for Brain-Computer Interfaces (BCI). Our project delves into two main areas:

- **Graph Neural Networks (GNNs):** Investigating the performance of GNNs on the BCI Competition IV dataset.
- **Spherical Convolutional Neural Networks (Spherical CNNs):** Comparing their effectiveness against traditional Convolutional Neural Networks (CNNs) in handling EEG data.

## Objectives

Our research aims to achieve two primary goals:

### Graph Neural Networks on BCI Data

- **Examine manually constructed graphs** for EEG data analysis, including:
  - Random graphs.
  - Coherence-based graphs.
  - Physical distance-based graphs.
- **Explore dynamically constructed graphs** using a separate GNN, enhancing the adaptability and accuracy of EEG data interpretation.

## Dynamic Graph Structure Learning

Dynamic graph structure learning is pivotal in understanding the complex, evolving relationships in EEG data. Unlike static graphs, dynamic graphs adapt over time, capturing the transient and evolving nature of brain activity. This approach is especially beneficial for EEG data, where the relationships between electrodes (nodes) can change due to various factors such as mental states, tasks, or external stimuli.

Our methodology leverages a Graph Structure Learning (GSL) layer that learns optimal graph topologies within specified time intervals. This allows the model to adapt to changes in the data dynamically, improving accuracy and interpretability. The key aspects include:

- **Temporal Adaptation:** The GSL layer updates graph structures based on temporal changes, ensuring that the model remains relevant over different states of brain activity.
- **Resolution Specificity:** Graphs are learned over pre-defined time intervals, allowing for a balance between temporal resolution and computational efficiency. This method acknowledges that brain connectivity patterns can vary significantly over short periods.
- **Self-attention Mechanism:** Inspired by self-attention mechanisms in natural language processing, our GSL approach allows each node to dynamically adjust its connections based on the evolving context, mirroring the brain's adaptive nature.

<img width="971" alt="image" src="https://github.com/dzxterity/GDL_for_EEG/assets/24210513/ba4f4824-fce9-46ac-9717-8e48368b6a5c">


This dynamic construction not only enhances the model's ability to capture real-time changes in brain activity but also opens new avenues for interpreting complex brain signals, offering insights into the underlying mechanisms of cognitive processes and disorders.

For more technical details on the implementation and evaluation of dynamic graph structure learning in our project, refer to [Modeling Multivariate Biosignals With Graph Neural Networks and Structured State Space Models](https://arxiv.org/abs/2211.11176).



### Spherical CNNs vs. Traditional CNNs

- **Investigate the advantages of spherical convolutions** over periodic element-wise convolutions in conventional CNNs. Spherical convolutions consider the curvature of the surface where data points (electrodes in the EEG cap) are located, potentially improving model performance by leveraging the geometric properties of EEG data.

## Spherical Convolutional Neural Networks (Spherical CNNs)

Spherical CNNs extend the capabilities of traditional CNNs to handle data defined on spherical domains, leveraging spherical convolutions as their core operation. This adaptation is crucial for analyzing EEG data, where electrodes are naturally positioned on the approximately spherical surface of the human scalp. The key advantages of spherical CNNs include:

- **Rotation Equivariance**: Unlike traditional CNNs that are translation equivariant, spherical CNNs are rotation equivariant, making them highly suitable for EEG data analysis, where orientation and position on the scalp are variable.
- **Efficient Spherical Convolutions**: The paper introduces advancements in computing spherical convolutions, significantly enhancing the efficiency and scalability of spherical CNNs. This is achieved through novel implementations optimized for modern hardware accelerators and improvements in model components.
- **Application to EEG Data**: By accounting for the spherical geometry of the scalp, spherical CNNs can more accurately capture the spatial relationships between EEG electrodes, potentially improving the interpretability and performance of EEG data analysis.

These advancements enable spherical CNNs to tackle larger and more complex problems than previously possible, opening new avenues for deep learning applications in EEG data interpretation and beyond.

For more details on the implementation and advancements in spherical CNNs, and to explore the codebase, visit the [Spherical CNN GitHub repository](https://github.com/google-research/spherical-cnn).

For an in-depth understanding of the technical advancements and methodologies employed in spherical CNNs, refer to the paper on [arXiv](https://arxiv.org/abs/2306.05420).


## Methodology

- **Dataset:** Utilize the BCI Competition IV dataset, a benchmark for evaluating the effectiveness of various neural network architectures on EEG data.
- **Modeling Approach:**
  - Design and implement various graph structures for EEG data representation.
  - Compare spherical CNNs with traditional CNNs to assess the impact of incorporating surface curvature into neural network models.
