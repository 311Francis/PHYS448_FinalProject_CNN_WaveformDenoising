# PHYS448_FinalProject_CNN_WaveformDenoising
PHYS448 final project on using CNN model to denoise HPGe detector waveform signals

This repository contains the code and results for a waveform denoising project using High-Purity Germanium (HPGe) detector data. The goal is to reconstruct clean waveforms from noisy measurements using a customized 1D Convolutional Neural Network (CNN) with an encoder–decoder architecture.
The project implements the model and training workflows in 

a. Keras

b. TensorFlow

c. PyTorch

##Data Extraction
Waveforms were loaded from the MJD_Train_1.hdf5 dataset of the Majorana Demonstrator experiment.The notebook illustrates how  to choose waveforms with different features and modify the desired energy range. 
