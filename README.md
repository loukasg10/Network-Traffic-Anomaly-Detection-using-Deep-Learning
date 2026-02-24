# Time Series Analysis in Network Traffic: Anomaly Detection for Cybersecurity
This repository contains the experimental code and analysis notebooks for my B.Sc. Computer Science Thesis at the University of Crete.

## 📌 Project Overview
Accurate forecasting of network traffic is a crucial component of modern cybersecurity. This project evaluates the efficacy of Deep Learning methods (specifically Recurrent Neural Networks) for unsupervised anomaly identification in large-scale academic networks. 

By utilizing a "Global" training strategy and logarithmic scaling, we developed a lightweight 1-Layer Gated Recurrent Unit (GRU) that successfully models heterogeneous traffic and detects both point anomalies (volumetric spikes) and contextual anomalies (infrastructure failures).

* **Author:** Loukas Georgiou
* **Institution:** University of Crete, Computer Science Department

## 📊 Dataset
The experiments in this repository utilize the **CESNET-TimeSeries24** dataset. Due to size limitations, the raw data files are not hosted in this repository.
* The dataset can be accessed via the official researchers here:[https://arxiv.org/abs/2409.18874]](https://www.nature.com/articles/s41597-025-04603-x)

## 🚀 Key Findings
1. **Global > Local:** A single Global GRU model trained across 541 diverse subnets outperformed specialized clustered models with a **98.5% win rate** and zero catastrophic failures.
2. **Log-Scaling is Mandatory:** Logarithmic transformation of the input data was required to stabilize gradient descent against the extreme heavy-tailed nature of network traffic.
3. **Dynamic Anomaly Detection:** Implementing a rolling $3\sigma$ threshold allowed the system to successfully flag both volumetric DDoS-like spikes and hidden protocol-level outages.

## 🛠️ Repository Contents
* `Clustering_selection.ipynb`  
* `ETS_evaluation.ipynb`
* `Feature_Analysis.ipynb`
* `GRU_subnets.ipynb`
* `LSTM_clustered.ipynb`
* `Model_Results_Analysis.ipynb`
* `Institutions.ipynb`
* `Mean_evaluation.ipynb`


## 💻 Tech Stack
* Python 3.x
* PyTorch / PyTorch Lightning
* Darts (Time Series Machine Learning Library)
* Pandas & NumPy
* Matplotlib & Seaborn
