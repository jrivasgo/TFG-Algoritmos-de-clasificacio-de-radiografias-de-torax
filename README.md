# TFG-Algoritmos-de-clasificacio-de-radiografias-de-torax
Chest X-ray Lesion Classification

This repository contains the code developed for a Final Degree Project focused on the classification of chest X-ray images using machine learning, deep learning and hybrid approaches.

The main objective of the project is to compare different artificial intelligence models applied to radiological image classification, with special attention to chest X-rays related to normal cases, COVID-19, viral pneumonia and bacterial pneumonia.

Important note: this project has an academic and experimental purpose. The models included in this repository are not intended for clinical diagnosis and must not be used as a substitute for professional medical judgement.

Project overview

Chest X-rays are widely used in medical imaging because they are accessible, relatively inexpensive and useful for studying respiratory diseases. However, their interpretation can be complex due to visual similarities between different pathologies, variations between patients, image quality differences and dataset imbalance.

This project explores how different machine learning and deep learning techniques can be used to classify chest X-ray images. Several models were trained, evaluated and compared using objective classification metrics such as accuracy, precision, recall, F1-score and confusion matrices.

The project also includes interpretability techniques, such as Grad-CAM, to help visualize which regions of the image influence the prediction of convolutional models.

Models included

The repository includes different approaches developed and compared during the project:

Random Forest + PCA
Custom Convolutional Neural Network
ResNet50 with Transfer Learning
Autoencoder + Random Forest
CNN feature extractor + Random Forest
CNN trained and evaluated using two datasets
Demonstration application for model prediction and result visualization

Each model was designed to study a different way of extracting and using information from chest X-ray images.

Technologies used

The project was developed mainly in Google Colab using Python and the following libraries:

Python
Google Colab
TensorFlow
Keras
Scikit-learn
NumPy
Pandas
Matplotlib
OpenCV
PIL
Joblib
Repository structure
chest-xray-lesion-classification/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── notebooks/
│   ├── 01_random_forest_pca.ipynb
│   ├── 02_custom_cnn.ipynb
│   ├── 03_resnet50_transfer_learning.ipynb
│   ├── 04_autoencoder_random_forest.ipynb
│   ├── 05_cnn_random_forest_hybrid.ipynb
│   └── 06_cnn_two_datasets.ipynb
│
├── src/
│   ├── preprocessing.py
│   ├── metrics.py
│   ├── gradcam.py
│   └── utils.py
│
├── results/
│   ├── classification_reports/
│   ├── confusion_matrices/
│   └── training_curves/
│
├── models/
│   └── README.md
│
└── app/
    └── demo_app.py

The structure may vary depending on the final organization of the notebooks and scripts, but this layout is recommended to keep the project clear and easy to maintain.

Datasets

This project uses public chest X-ray datasets. The images are not included directly in this repository due to size, organization and data management reasons.

The datasets used in the project include:

COVID-19 chest X-ray images
Normal chest X-ray images
Viral pneumonia chest X-ray images
Bacterial pneumonia chest X-ray images

Before training the models, the images were organized by class, resized, normalized and split into training, validation and test subsets.

Methodology

The general workflow followed in this project is:

Dataset selection and organization.
Image preprocessing.
Train-validation-test split.
Model design and training.
Hyperparameter tuning when applicable.
Evaluation using classification metrics.
Analysis of confusion matrices.
Comparison between models.
Grad-CAM visualization for interpretability.
Demonstration application for testing trained models.
Evaluation metrics

The models were evaluated using several classification metrics:

Accuracy
Precision
Recall
F1-score
Confusion matrix

Special attention was given to false positives and false negatives, since errors in medical image classification can have important implications. However, all results must be interpreted within an academic and experimental context.

Model comparison

The project compares classical machine learning models, convolutional neural networks, pretrained architectures and hybrid approaches.

The comparison focuses not only on global accuracy, but also on the behaviour of each model across different classes. This is especially important when working with medical images, where class imbalance and visual similarity between diseases can affect the reliability of the predictions.

Grad-CAM interpretability

Grad-CAM was used to generate visual activation maps for convolutional models. These maps help identify which regions of the chest X-ray contributed most to the model prediction.

This interpretability step is useful to better understand the behaviour of the model, although it does not replace clinical validation or expert medical interpretation.

Installation

Clone the repository:

git clone https://github.com/your-username/chest-xray-lesion-classification.git
cd chest-xray-lesion-classification

Create a virtual environment:

python -m venv venv

Activate the environment:

# macOS / Linux
source venv/bin/activate
# Windows
venv\Scripts\activate

Install the required dependencies:

pip install -r requirements.txt
Running the notebooks

The notebooks can be executed locally or in Google Colab.

To run them in Google Colab:

Open Google Colab.
Upload the selected notebook.
Mount Google Drive if the datasets are stored there.
Update the dataset paths.
Execute the cells in order.

Example dataset path used in Colab:

from google.colab import drive
drive.mount('/content/drive')
Requirements

A possible requirements.txt file may include:

tensorflow
keras
scikit-learn
numpy
pandas
matplotlib
opencv-python
pillow
joblib

Depending on the final notebooks, additional libraries may be required.

Disclaimer

This repository is part of an academic Final Degree Project.

The models developed here are experimental and were trained using public datasets. They are not clinically validated and must not be used for real medical diagnosis, treatment decisions or patient evaluation.

Any potential clinical use would require external validation, regulatory compliance, expert supervision, privacy guarantees and testing with real-world medical data.

Author

Jorge Rivas Gómez

Final Degree Project
Faculty of Computer Science
Universidad Pontificia de Salamanca




