# PHYS448 FinalProject on CNN WaveformDenoising
PHYS448 final project on using CNN model to denoise HPGe detector waveform signals

This repository contains the code and results for a waveform denoising project using High-Purity Germanium (HPGe) detector data. The goal is to reconstruct clean waveforms from noisy measurements using a customized 1D Convolutional Neural Network (CNN) with an encoder–decoder architecture.
The project implements the model and training workflows in 

- Keras

- TensorFlow

- PyTorch

## Data Extraction

Waveforms were loaded from the MJD_Train_1.hdf5 dataset of the Majorana Demonstrator experiment.The notebook illustrates how  to choose waveforms with different features and modify the desired energy range. 

Here are the data: https://dataplanet.ucsd.edu/dataset.xhtml?persistentId=perma:83.ucsddata/UQWQAV

If you have further question, you can consult the paper: https://arxiv.org/abs/2308.10856

## CNN
This part of the code takes waveforms with artificially added noise at various SNR levels and feeds them into the CNN model, training the network to learn the mapping from noisy inputs to clean target waveforms.
- The notebook adds controllable noise to clean waveforms.
- CNN learns to reconstruct waveforms that closely preserve the true HPGe pulse shape while suppressing unwanted noise.
- After training, the model can denoise any input waveform,producing outputs with significantly reduced noise while maintaining essential pulse features such as the rising edge and amplitude.

## Fully-Connected NN
The fully connected neural network notebook provides a baseline model for waveform denoising. 
- The notebook adds controllable noise to clean waveforms.
- FCNN learns global waveform trends and performs basic noise suppression.
- After training, the model outputs a denoised waveform of the same length, offering a simple but interpretable reference point against which the CNN and RNN architectures can be compared.

## RNN
The RNN model treats each waveform as a sequential signal and processes it sample-by-sample using recurrent layers such as LSTM or GRU. 
- The notebook adds controllable noise to clean waveforms.
- RNN trains the network to reconstruct the corresponding clean sequences.
- After training, the model generates denoised waveforms that preserve temporal structure while reducing noise, providing an alternative sequence-based approach which can compare with the CNN and FCNN architechtures.
