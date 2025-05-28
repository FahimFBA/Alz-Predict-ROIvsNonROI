# Efficient Prediction for Alzheimer's Disease

## 📄 Paper

This repository is based on the following peer-reviewed publication:

**Paper Title**: [Enhanced ROI guided deep learning model for Alzheimer’s detection using 3D MRI images](https://doi.org/10.1016/j.imu.2025.101650)

**Journal**: *Informatics in Medicine Unlocked*, Volume 56, 2025, Page 101650

**DOI**: [https://doi.org/10.1016/j.imu.2025.101650](https://doi.org/10.1016/j.imu.2025.101650)

**Read on**:

* [ScienceDirect](https://www.sciencedirect.com/science/article/pii/S2352914825000383)
* [ResearchGate](https://www.researchgate.net/publication/392007551_Enhanced_ROI_guided_deep_learning_model_for_Alzheimer's_detection_using_3D_MRI_images)

### 📚 Citation

```
@article{KHAN2025101650,
title = {Enhanced ROI guided deep learning model for Alzheimer’s detection using 3D MRI images},
journal = {Informatics in Medicine Unlocked},
volume = {56},
pages = {101650},
year = {2025},
issn = {2352-9148},
doi = {https://doi.org/10.1016/j.imu.2025.101650},
url = {https://www.sciencedirect.com/science/article/pii/S2352914825000383},
author = {Israt Jahan Khan and Md. Fahim Bin Amin and Md. Delwar Shahadat Deepu and Hazera Khatun Hira and Asif Mahmud and Anas Mashad Chowdhury and Salekul Islam and Md. Saddam Hossain Mukta and Swakkhar Shatabda},
keywords = {Alzheimer’s disease, Regions of Interest (ROIs), 3D MRI, Transfer learning, ResNet 3D, Efficient computation},
abstract = {Alzheimer’s disease is an incurable condition that predominantly affects the human brain, leading to the shrinkage of various brain regions and the disruption of neuronal connections. Current state-of-the-art methods for detecting Alzheimer’s disease using 3D MRI images are resource-intensive and time-consuming. In this paper, we propose a Regions of Interest (ROI)-guided detection paradigm to address these challenges. We employ a 3D ResNet integrated with a Convolutional Block Attention Module (CBAM), demonstrating that emphasising ROIs in brain imaging can substantially reduce both computational expenditure and training time. Our model exhibits robust performance in discriminating Alzheimer’s disease from mild cognitive impairment, achieving an accuracy of 88% across the entire brain and 92% within targeted ROIs on the ADNI dataset. The accuracy on the OASIS dataset is even higher, reaching 98% for all regions and 98.33% for the ROIs. When distinguishing Alzheimer’s disease from cognitively normal individuals, the accuracy improves further, achieving 93.33% for the ROIs on the ADNI dataset and 97.8% on the OASIS dataset. In differentiating cognitively normal individuals from those with mild cognitive impairment, the model attains an accuracy of 88.2% for the ROIs on the ADNI dataset and 98.6% on the OASIS dataset. These findings highlight a notable enhancement in detection accuracy through the utilisation of fewer, yet more salient brain regions, underscoring the efficacy of our ROI-guided approach.}
}
```

## 🔍 Short Demonstration

This project leverages advanced Convolutional Neural Networks (CNNs) for automated segmentation and analysis of 3D MRI brain images to detect Alzheimer's Disease. The core model architecture is a **3D ResNet enhanced with a Convolutional Block Attention Module (CBAM)**, significantly improving both model accuracy and interpretability.

Our workflow includes:

* Preprocessing (bias correction, skull stripping, CLAHE)
* Image registration and standardization
* FastSurfer-based segmentation
* ROI extraction
* Extensive data augmentation

Datasets were obtained from **ADNI** and **OASIS**, and experiments focused on classifying subjects into:

* Alzheimer’s Disease (AD)
* Mild Cognitive Impairment (MCI)
* Cognitively Normal (CN)

This method is particularly effective for early-stage detection, guiding clinical decision-making through high-accuracy, ROI-focused models.



## Abstract

Alzheimer’s disease is an incurable condition that predominantly affects the human brain, leading to the shrinkage of various brain regions and the disruption of neuronal connections. Current state-of-the-art methods for detecting Alzheimer’s disease using 3D MRI images are resource-intensive and time-consuming. In this paper, we propose a Regions of Interest (ROI)-guided detection paradigm to address these challenges. We employ a 3D ResNet integrated with a Convolutional Block Attention Module (CBAM), demonstrating that emphasising ROIs in brain imaging can substantially reduce both computational expenditure and training time. Our model exhibits robust performance in discriminating Alzheimer’s disease from mild cognitive impairment, achieving an accuracy of 88% across the entire brain and 92% within targeted ROIs on the ADNI dataset. The accuracy on the OASIS dataset is even higher, reaching 98% for all regions and 98.33% for the ROIs. When distinguishing Alzheimer’s disease from cognitively normal individuals, the accuracy improves further, achieving 93.33% for the ROIs on the ADNI dataset and 97.8% on the OASIS dataset. In differentiating cognitively normal individuals from those with mild cognitive impairment, the model attains an accuracy of 88.2% for the ROIs on the ADNI dataset and 98.6% on the OASIS dataset. These findings highlight a notable enhancement in detection accuracy through the utilisation of fewer, yet more salient brain regions, underscoring the efficacy of our ROI-guided approach.


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
|       1        | ADNI - AD vs MCI| 88%      | 88%           | [View](https://nbviewer.org/github/FahimFBA/Alz-Predict-ROIvsNonROI/blob/main/Notebooks/ADNI/Complete%20Region%20of%20Human%20Brain/Upgraded%20Filter%20AD%20vs%20MCI/Upgrade_Filter_allReg_ADNI_ADvsMCI.ipynb) -- [Notebook](Notebooks/ADNI/Complete%20Region%20of%20Human%20Brain/Upgraded%20Filter%20AD%20vs%20MCI/Upgrade_Filter_allReg_ADNI_ADvsMCI.ipynb) | Resnet18 with CBAM |
|       2        | ADNI (6 ROIs) - AD vs MCI| 92% | 98.33%    | [View](https://nbviewer.org/github/FahimFBA/Alz-Predict-ROIvsNonROI/blob/main/Notebooks/ADNI/6%20ROIs/Upgrade%20Filter%206ROI%20AD%20vs%20MCI/Main%20Notebook/Upgrade_Filter_6ROI_ADNI_ADvsMCI.ipynb) -- [Notebook](./Notebooks/ADNI/6%20ROIs/Upgrade%20Filter%206ROI%20AD%20vs%20MCI/Main%20Notebook/Upgrade_Filter_6ROI_ADNI_ADvsMCI.ipynb)  | Resnet18 with CBAM |
|       3        | OASIS - AD vs MCI| 98%  | 98.3%            |  |  |
|       4        | OASIS (6 ROIs) - AD vs MCI | 98.33% | 97.78% |  |  |
|       5        | ADNI - AD vs CN | 88.89% | 97.5% | [View](https://nbviewer.org/github/FahimFBA/Alz-Predict-ROIvsNonROI/blob/main/Notebooks/ADNI/Complete%20Region%20of%20Human%20Brain/Upgraded%20Filter%20AD%20vs%20CN/Upgrade_Filter_allReg_IJK_ADNI_ADvsCN.ipynb) -- [Notebook](Notebooks/ADNI/Complete%20Region%20of%20Human%20Brain/Upgraded%20Filter%20AD%20vs%20CN/Upgrade_Filter_allReg_IJK_ADNI_ADvsCN.ipynb) | Resnet18 with CBAM |
|       6        | ADNI (6 ROIs) - AD vs CN | 93.33% | 95.63% | [View](https://nbviewer.org/github/FahimFBA/Alz-Predict-ROIvsNonROI/blob/main/Notebooks/ADNI/6%20ROIs/Upgrade%20Filter%206ROI%20AD%20vs%20CN/Upgrade_Filter_6ROI_ADNI_ADvsCN.ipynb) -- [Notebook](Notebooks/ADNI/6%20ROIs/Upgrade%20Filter%206ROI%20AD%20vs%20CN/Upgrade_Filter_6ROI_ADNI_ADvsCN.ipynb) | Resnet18 with CBAM |
|       7        | OASIS - AD vs CN | 100% | 100% | [View](https://nbviewer.org/github/FahimFBA/Alz-Predict-ROIvsNonROI/blob/main/Notebooks/OASIS/Complete%20Region%20of%20Human%20Brain/Upgrade%20Filter%20allreg%20OASIS%20AD%20vs%20CN/Upgraded_ADvsCN_Filter_allreg_oasis.ipynb) -- [Notebook](Notebooks/OASIS/Complete%20Region%20of%20Human%20Brain/Upgrade%20Filter%20allreg%20OASIS%20AD%20vs%20CN/Upgraded_ADvsCN_Filter_allreg_oasis.ipynb) |  | 
|       8        | OASIS (6 ROIs) - AD vs CN | 97.8% | 99.5%  | [View](https://nbviewer.org/github/FahimFBA/Alz-Predict-ROIvsNonROI/blob/main/Notebooks/OASIS/6%20ROIs/Upgraded%20Filter%20AD%20vs%20CN/Upgrade_Filter_6ROI_OASIS_ADvsCN.ipynb) -- [Notebook](./Notebooks/OASIS/6%20ROIs/Upgraded%20Filter%20AD%20vs%20CN/) | Resnet18 with CBAM |
|       9        | ADNI - CN vs MCI | 87.27% | 89.5%          |  |  |
|       10       | ADNI (6 ROIs) - CN vs MCI | 88.2% | 91.03% |  |  |
|       11       | OASIS - CN vs MCI | 98.05% | 98.89%        | [View](https://nbviewer.org/github/FahimFBA/Alz-Predict-ROIvsNonROI/blob/main/Notebooks/OASIS/Complete%20Region%20of%20Human%20Brain/Upgrade%20Filter%20allreg%20OASIS%20MCI%20vs%20CN/Upgraded_MCIvsCN_Filter_allreg_oasis.ipynb) -- [Notebook](Notebooks/OASIS/Complete%20Region%20of%20Human%20Brain/Upgrade%20Filter%20allreg%20OASIS%20MCI%20vs%20CN/Upgraded_MCIvsCN_Filter_allreg_oasis.ipynb) |  |
|       12       | OASIS (6 ROIs) - CN vs MCI | 98.6% | 99.6% | [View](https://nbviewer.org/github/FahimFBA/Alz-Predict-ROIvsNonROI/blob/main/Notebooks/OASIS/6%20ROIs/Upgraded%20Filter%20MCI%20vs%20CN/Upgrade_Filter_6ROI_OASIS_MCIvsCN.ipynb) -- [Notebook](./Notebooks/OASIS/6%20ROIs/Upgraded%20Filter%20MCI%20vs%20CN/Upgrade_Filter_6ROI_OASIS_MCIvsCN.ipynb) | Resnet18 with CBAM |



## Recreating the Conda Environment for this Project

This repository includes files to help you recreate the development environment used in this project. Follow the instructions below to set up the environment on your local machine.

### Files Included
- **`environment.yml`**: Captures the full Conda environment, including both Conda and pip-installed packages.
- **`requirements.txt`**: Lists only pip-installed packages, useful for users who prefer pip-based installations.

---

### 1. Recreate the Conda Environment

#### Prerequisites
- Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/distribution).

#### Steps
1. Open a terminal and navigate to the project directory.
2. Run the following command to create the environment:
   ```bash
   conda env create -f environment.yml
   ```
3. Activate the newly created environment:
   ```bash
   conda activate fydp-old
   ```
4. Verify the environment:
   ```bash
   conda list
   ```

---

### 2. Using the `requirements.txt` File (Pip-Only Option)

#### Prerequisites
- Ensure Python and `pip` are installed on your system.

#### Steps
1. Create a virtual environment:
   ```bash
   python -m venv venv
   ```
2. Activate the virtual environment:
   - On Linux/macOS:
     ```bash
     source venv/bin/activate
     ```
   - On Windows:
     ```bash
     venv\Scripts\activate
     ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Verify the installation:
   ```bash
   pip list
   ```

---

### Notes
- **Preferred Method**: The `environment.yml` file is recommended as it fully captures both Conda and pip-installed packages, ensuring 100% reproducibility.
- **Pip Limitation**: The `requirements.txt` file only includes pip-installed packages and may not recreate Conda-specific dependencies or system-level requirements.

---

Feel free to reach out via [GitHub issues](https://github.com/FahimFBA/Alz-Predict-ROIvsNonROI/issues) if you encounter any problems during the setup. Happy coding! 🎉

