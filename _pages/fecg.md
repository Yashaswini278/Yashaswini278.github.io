---
layout: page
title: fecg 
permalink: /fecg/
description: 
nav: false
nav_order: 1
#display_categories: [work, fun]
horizontal: false
---
In this project, a Residual Convolutional Autoencoder, was designed for continuous fetal well-being monitoring by separating fetal ECG signals from abdominal ECG data. Training data from the FECGSYNDB database was added with noise at various SNR levels and segmented for robust model training. Testing was performed on PCDB and ADFECG datasets, with preprocessing steps like filtering, normalization, and signal flipping to improve fetal R-peak detection accuracy. The model’s effectiveness was measured using Positive Predictive Value (PPV), Sensitivity, and F1 score, demonstrating high accuracy in fetal ECG signal extraction across diverse test cases​

<div style="text-align: center;">
  <img src="/assets/research/fecg1.png" alt="Image Description" style="width: 100%">
</div>

<div style="text-align: center;">
  <img src="/assets/research/fecg2.png" alt="Image Description" style="width: 100%">
</div>

