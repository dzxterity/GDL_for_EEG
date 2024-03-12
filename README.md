# Enhancing ECoG Signal Decoding: A Novel Approach to Directional Movement Classification

## Overview

This repository focuses on applying Geometric Deep Learning to ECoG data, specifically for advancing Brain-Computer Interfaces (BCI). Our project explores:

- **Graph Neural Networks (GNNs):** Performance of GNNs on the BCI Competition IV dataset.


## Objectives

### Graph Neural Networks on BCI Data

We aim to examine manually constructed graphs for ECoG data analysis, exploring:
- Random graphs.
- Coherence-based graphs, at varying thresholds.
- Physical distance-based graphs.

Additionally, we explore dynamically constructed graphs through a separate GNN to improve the adaptability and accuracy of ECoG data interpretation.

## ECoG Data Preprocessing Pipeline

The ECoG data preprocessing pipeline from the paper "FingerFlex: Inferring Finger Trajectories from ECoG signals" includes the following steps:

1. Multichannel ECoG data standardization and channel median subtraction.
2. Bandpass (40-300 Hz) and 50 Hz harmonics filtering.
3. Convolution with Morlet wavelets.
4. Downsampling from 1000 Hz to 100 Hz via decimation.
5. Scaling of the obtained features via RobustScaler.
6. Signal shift by delay hyperparameter to produce processed time-frequency features.

<img width="689" alt="Screenshot 2024-03-12 at 13 58 40" src="https://github.com/dzxterity/GDL_for_EEG/assets/24210513/64a37ff9-978d-4810-b1bc-43ecd13c288d">


For more details on the preprocessing steps for ECoG data, please refer to ["FingerFlex: Inferring Finger Trajectories from ECoG signals"](https://arxiv.org/abs/2211.01960).


### Manual Graph Construction for ECoG Signals

This section focuses on the influence of graph construction based on different thresholds of correlation/coherence of ECoG signals and compares the performances of neural networks with these varying graph constructions.

## Dynamic Graph Structure Learning

Dynamic graph structure learning is crucial for understanding the complex, evolving relationships in ECoG data. Our approach utilizes a Graph Structure Learning (GSL) layer to dynamically learn optimal graph topologies, incorporating temporal adaptation, resolution specificity, and a self-attention mechanism.

<img width="1395" alt="Screenshot 2024-03-12 at 13 48 12" src="https://github.com/dzxterity/GDL_for_EEG/assets/24210513/02e53f72-79f5-4d78-93f9-7fe7bcd489f5">


For more technical details on our dynamic graph structure learning methodology, refer to the paper ["Modeling Multivariate Biosignals With Graph Neural Networks and Structured State Space Models"](https://arxiv.org/abs/2211.11176).

## Mamba: Linear-Time Sequence Modeling with Selective State Spaces

Incorporating the Mamba architecture allows for linear-time sequence modeling with selective state spaces, enhancing our approach to decoding ECoG signals for directional movement classification.

<img width="1047" alt="Screenshot 2024-03-12 at 13 51 15" src="https://github.com/dzxterity/GDL_for_EEG/assets/24210513/b5cbf985-4ff7-4e3f-a32e-992c401ee2c4">

For more information on Mamba architecture, refer to the paper ["Mamba: Linear-Time Sequence Modeling with Selective State Spaces"](https://arxiv.org/abs/2312.00752).


## Methodology

- **Dataset:** Utilizing the BCI Competition IV dataset as a benchmark.
- **Modeling Approach:** Designing and implementing various graph structures for ECoG data representation.

