# Machine_learning_in_Neuroscience
EDA &amp; SVM in functional near-infrared spectroscopy data (fNIRS) in neuroscience

Medium link: https://medium.com/@jackson3b04/using-machine-learning-to-decode-fnirs-data-f5cb3aab1291

Using Machine Learning to Decode fNIRS Data
Overview
This research investigates cognitive reappraisal through neurofeedback-based training using functional near-infrared spectroscopy (fNIRS). The study employs various analytical approaches including correlation matrices, repeated-measures ANOVA, and machine learning methods like Support Vector Machines (SVM).

Key Hypotheses
Brain activity in the lateral prefrontal cortex (lPFC) will increase across training runs during reappraisal trials
Cognitive reappraisal enhances connectivity in the lPFC ROI more strongly for the experimental neurofeedback group
SVM classifier can distinguish between regulation and view conditions
SVM classifier accuracy significantly differs from random guessing
Methods
fNIRS Data Preprocessing Pipeline
[Insert Figure 1 here - fNIRS data preprocessing pipeline diagram]

Signal Processing Steps
Raw intensity data collection
Bad data filtering & channel selection
Optical density conversion
Scalp coupling index (SCI) calculation
Motion correction using wavelet-based method
Bandpass filtering
Conversion to haemoglobin concentration
Motion correction using CBSI
Region of Interest (ROI)
[Insert Figure 6 here - fNIRS cap configuration with lateral PFC ROI]

Results
Connectivity Analysis
[Insert Figure 8 here - Correlation matrices]

Time Series Analysis
[Insert Figure 9 here - Grand average of oxygenated haemoglobin brain activity]

Training Effects
[Insert Figures 12a and 12b here - Neurofeedback group results]
[Insert Figures 13a and 13b here - Sham group results]

Machine Learning Classification
[Insert Figure 15 here - Confusion Matrix]

Key Findings
Significant increase in brain activity between neurofeedback training sessions 2 and 3
Enhanced functional connectivity during reappraisal tasks in the neurofeedback group
SVM classifier achieved 77.78% accuracy in distinguishing between conditions
Statistical significance confirmed through chi-square test (χ² = 4.43, p = 0.0353)
Code Notebooks
Time Series Analysis: Colab Notebook
Training Effect Analysis: Colab Notebook
SVM Classification: Colab Notebook
Future Directions
Investigation of additional statistical predictors
Development of more sophisticated temporal feature analysis
Enhancement of signal-to-noise ratio in machine learning models
References
[References section from the original document]

Would you like me to explain or break down any part of this README?
