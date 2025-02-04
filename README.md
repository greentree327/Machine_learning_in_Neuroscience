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
<img src="https://github.com/user-attachments/assets/d21167e4-0caa-48bd-8342-d21f4903a7c3" width="800" height="300" alt="fNIRS data preprocessing pipeline diagram"/>

### Significant Signal Processing Steps & Results

#### 5. Wavelet-Based Motion Correction
<p align="center">
  <img src="https://github.com/user-attachments/assets/5f9000b7-6862-4da5-bc24-9aa3d8fd7869" width="600" height="300" alt="Wavelet Correction"/>
</p>

**Before vs After:**
- Successfully removed sudden spikes (IQR > 1.5)
- Smoother signal trajectory while preserving underlying neural responses

#### 6. Bandpass Filtering
<p align="center">
  <img src="https://github.com/user-attachments/assets/069dc3c0-ee82-41b0-ba09-65db6c099717" width="600" height="400" alt="Bandpass Filter Effect"/>
</p>

**Filtering Results:**
- High-pass filter (0.01 Hz): Removed slow drifts
- Low-pass filter (0.4 Hz): Eliminated high-frequency noise
- Removed physiological noise:
  - Heart rate (~1-1.2 Hz)
  - Respiration (~0.3-0.6 Hz)
  - Blood pressure/Mayer waves (~0.1 Hz)

#### 8. CBSI Motion Correction
<p align="center">
  <img src="https://github.com/user-attachments/assets/7d803d30-0ad7-47c7-a339-613ff9fe51a7" width="600" height="300" alt="CBSI Correction"/>
</p>

**Improvements:**
- Enhanced signal quality through correlation-based signal improvement
- Stronger mirroring effect between HbO and HbR signals
- More distinct hemodynamic response patterns
- 
### Region of Interest (ROI)
<p align="center">
  <img src="https://github.com/user-attachments/assets/63ad0b0d-9562-44a2-902e-0b58f154f765" width="350" height="150" alt="fNIRS cap configuration"/>
</p>

## Results

### Connectivity Analysis
<p align="center">
  <img src="https://github.com/user-attachments/assets/80c5dad1-41fe-46c5-81f9-26dd58ff79b9" width="600" height="400" alt="Correlation matrices"/>
</p>

- Technique: Pearson correlation matrices between channel pairs
- Finding: Stronger S4/-D2-D4-D6 cluster correlation in neurofeedback group (r > 0.7)

### Time Series Analysis
<p align="center">
  <img src="https://github.com/user-attachments/assets/3121983d-4077-4c54-8b0e-5ae96d968aaa" width="800" height="300" alt="Grand average of oxygenated haemoglobin brain activity"/>
</p>

- Technique: Averaged HbO response across trials and subjects
- Finding: Peak activation difference between groups during 6-12s window (5 x 10⁻⁸ mol/L)

### Machine Learning Classification
<p align="center">
  <img src="https://github.com/user-attachments/assets/73f78d9a-ebb7-43b3-be19-4aaba3e730ab" width="400" height="400" alt="Confusion Matrix"/>
</p>

- Technique: Linear SVC with grid search CV (optimal C = 0.1954)
- Finding: 77.78% accuracy, significantly above chance (χ² = 4.43, p = 0.0353)
- 
### Training Effects
<div align="center">
  <img src="https://github.com/user-attachments/assets/37ec65ab-350c-4d3b-b069-5b99e6fea2fe" width="600" height="400" alt="Neurofeedback group results"/>
  <img src="path/to/figure12b.png" width="600" height="400" alt="Neurofeedback group statistics"/>
  <img src="https://github.com/user-attachments/assets/3f0555a5-b4a2-41d5-a63f-226503a4953f" width="600" height="400" alt="Sham group results"/>
  <img src="path/to/figure13b.png" width="600" height="400" alt="Sham group statistics"/>
</div>

- Technique: Repeated measures ANOVA with post-hoc pairwise t-tests
- Finding: Sessions 2-3 improvement in neurofeedback group (p = 0.013, F = 2.0655)


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
