# Enhancing Frame-Level Student Engagement Classification Through Knowledge Transfer Techniques


**Riju Das, Soumyabrata Dev**  
**“Enhancing frame-level student engagement classification through knowledge transfer techniques”**  
*Applied Intelligence, 2024* — DOI: **10.1007/s10489-023-05256-2**

## Overview

Student engagement varies over time during an online learning session—however, most public engagement datasets (especially video-based ones) provide only **video-level labels**, which can hide important engagement fluctuations across frames.

This repository provides code and extracted facial-feature datasets for **frame-level engagement classification** using **knowledge transfer**:

- A deep model is **pretrained** on a labeled *image-based* engagement dataset (**WACV**)
- The learned knowledge is then **transferred / adapted** to a *video-based* dataset (**DAiSEE**) to enable **frame-level engagement estimation**
- We also include baseline experiments using classical ML (e.g., **XGBoost**) on extracted facial features

The main focus of this project is **fine-grained (frame-level) engagement prediction** from facial behavior features.

## Method Summary (High-Level)

1. **Feature extraction** (OpenFace)
   - Extract per-frame facial behavior features (Action Units, gaze, head pose, etc.)
2. **Source-domain learning**
   - Train model on the labeled **WACV image-based dataset**
3. **Knowledge transfer**
   - Transfer learned representations to the target dataset (**DAiSEE videos**)  
4. **Frame-level prediction**
   - Generate engagement predictions at the frame level for DAiSEE videos

## Repository Structure
All codes are written in python3 and can be found in ./Scripts.
```bash
Frame-level-student-engagement/
├── Scripts/
│   ├── DataFormatter.py        # Dataset formatting 
│   ├── XGB_pred.ipynb          # XGBoost baseline training/evaluation
│   └── Tab_CNN.ipynb           # transfer learning
├── README.md
```

* DataFormatter.py : DataFormatter class that prepares the input data for a machine learning model. It splits the dataset into training, validation, and test sets, reshapes the input features to include a third dimension, and performs one-hot encoding on the target labels. This ensures that the data is properly formatted and ready for training a model.
* XGB_pred.ipynb : The code performs tasks to train and evaluate an XGBoost classifier for student engagement prediction. 
* Tab_CNN.ipynb : 
This code appears to be a script for training and evaluating a Convolutional Neural Network (CNN) model on two different datasets: "WACV_train_data" and "DAiSEE_TL_data". The code builds a CNN model using the Keras library, trains it on the "WACV_train_data" dataset, evaluates its performance on the "DAiSEE_TL_data" dataset using transfer learning concepts.

## Data
The datasets used in our case study can be found in the following links:

* [DAiSEE: Extracted facial features dataset](https://drive.google.com/file/d/1jE7ytpdF2Hn83ZQzd21MdmS1Oir_y0ty/view?usp=sharing)
* [WACV: Extracted facial features dataset](https://drive.google.com/file/d/11Xcl3xYsaaKcRgxsvyzrPKW9OOaVIyKP/view?usp=sharing)

## Citation
If you use this repository, please cite the paper:
```bibtex
@article{das2024enhancing,
  title   = {Enhancing frame-level student engagement classification through knowledge transfer techniques},
  author  = {Das, Riju and Dev, Soumyabrata},
  journal = {Applied Intelligence},
  volume  = {54},
  pages   = {2261--2276},
  year    = {2024},
  doi     = {10.1007/s10489-023-05256-2},
  publisher = {Springer}
}
```
## 👤 Contact

Riju Das ([riju.das@ucd.ie](mailto:riju.das@ucd.ie))
Ph.D. Scholar – University College Dublin

