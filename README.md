# Inferring-Network-Parameters-from-Simulated-Place-Cell-Responses-Under-NMDA-Modulation

This notebook implements a biologically inspired 2D neural network model based on Leaky Integrate-and-Fire (LIF) neurons. The model simulates output activity maps in response to Gaussian sensory stimuli and allows control over key parameters such as the excitatory/inhibitory ratio (EI ratio), NMDA conductance, and synaptic noise level.

Bayesian inference is performed using the sbi library (Neural Posterior Estimation, NPE) to estimate these parameters from real experimental data. The goal is to find model configurations that reproduce the observed patterns in 10x10 neural activity maps.

## Repository Structure

This repository is organized into several modules to facilitate simulation, inference, and analysis of NMDA-related parameters using a 2D LIF neural network model:

### 0_Requirements
Contains setup needed to run the project.


### 1_NMDAModel
Implements the core neural network simulation model.

- 1_Model: Defines the main structure of the 2D LIF-based network.
- 2_Visualize_place_cell: Visualizes activity of simulated place cells.


### 2_NPE
Contains the scripts for training and applying the **Neural Posterior Estimation** (NPE) method.

- 1_Step_by_step_inference: A guided example to understand the NPE process.
- 2_Test_observation: Tests the trained model on simulated data.
- 3_Save_and_load_training_data: Scripts to persist or reload simulations and posteriors.


### 3_Inference_from_real_Place_Cells
Applies the trained model to real experimental data.

- 1_Test_with_1_place_cell: Runs inference on a single place cell.
- 2_Inference_for_all_place_cells: Runs inference across all recorded cells.


### 4_Visualization
Tools for analyzing and visualizing the results.

- 1_meanNMDA_dayswise_evolution: Tracks average NMDA conductance over time.
- 2_daily_histograms: Daily distributions of inferred values.
- 3_gaussian_fit: Fits Gaussian distributions to inferred data.
- 4_gaus_param_evolution: Follows evolution of Gaussian fit parameters.


## Reference Paper

This project is based on the computational model proposed in the study:

> **Zamani, A. et al.** (2022). *Anti-NMDAR encephalitis antibodies cause long-lasting degradation of the hippocampal neural representation of memory*. bioRxiv. https://doi.org/10.1101/2022.11.25.517901

In this work, the authors combined in vivo calcium imaging with behavioral assays and a computational model to investigate how anti-NMDAR antibodies disrupt hippocampal spatial memory in mice. Their computational model serves as the basis for this codebase, which expands the simulation and inference pipeline to study the impact of NMDA conductance reduction on CA1 neuronal dynamics and information encoding.

This repository reproduces and extends aspects of the computational modeling described in the article, providing tools for simulating, visualizing, and inferring the effects of NMDA receptor reduction in hippocampal networks.

