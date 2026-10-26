# Five-Layer Neural Network Classifier on Cat vs Non-Cat Dataset

## 📌 Overview

This project implements a **Five-Layer Neural Network** to classify images into two categories: **Cat** and **Non-Cat**.

The project uses deep learning techniques to train a neural network on image data and evaluates the effect of different regularization methods on training accuracy, test accuracy, loss, and model variance.

The implementation is provided in a Jupyter Notebook using Python, NumPy, TensorFlow/Keras, and other machine learning libraries.

## 🎯 Objectives

- Build a five-layer neural network for binary image classification.
- Classify images as Cat or Non-Cat.
- Implement five-fold cross-validation.
- Compare training and test accuracy across different models.
- Study the effects of regularization techniques.
- Visualize loss curves and compare model variance.

## 🧠 Model Architecture

The neural network contains five trainable layers:

| Layer | Number of Neurons | Activation Function |
|---|---:|---|
| Input | 12,288 features | — |
| Hidden Layer 1 | 128 | ReLU |
| Hidden Layer 2 | 64 | ReLU |
| Hidden Layer 3 | 32 | ReLU |
| Hidden Layer 4 | 16 | ReLU |
| Output Layer | 1 | Sigmoid |

**Architecture:** `12288 → 128 → 64 → 32 → 16 → 1`

Each image has dimensions of 64 × 64 × 3. The image pixels are flattened into a vector of 12,288 features and normalized to values between 0 and 1.

## 🛠️ Technologies Used

- **Python** — Programming language
- **NumPy** — Numerical computations
- **Pandas** — Results tables and data handling
- **Matplotlib** — Data visualization and loss curves
- **TensorFlow/Keras** — Neural network implementation
- **Scikit-learn** — Stratified five-fold cross-validation
- **h5py** — Loading HDF5 datasets
- **Jupyter Notebook** — Interactive development and experimentation

## 📂 Project Structure

```text
Five-Layer-Neural-Network/
│
├── Copy of Five_Layer_NN.ipynb
├── train_catvnoncat.h5
├── test_catvnoncat.h5
└── README.md
```

*Note: The HDF5 dataset files must be available locally to run the notebook. The filenames shown above are the ones referenced by the code.*

## 📊 Dataset

The project uses a Cat vs Non-Cat image dataset containing two classes:

- Cat
- Non-Cat

**Image details:**
- Image size: 64 × 64 pixels
- Color channels: 3 (RGB)
- Input features per image: 12,288
- Preprocessing: Flattening and pixel normalization

The notebook loads the training and test images and their labels from HDF5 files.

## ⚙️ Regularization Techniques

The project compares a baseline model with the following methods:

### 1. Baseline Model
A neural network trained without additional regularization, used as the reference for comparison.

### 2. LASSO Regularization
Uses L1 regularization to penalize the absolute values of model weights.

### 3. RIDGE Regularization
Uses L2 regularization to penalize squared model weights.

### 4. Elastic Net
Combines L1 and L2 regularization.

### 5. Dropout
Randomly deactivates neurons during training to help reduce overfitting.

Tested dropout rates: `0.1, 0.2, 0.3, 0.4, 0.5`.

### 6. DropConnect
Randomly removes connections between neurons during training.

Tested DropConnect rates: `0.2, 0.4, 0.5`.

### 7. Batch Normalization
Normalizes layer activations to help stabilize neural network training.

## 🔄 Five-Fold Cross-Validation

The notebook uses five-fold cross-validation to evaluate model performance.

1. Divide the dataset into five folds.
2. Train using four folds.
3. Evaluate using the remaining fold.
4. Repeat the process five times.
5. Calculate average training accuracy, average test accuracy, and test-accuracy variance.

This approach helps assess model performance across different data splits.

## 📈 Evaluation and Results

The notebook compares the baseline and regularized models using:

- Average training accuracy
- Average test accuracy
- Test-accuracy variance
- Loss curves across training epochs
- Accuracy comparison plots
- Variance comparison plots

The final results table is generated within the notebook.

*Actual accuracy values are not included here because they should be taken from the executed notebook results rather than assumed.*

## 🚀 Installation and Setup

### Prerequisites

Install Python and Jupyter Notebook, then install the required libraries.

```bash
pip install numpy pandas matplotlib h5py tensorflow scikit-learn jupyter
```

### Steps to Run

**1. Clone the repository**

```bash
git clone <your-repository-url>
cd Five-Layer-Neural-Network
```

Replace `<your-repository-url>` with your actual GitHub repository URL.

**2. Add the dataset files**

Place `train_catvnoncat.h5` and `test_catvnoncat.h5` in the directory expected by the notebook.

**3. Launch Jupyter Notebook**

```bash
jupyter notebook
```

**4. Open the notebook**

Open `Copy of Five_Layer_NN.ipynb`.

**5. Execute the cells**

Run the notebook from top to bottom to load the data, train the models, perform cross-validation, and generate evaluation plots.

## 💡 Key Learnings

- Understanding deep neural network architecture
- Implementing forward and backward propagation
- Working with image data and feature normalization
- Applying binary classification using sigmoid activation
- Evaluating models using cross-validation
- Comparing L1, L2, Elastic Net, Dropout, and DropConnect regularization
- Analyzing model accuracy, loss, and variance

## 🔮 Future Improvements

- Add precision, recall, F1-score, and a confusion matrix.
- Experiment with different network architectures and hyperparameters.
- Compare the fully connected network with a Convolutional Neural Network (CNN).
- Add prediction functionality for new images.
- Save the trained model for reuse.

## 🏁 Conclusion

This project demonstrates the implementation of a five-layer neural network for Cat vs Non-Cat image classification. It explores five-fold cross-validation and several regularization techniques to understand their effects on accuracy, loss, and variance.

The project provides practical experience with deep learning, binary image classification, model evaluation, and overfitting control.

## 👨‍💻 Author

**Himanshu Kumar**

GitHub: (https://github.com/himanshukumar1500)
---

⭐ If you find this project useful, consider giving the repository a star.
