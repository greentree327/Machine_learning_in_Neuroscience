# Using Machine Learning to Decode fNIRS Data

## Project Supervision
- Professor Benjamin BECKER, The University of Hong Kong
- Miss. Michelle Tsang (Post-doctoral researcher), The University of Hong Kong

## Project Link
[Read the full article on Medium](https://medium.com/@jackson3b04/using-machine-learning-to-decode-fnirs-data-f5cb3aab1291)

## Overview
This research investigates cognitive reappraisal through neurofeedback-based training using functional near-infrared spectroscopy (fNIRS). The study employs various analytical approaches including correlation matrices, repeated-measures ANOVA, and machine learning methods like Support Vector Machines (SVM).

## Key Hypotheses
1. Brain activity in the lateral prefrontal cortex (lPFC) will increase across training runs during reappraisal trials
2. Cognitive reappraisal enhances connectivity in the lPFC ROI more strongly for the experimental neurofeedback group
3. SVM classifier can distinguish between regulation and view conditions
4. SVM classifier accuracy significantly differs from random guessing

## Methods

### fNIRS Data Preprocessing Pipeline
![fNIRS data preprocessing pipeline diagram](https://github.com/user-attachments/assets/d21167e4-0caa-48bd-8342-d21f4903a7c3)

### Signal Processing Steps
1. Raw intensity data collection
2. Bad data filtering & channel selection
3. Optical density conversion
4. Scalp coupling index (SCI) calculation
5. Motion correction using wavelet-based method
6. Bandpass filtering
7. Conversion to haemoglobin concentration
8. Motion correction using CBSI

### Region of Interest (ROI)
![fNIRS cap configuration with lateral PFC ROI](https://github.com/user-attachments/assets/df70dab2-e73e-4d59-92c1-ee756e082dae)

## Results

### Connectivity Analysis
![Correlation matrices](path/to/figure8.png)

### Time Series Analysis
![Grand average of oxygenated haemoglobin brain activity](path/to/figure9.png)

### Training Effects
![Neurofeedback group results](path/to/figure12a.png)
![Neurofeedback group statistics](path/to/figure12b.png)
![Sham group results](path/to/figure13a.png)
![Sham group statistics](path/to/figure13b.png)

### Machine Learning Classification
![Confusion Matrix](path/to/figure15.png)

## Key Findings
- Significant increase in brain activity between neurofeedback training sessions 2 and 3
- Enhanced functional connectivity during reappraisal tasks in the neurofeedback group
- SVM classifier achieved 77.78% accuracy in distinguishing between conditions
- Statistical significance confirmed through chi-square test (χ² = 4.43, p = 0.0353)

## Code Notebooks
- [Time Series Analysis](https://colab.research.google.com/drive/1FihVOAB9FzkabtAvvs_wnaAwZkQ5U6hC)
- [Training Effect Analysis](https://colab.research.google.com/drive/1RwM6ios_9bD7f5zta75dY4O4DW6fxYOc?usp=sharing)
- [SVM Classification](https://colab.research.google.com/drive/1evaWxqxLImmzlgWtz8NJu5lWMRY8HMFS#scrollTo=nF-cLnec8Vxs)

## Future Directions
- Investigation of additional statistical predictors
- Development of more sophisticated temporal feature analysis
- Enhancement of signal-to-noise ratio in machine learning models

## References
1. Berboth, S., & Morawetz, C. (2021). Amygdala-prefrontal connectivity during emotion regulation: A meta-analysis of psychophysiological interactions. Neuropsychologia, 153, 107767.
2. Bookheimer, S. Y., et al. (2011). Decoding Continuous Variables from Neuroimaging Data: Basic and Clinical Applications. Frontiers in Neuroscience, 5(Pt 1).
3. Buhle, J. T., et al. (2014). Cognitive reappraisal of emotion: a meta-analysis of human neuroimaging studies. Cerebral Cortex, 24(11), 2981–2990.
4. Full reference list available in the paper.
