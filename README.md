# Cluster Counting with Spiking Neural Networks

## Overview

This repository contains the code used for the cluster-counting studies presented in our paper. The project investigates particle identification using spiking neural networks (SNNs) applied to detector time-series signals, focusing on pion, kaon, and proton discrimination.

The repository includes model training, inference, and performance comparison between machine-learning-based approaches and conventional cluster-counting methods.

## Repository Structure

### `TimeSeriesDataCode.ipynb`

Training notebook for the binary classification model (**v10**).

This notebook contains the complete workflow for:

* Data loading and preprocessing
* SNN model training
* Validation and testing
* Saving the trained binary classification model

The resulting model is used to distinguish between **pions and kaons**.

### `TimeSeriesData_3classes.ipynb`

Training notebook for the three-class classification model (**v12**).

This notebook extends the binary classification framework to perform classification among:

* Pions
* Kaons
* Protons

The notebook includes data preparation, training, validation, and model export.

### `PionsKaons.ipynb`

Inference and analysis notebook.

This notebook loads the trained models from:

* **v10** (2-class model)
* **v12** (3-class model)

and evaluates their performance on detector time-series data.

The final block of the notebook provides a direct comparison between:

* Ground-truth particle labels
* Binary classification results (**v10**, 2 classes)
* Multi-class classification results (**v12**, 3 classes)
* Traditional **D² derivative** cluster-counting method

This section contains the complete comparison of kaon separation performance and was used to generate the results presented in the paper.

## Usage

1. Run `TimeSeriesDataCode.ipynb` to train the binary classification model (**v10**).
2. Run `TimeSeriesData_3classes.ipynb` to train the three-class classification model (**v12**).
3. Run `PionsKaons.ipynb` to load the trained models and reproduce the evaluation results.
4. Execute the final notebook block to generate the comparison between:

   * Ground truth
   * v10 (2-class classification)
   * v12 (3-class classification)
   * D² derivative cluster-counting method
