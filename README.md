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

This dynamic construction not only enhances the model's ability to capture real-time changes in brain activity but also opens new avenues for interpreting complex brain signals, offering insights into the underlying mechanisms of cognitive processes and disorders.

For more technical details on the implementation and evaluation of dynamic graph structure learning in our project, refer to [Modeling Multivariate Biosignals With Graph Neural Networks and Structured State Space Models](https://arxiv.org/abs/2211.11176).



### Spherical CNNs vs. Traditional CNNs

- **Investigate the advantages of spherical convolutions** over periodic element-wise convolutions in conventional CNNs. Spherical convolutions consider the curvature of the surface where data points (electrodes in the EEG cap) are located, potentially improving model performance by leveraging the geometric properties of EEG data.

## Methodology

- **Dataset:** Utilize the BCI Competition IV dataset, a benchmark for evaluating the effectiveness of various neural network architectures on EEG data.
- **Modeling Approach:**
  - Design and implement various graph structures for EEG data representation.
  - Compare spherical CNNs with traditional CNNs to assess the impact of incorporating surface curvature into neural network models.
