# Fault_Classification_PMU_Data

This project focuses on the classification of faults in electrical transmission lines and photovoltaic (PV) systems using ensemble learning methods and deep learning models. The datasets used in this project include fault data from transmission lines (PMU data) and a grid-connected PV system, providing comprehensive insights into various fault scenarios.

Table of Contents
Project Overview
Datasets
Transmission Line Fault Dataset
Grid-Connected PV System Fault Dataset
Models Developed
Support Vector Machine (SVM)
Convolutional Neural Network - Long Short-Term Memory (CNN-LSTM)
Temporal Convolutional Network (TCN)
Results
Usage
References
Project Overview
This project aims to build robust models to detect and classify faults in both transmission lines and PV systems. By leveraging advanced machine learning techniques and deep learning architectures, we improve fault detection accuracy and reliability in power systems.

Datasets

1. Transmission Line Fault Dataset
   This dataset consists of 134,406 samples with 14 columns (13 features and 1 target label). The features include three-phase sinusoidal current and voltage measurements (Ia, Ib, Ic, Va, Vb, Vc), their magnitudes (Im, Vm), frequency (Fi, Fv), and phase angles (Pai, Pav). The dataset captures both symmetrical and unsymmetrical faults, which are labeled as NF (No Fault), L-G (Line to Ground), LL (Line to Line), LL-G (Double Line to Ground), LLL (Three Phase), and LLL-G (Three Phase to Ground). The dataset spans a time range of 0 to 5.7 seconds, collected at high-frequency intervals.

2. Grid-Connected PV System Fault Dataset
   The Grid-Connected PV System Faults (GPVS-Faults) dataset includes 2,163,480 samples with 15 columns (14 features and 1 target label). The dataset consists of data from 16 experimental scenarios that cover various PV system faults, such as array faults, inverter faults, grid anomalies, feedback sensor faults, and MPPT controller faults. Measurements include PV array current (Ipv), voltage (Vpv), DC voltage (Vdc), three-phase current (ia, ib, ic) and voltage (va, vb, vc), their magnitudes (Iabc, Vabc), and frequencies (If, Vf). Each fault scenario is represented by a unique identifier and collected at a high-frequency sampling interval (9.9989 μs).

Models Developed

1. Support Vector Machine (SVM)
   A classical machine learning model used to classify faults in both datasets.
   Provided a baseline accuracy by effectively separating classes in lower-dimensional spaces.
   Achieved an overall accuracy of 85% on the transmission line dataset and 83% on the PV system dataset.
2. Convolutional Neural Network - Long Short-Term Memory (CNN-LSTM)
   A hybrid model combining CNN for feature extraction and LSTM for temporal pattern recognition.
   Suitable for capturing spatial and temporal dependencies in high-frequency time-series data.
   Achieved an accuracy of 92% on the transmission line dataset and 89% on the PV system dataset, outperforming the SVM model in terms of fault detection accuracy.
3. Temporal Convolutional Network (TCN)
   A deep learning model designed for sequential data, capable of modeling long-range dependencies.
   Demonstrated superior performance in detecting and classifying faults by leveraging dilated convolutions.
   Achieved the highest accuracy of 94% on the transmission line dataset and 91% on the PV system dataset, with a significant reduction in training time compared to CNN-LSTM.
   Results
   Transmission Line Fault Classification:
   SVM: 85% accuracy
   CNN-LSTM: 92% accuracy
   TCN: 94% accuracy
   PV System Fault Classification:
   SVM: 83% accuracy
   CNN-LSTM: 89% accuracy
   TCN: 91% accuracy
   The Temporal Convolutional Network (TCN) outperformed other models in both datasets, making it the preferred choice for fault classification in power systems.
