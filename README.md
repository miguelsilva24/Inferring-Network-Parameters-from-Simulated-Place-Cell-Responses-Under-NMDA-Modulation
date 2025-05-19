# Inferring-Network-Parameters-from-Simulated-Place-Cell-Responses-Under-NMDA-Modulation

This notebook implements a biologically inspired 2D neural network model based on Leaky Integrate-and-Fire (LIF) neurons. The model simulates output activity maps in response to Gaussian sensory stimuli and allows control over key parameters such as the excitatory/inhibitory ratio (EI ratio), NMDA conductance, and synaptic noise level.

Bayesian inference is performed using the sbi library (Neural Posterior Estimation, NPE) to estimate these parameters from real experimental data. The goal is to find model configurations that reproduce the observed patterns in 10x10 neural activity maps.
