# Hyperspectral Land Cover Classifier

A machine learning project for classifying land cover types using hyperspectral imaging data from the Indian Pines dataset. The project implements multiple classification approaches including SVM, Random Forest, and 3D-CNN.

## Dataset

The project uses the Indian Pines dataset which consists of:
- Hyperspectral image data (145x145x200 dimensions)
- Ground truth labels (145x145 dimensions)

Files required:
- `Dataset/Indian_pines_corrected.mat` - Hyperspectral image data
- `Dataset/Indian_pines_gt.mat` - Ground truth labels
- `Dataset/Ground_truth_data.npy` - Processed ground truth data
- `Dataset/Hyperspectral_data.npy` - Processed hyperspectral data

## Implementation Approaches

### 1. Support Vector Machine (SVM)
- Implemented in `HSI-SVM.ipynb`
- Features:
  - Data preprocessing and scaling
  - SVM classifier implementation
  - Random Forest classifier comparison
  - Achieves 92.74% classification accuracy with SVM
  - Achieves 97.45% classification accuracy with Random Forest

### 2. 3D Convolutional Neural Network (3D-CNN)
- Implemented in `HSI-3DCNN.ipynb`
- Features:
  - Principal Component Analysis (PCA) for dimensionality reduction
  - 3D patch extraction (25x25x50 patches)
  - Deep learning based classification
  - Data split: 30% training, 70% testing

## Results

The models achieve high classification accuracy on the Indian Pines dataset:
- SVM: 92.74%
- Random Forest: 97.45%
- 3D-CNN: Results vary based on training

The classification results are visualized using confusion matrices and comparison plots with ground truth data.

## Requirements

- Python libraries:
  - scipy
  - numpy
  - scikit-learn
  - matplotlib
  - tensorflow/keras (for 3D-CNN)
  - xgboost

## Usage

1. Place the dataset files in the `Dataset` directory
2. Run the Jupyter notebooks:
   - `HSI-SVM.ipynb` for SVM and Random Forest implementation
   - `HSI-3DCNN.ipynb` for 3D-CNN implementation
3. View the results and visualizations within the notebooks