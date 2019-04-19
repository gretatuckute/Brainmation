# Animated brains, *Brainmation*
Toolbox for creating GIFs in Python based on neural time series data using [MNE](https://mne-tools.github.io/stable/index.html) and [Matplotlib](https://matplotlib.org/).

### Script information 
The script, *makeBrainmation.py*, loads sample EEG data, preprocesses EEG data epoch-wise and generates a topomap animation.
Running the script saves a sample GIF in the current working directory.

#### Functions within *makeBrainmation.py*
- createInfo: Creates an MNE info data structure.
- preprocEpoch: Preprocesses epoched (M)EEG data (in collaboration with [Sofie Therese Hansen](https://github.com/STherese)).
- createEpochsArray: Creates an MNE EpochsArray from a NumPy array containing (M)EEG data. Possibility of adding events/categories associated with individual trials.
- extractEvoked: Converts an MNE EpochsArray structure to an Evoked structure.

#### Example output 
![](https://raw.githubusercontent.com/gretatuckute/Brainmation/Brainmation_example.gif)

Example of a sensitivity map computed based on a SVM classifier separating animate/inanimate visual stimuli. The EEG signal was bandpass filtered to 1-25 Hz and downsampled to 100 Hz. Epochs of 600 ms (100 ms pre and 500 ms post stimulus onset) were extracted.

#### Acknowledgements

The implementation is based on:

- [MNE (MEG + EEG data analysis & visualization)](https://mne-tools.github.io/stable/index.html)

- [Matplotlib](https://matplotlib.org/). 

- 

