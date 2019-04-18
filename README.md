# NeuralGIF
Code for creating GIFs in Python based on neural time series data.

### Script information 

c

The script, *computeSensitivityMap.py* fits a SVM classifier based on the input data matrix and label array, and computes the corresponding sensitivity map. 

#### Inputs 
- X: EEG data 2d matrix containing trials as rows, and features (channels * time points) as columns.
- y: List/NumPy array containing binary class labels, y = {-1, 1}.
- C: SVM classifier regularization parameter. 
- Gamma: Free parameter of the RBF kernel, SVM classifier.

#### Outputs
- s_matrix: sensitivity map matrix.
- plt: Visualization of the sensitivity map.

#### Example function call
computeSensitivityMap(X, y, C_val = 1, gamma_val = 0.0005, no_channels = 32, no_timepoints = 60)

#### Example output 
![alt text](https://raw.githubusercontent.com/gretatuckute/DecodingSensitivityMapping/master/Example/sensitivity_map.png)

Example of a sensitivity map computed based on a SVM classifier separating animate/inanimate visual stimuli. The EEG signal was bandpass filtered to 1-25 Hz and downsampled to 100 Hz. Epochs of 600 ms (100 ms pre and 500 ms post stimulus onset) were extracted.

#### Acknowledgements

The implementation is based on the projects:

- TensorFlow implementation of VGG-19 'neural-style-tf' by [cysmith](https://github.com/cysmith/neural-style-tf).

- Brain surface reconstruction is made with [Freesurfer 6.0.0](https://surfer.nmr.mgh.harvard.edu/) and processed in [MeshLab](http://www.meshlab.net/). 

