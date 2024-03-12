# Enhancing ECoG Signal Decoding: A Novel Approach to Directional Movement Classification

## Overview

This repository focuses on applying Geometric Deep Learning to ECoG data, specifically for advancing Brain-Computer Interfaces (BCI). Our project explores two main areas:

- **Graph Neural Networks (GNNs):** Performance of GNNs on the BCI Competition IV dataset.
- **Spherical Convolutional Neural Networks (Spherical CNNs):** Comparison of their effectiveness against traditional Convolutional Neural Networks (CNNs) in ECoG data analysis.

## Objectives

### Graph Neural Networks on BCI Data

We aim to examine manually constructed graphs for ECoG data analysis, exploring:
- Random graphs.
- Coherence-based graphs, at varying thresholds.
- Physical distance-based graphs.

Additionally, we explore dynamically constructed graphs through a separate GNN to improve the adaptability and accuracy of ECoG data interpretation.

### Manual Graph Construction for ECoG Signals

This section focuses on the influence of graph construction based on different thresholds of correlation/coherence of ECoG signals and compares the performances of neural networks with these varying graph constructions.

## Dynamic Graph Structure Learning

Dynamic graph structure learning is crucial for understanding the complex, evolving relationships in ECoG data. Our approach utilizes a Graph Structure Learning (GSL) layer to dynamically learn optimal graph topologies, incorporating temporal adaptation, resolution specificity, and a self-attention mechanism.

![Dynamic Graph Structure Learning Visualization](https://github.com/dzxterity/GDL_for_ECoG/assets/24210513/ba4f4824-fce9-46ac-9717-8e48368b6a5c)

### Spherical CNNs vs. Traditional CNNs

We investigate the advantages of spherical CNNs over traditional CNNs, highlighting the importance of considering the curvature of the scalp in ECoG data analysis.

## Spherical Convolutional Neural Networks (Spherical CNNs)

Spherical CNNs are tailored for data defined on spherical domains, offering rotation equivariance and efficient spherical convolutions, which are particularly suited for analyzing ECoG data.

![Spherical CNNs Visualization](https://github.com/dzxterity/GDL_for_ECoG/assets/24210513/a8955607-a6d5-486f-9302-0ff88228d189)

## Mamba: Linear-Time Sequence Modeling with Selective State Spaces

Incorporating the Mamba architecture allows for linear-time sequence modeling with selective state spaces, enhancing our approach to decoding ECoG signals for directional movement classification.

## Methodology

- **Dataset:** Utilizing the BCI Competition IV dataset as a benchmark.
- **Modeling Approach:** Designing and implementing various graph structures for ECoG data representation and comparing spherical CNNs with traditional CNNs.

