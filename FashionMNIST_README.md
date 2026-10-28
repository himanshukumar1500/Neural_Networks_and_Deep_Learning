# FashionMNIST Classification Using PyTorch

## 📌 Overview

In this practical, I implemented a deep learning model using PyTorch to classify clothing images from the FashionMNIST dataset. I trained a neural network, calculated the model size, experimented with different hyperparameters to improve accuracy, and implemented the One-vs-All classification method.

This project helped me understand neural network training, model evaluation, hyperparameter tuning, and multiclass image classification.

## 🎯 Objectives

1. Implement a neural network using PyTorch.
2. Calculate the total trainable parameters and final model size.
3. Improve classification accuracy using hyperparameter tuning.
4. Implement One-vs-All (One-vs-Rest) classification.
5. Compare multiclass and One-vs-All classification performance.

## 📊 Dataset: FashionMNIST

FashionMNIST is a dataset of grayscale clothing images divided into 10 categories.

| Property | Description |
|---|---|
| Training images | 60,000 |
| Testing images | 10,000 |
| Image dimensions | 28 × 28 pixels |
| Number of classes | 10 |
| Image type | Grayscale |

### Classes

- T-shirt/top
- Trouser
- Pullover
- Dress
- Coat
- Sandal
- Shirt
- Sneaker
- Bag
- Ankle boot

The dataset is downloaded automatically using Torchvision.

## 🛠️ Technologies Used

- Python
- PyTorch
- Torchvision
- NumPy
- Pandas
- Matplotlib
- Google Colab

## 🧠 Model Architecture

The baseline model is a fully connected neural network (Multilayer Perceptron).

| Layer | Configuration |
|---|---|
| Input layer | 784 features |
| Hidden layer 1 | 256 neurons, ReLU |
| Dropout | 0.2 |
| Hidden layer 2 | 128 neurons, ReLU |
| Dropout | 0.2 |
| Output layer | 10 neurons |

**Loss function:** Cross-Entropy Loss

**Optimizer:** Adam

**Learning rate:** 0.001

**Batch size:** 128

**Training epochs:** 5 for the baseline model

## 🔬 Experiments Performed

### 1. Model Size Calculation

I calculated the total number of trainable parameters and estimated the memory required to store the model parameters. I also saved the trained model and checked the checkpoint file size.

- **Trainable parameters:** 235,146
- **Estimated parameter memory:** Approximately 0.94 MB using 32-bit floating-point values.

The saved checkpoint file size is measured separately during execution.

### 2. Hyperparameter Tuning

I experimented with different hyperparameters to study their effect on model performance.

- Learning rate
- Batch size
- Hidden-layer size
- Dropout rate
- Optimizer (Adam and SGD)

I compared the resulting test accuracies to identify the best-performing configuration.

### 3. One-vs-All Classification

I implemented One-vs-All classification using 10 separate binary classifiers.

Each classifier learns to distinguish one clothing category from all the remaining categories. During prediction, the class with the highest classifier score is selected.

### 4. Performance Comparison

I compared the baseline multiclass model with the One-vs-All approach using test accuracy and a comparison graph.

## 🚀 How to Run the Project

### Using Google Colab

1. Download the notebook from this repository.
2. Open [Google Colab](https://colab.research.google.com/).
3. Select **File → Upload notebook**.
4. Upload `FashionMNIST_PyTorch_Practical.ipynb`.
5. Select a GPU runtime if available.
6. Run all cells from top to bottom.
7. Review the model size, hyperparameter tuning results, and classification accuracy.

### Run Locally

Install the required libraries:

```bash
pip install torch torchvision numpy matplotlib pandas
```

Open the notebook in Jupyter Notebook or JupyterLab and execute the cells in order.

The FashionMNIST dataset will be downloaded automatically.

## 📈 Results

Record the actual results after running the notebook.

| Metric | Result |
|---|---|
| Dataset | FashionMNIST |
| Trainable parameters | 235,146 |
| Parameter memory | Approximately 0.94 MB |
| Saved model size | Measure during execution |
| Best hyperparameter configuration | From tuning results |
| Multiclass test accuracy | From program output |
| One-vs-All test accuracy | From program output |

*Note: Accuracy values depend on the training process, hyperparameters, and random initialization. Update the results with the actual values obtained from your Colab run.*

## 📁 Project Structure

```text
Neural_Networks_and_Deep_Learning/
│
├── Five_Layer_NN.ipynb
├── Five_Layer_NN_README.md
├── mnist_classification.ipynb
├── MNIST_README.md
├── FashionMNIST_PyTorch_Practical.ipynb
├── FashionMNIST_README.md
├── README.md
├── .gitignore
└── LICENSE
```

The model checkpoint files are generated when the corresponding save commands are executed.

## 💡 Learning Outcomes

Through this practical, I learned:

- How to load and visualize image datasets using Torchvision.
- How to build and train neural networks using PyTorch.
- How to calculate trainable parameters and model size.
- How to tune hyperparameters to improve model performance.
- How One-vs-All classification works.
- How to compare different classification methods using accuracy.

## 🏁 Conclusion

In this practical, I implemented a PyTorch neural network for FashionMNIST image classification. I calculated the model size, experimented with different hyperparameters, and implemented One-vs-All classification using separate binary classifiers. Finally, I compared the performance of multiclass and One-vs-All classification to understand their differences.

## 👨‍💻 Author

**Himanshu Kumar**

- **Course:** B.E. in Computer Science and Engineering (CSE)
- **College:** UIET
- **GitHub:** [@himanshukumar1500](https://github.com/himanshukumar1500)

## 📚 References

- [FashionMNIST Dataset](https://github.com/zalandoresearch/fashion-mnist)
- [PyTorch Documentation](https://pytorch.org/docs/stable/index.html)
- [Torchvision Documentation](https://pytorch.org/vision/stable/index.html)
- [Google Colab](https://colab.research.google.com/)
