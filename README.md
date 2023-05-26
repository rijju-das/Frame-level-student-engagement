# Frame-level-student-engagement
Video based real life student engagement classification using knowledge transfer concept

<h2> Executive summary</h2>
This project focuses on developing a robust student engagement detection system by leveraging facial features and video datasets. The main contributions include the introduction of a novel labeling methodology that captures the temporal dynamics of engagement within video frames, a comparative analysis highlighting the advantages of video datasets over image datasets in capturing engagement variations, and a comprehensive evaluation of all 712 facial features generated by OpenFace. The project aims to advance the field of student engagement detection and support educators in understanding students' levels of attention and interest. The GitHub repository provides the necessary resources for further research and collaboration in this domain.

<h2> Code</h2>
All codes are written in python3 and can be found in ./scripts/.
* DataFormatter.py : DataFormatter class that prepares the input data for a machine learning model. It splits the dataset into training, validation, and test sets, reshapes the input features to include a third dimension, and performs one-hot encoding on the target labels. This ensures that the data is properly formatted and ready for training a model.
* XGB_pred.ipynb : The code performs tasks to train and evaluate an XGBoost classifier for student engagement prediction. 
* Tab_CNN.ipynb : 
This code appears to be a script for training and evaluating a Convolutional Neural Network (CNN) model on two different datasets: "WACV_train_data" and "DAiSEE_TL_data". The code builds a CNN model using the Keras library, trains it on the "WACV_train_data" dataset, evaluates its performance on the "DAiSEE_TL_data" dataset using transfer learning concepts.

<h2> Data</h2>
The datasets used in our case study can be found in the following links:
[https://drive.google.com/file/d/1jE7ytpdF2Hn83ZQzd21MdmS1Oir_y0ty/view?usp=sharing] 
[https://drive.google.com/file/d/11Xcl3xYsaaKcRgxsvyzrPKW9OOaVIyKP/view?usp=sharing]
