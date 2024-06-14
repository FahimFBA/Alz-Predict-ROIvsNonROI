# Efficient Prediction for Alzheimer's Disease

## Short Demonstration
This project leverages advanced Convolutional Neural Networks (CNNs) for the automated segmentation and analysis of MRI brain images to detect Alzheimer's Disease. We use 3D ResNet enhanced with Convolutional Block Attention Module (CBAM) to improve the model's performance and interpretability. Our approach includes data preprocessing, MRI registration, and data augmentation techniques. The dataset is sourced from ADNI and OASIS, segmented using FastSurfer, and processed with CLAHE for better contrast. This method aims for accurate and efficient Alzheimer's detection, enhancing early diagnosis and treatment strategies.

## Abstract



## Datasets
In the first phase, we gathered 3D MRI datasets from ADNI and OASIS, renowned initiatives for advancing the understanding of Alzheimer’s disease. We categorized the data into Alzheimer’s Disease (AD), Mild Cognitive Impairment (MCI), and Cognitively Normal (CN) classes. Additionally, we obtained CSV files containing detailed patient information for labeling. Strict privacy rules were followed to ensure the security of sensitive medical data.

## Dataset Organization
For our research, we categorized the dataset into three distinct groups: AD (Alzheimer's Disease), CN (Cognitively Normal), and MCI (Mild Cognitive Impairment).

### ADNI 
We utilized the ADNI Screening 1.5T dataset, which includes subjects who underwent a screening scan. We collected Neuroimaging Informatics Technology Initiative (NIfTI) images from 2294 subjects.

### OASIS
The dataset includes 416 patients aged 18 to 96. Each person undergoes three or four T1-weighted MRI scans in a single session. Among the participants over sixty, 100 have been diagnosed with Alzheimer's disease. Additionally, there is a reliability dataset with 20 nondemented participants.

## Dataset Preprocessing


## Experiments

| Experiment Sl. | Experiment Name | Accuracy | Val. Accuracy | Notebook | Model |
| -------------- | --------------- | -------- | --------------| -------- | ----- |
|       1        | ADNI - AD vs MCI| 88%      | 88%           |          |       |
|       2        | ADNI (ROIs) - AD vs MCI| 92% | 98.33%      |          |       |
|       3        | OASIS - AD vs MCI| 98%  | 98.3%            |          |       |
|       4        | OASIS (ROIs) - AD vs MCI | 98.33% | 97.78% |          |       |
|       6        | ADNI (ROIs) - AD vs CN | 93.33% | 95.63%   |          |       |
|       7        | OASIS - AD vs CN | 100% | 100%             |          |       | 
|       8        | OASIS (ROIs) - AD vs CN | 97.8% | 99.5%    |          |       |
|       9        | ADNI - CN vs MCI | 87.27% | 89.5%          |          |       |
|       10       | ADNI (ROIs) - CN vs MCI | 88.2% | 91.03%   |          |       | 
|       11       | OASIS - CN vs MCI | 98.05% | 98.89%        |          |       |
|       12       | OASIS (ROIs) - CN vs MCI | 98.6% | 99.6%   |          |       |