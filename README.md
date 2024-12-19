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
|       1        | ADNI - AD vs MCI| 88%      | 88%           | [Here](./Notebooks/ADNI/Complete%20Region%20of%20Human%20Brain/Upgraded%20Filter%20AD%20vs%20CN/Upgrade_Filter_allReg_IJK_ADNI_ADvsCN.ipynb) | Resnet18 with CBAM |
|       2        | ADNI (6 ROIs) - AD vs MCI| 92% | 98.33%    | [Here](./Notebooks/ADNI/6%20ROIs/Upgrade%20Filter%206ROI%20AD%20vs%20MCI/Main%20Notebook/Upgrade_Filter_6ROI_ADNI_ADvsMCI.ipynb)  | Resnet18 with CBAM |
|       3        | OASIS - AD vs MCI| 98%  | 98.3%            |  |       |
|       4        | OASIS (6 ROIs) - AD vs MCI | 98.33% | 97.78% | [Here](./Notebooks/OASIS/6%20ROIs/Upgraded%20Filter%20AD%20vs%20CN/) | Resnet18 with CBAM |
|       5        | ADNI - AD vs CN | 88.89% | 97.5%           | [Here](./Notebooks/ADNI/Complete%20Region%20of%20Human%20Brain/Upgraded%20Filter%20AD%20vs%20CN/Upgrade_Filter_allReg_IJK_ADNI_ADvsCN.ipynb) | Resnet18 with CBAM |
|       6        | ADNI (6 ROIs) - AD vs CN | 93.33% | 95.63% | [Here](./Notebooks/ADNI/6%20ROIs/Upgrade%20Filter%206ROI%20AD%20vs%20MCI/Main%20Notebook/Upgrade_Filter_6ROI_ADNI_ADvsMCI.ipynb) | Resnet18 with CBAM |
|       7        | OASIS - AD vs CN | 100% | 100%             |          |       | 
|       8        | OASIS (6 ROIs) - AD vs CN | 97.8% | 99.5%  | [Here](./Notebooks/OASIS/6%20ROIs/Upgraded%20Filter%20AD%20vs%20CN/) | Resnet18 with CBAM |
|       9        | ADNI - CN vs MCI | 87.27% | 89.5%          | [Here](./Notebooks/ADNI/Complete%20Region%20of%20Human%20Brain/Upgraded%20Filter%20AD%20vs%20CN/Upgrade_Filter_allReg_IJK_ADNI_ADvsCN.ipynb) | Resnet18 with CBAM |
|       10       | ADNI (6 ROIs) - CN vs MCI | 88.2% | 91.03% | [Here](./Notebooks/ADNI/6%20ROIs/Upgrade%20Filter%206ROI%20AD%20vs%20MCI/Main%20Notebook/Upgrade_Filter_6ROI_ADNI_ADvsMCI.ipynb) | Resnet18 with CBAM | 
|       11       | OASIS - CN vs MCI | 98.05% | 98.89%        |          |       |
|       12       | OASIS (6 ROIs) - CN vs MCI | 98.6% | 99.6% | [Here](./Notebooks/OASIS/6%20ROIs/Upgraded%20Filter%20AD%20vs%20CN/) | Resnet18 with CBAM |