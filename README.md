# Derive the Stellar Properties with Simulation-based Likelihood-free Inference| Advisor: Prof. Joshua Speagle  

## Research Outline:

### Introduction

- The importance of understanding the stars and the stellar parameters.
- How to get the stellar parameters, which can be inferred from modeling SED.
- Traditional methods used to infer stellar parameters.
- Drawbacks and challenges of using traditional Bayesian methods.
- Introduction to SBI and its weaknesses.
- Introducing the use of SBI++.

### Data

- Describe Brutus and how the theoretical model works
We used BRUTUS, an open-source Python package to generate simulated stellar spectral energy distributions (SEDs), based on grids of stellar models constrained by photometric and astrometric data. The intrinsic magnitudes are constructed using a combination of intrinsic parameters that incorporate stellar evolutionary models and stellar atmospheric models
combined with a given set of photometric filters. These are modified by extrinsic parameters including the distance, which can be compared to astrometric parallax measurements, and the visual extinction and “differential” reddening, which are based on empirical dust extinction models.


- Describe the 6 stellar parameters
We used a uniform prior for the six stellar parameters, the parameters included the initial mass of the star, stellar metallicity (Fe/H), EEP/100 (Equivalent Evolutionary Points), visual extinction (AV), differential reddening (RV) and log(distance).

- How we simulate the SED data:
Noise used: Adding noise to theoretical SEDs to mimic observational uncertainties. In order to align our training set with real-world observations, we introduce a degree of uncertainty to the training data by incorporating Gaussian noise. Specifically, we apply an error term of 0.02 for the standard SBI approach, while for the enhanced SBI++ approach, we adopt a uniform distribution of errors ranging from 0.02 to 0.1.

### Method

The primary goal of this study is to determine the posterior distributions of stellar parameters obtained through a Spectral Energy Distribution (SED) analysis. To achieve this, we employ a Sequential Neural Posterior Estimation (SNPE) framework, which combines Simulation-Based Inference (SBI) and leverages the power of Normalizing Flow. This approach models the posterior distributions based on a training dataset of simulated SEDs, enabling efficient and accurate parameter estimation. Through the use of simulated SEDs, SBI enables us to approximate the posterior distributions of the six stellar parameters in our model. This technique provides a flexible and versatile framework for parameter estimation, accommodating complex and high-dimensional parameter spaces.

Normalizing Flow is a probabilistic machine-learning method that transforms simple probability distributions into more complex ones through a series of invertible transformations.
By employing Normalizing Flows, our neural network can capture intricate relationships between the observed SEDs and the underlying stellar parameters.




