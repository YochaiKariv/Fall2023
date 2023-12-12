{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": [],
      "authorship_tag": "ABX9TyOuKLHbKHPW98ed1Kn0LigD",
      "include_colab_link": true
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "cells": [
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "view-in-github",
        "colab_type": "text"
      },
      "source": [
        "<a href=\"https://colab.research.google.com/github/YochaiKariv/Fall2023/blob/main/Problem_set_1_MD.ipynb.md\" target=\"_parent\"><img src=\"https://colab.research.google.com/assets/colab-badge.svg\" alt=\"Open In Colab\"/></a>"
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "# Detailed Report on MNIST Loading, Visualization, and Random Model Implementation\n",
        "\n",
        "## Introduction\n",
        "\n",
        "This report details the code for loading, visualizing, and implementing a random model on the MNIST dataset using Python libraries such as TensorFlow and NumPy. The MNIST dataset is a collection of handwritten digits commonly used in machine learning and computer vision.\n",
        "\n",
        "## MNIST Loading and Visualization\n",
        "\n",
        "### Code Overview\n",
        "- The MNIST dataset is loaded using TensorFlow's Keras API.\n",
        "- The dataset is split into training (`X_train`, `y_train`) and testing (`X_test`, `y_test`) sets.\n",
        "- Matplotlib is used for visualization.\n",
        "\n",
        "### Process\n",
        "1. **Dataset Loading**: `mnist.load_data()` function retrieves the MNIST dataset, returning two tuples containing training and test datasets.\n",
        "2. **Visualization**:\n",
        "   - A 4x4 grid is created using `plt.figure()`.\n",
        "   - The first 16 images of `X_train` are displayed in this grid.\n",
        "   - Each image is displayed in grayscale using `cmap='gray'`.\n",
        "\n",
        "## Random Model Implementation\n",
        "\n",
        "### Process\n",
        "1. **Data Preparation**:\n",
        "   - Training and test images are flattened into 1D arrays, transforming the 28x28 images into 784-element vectors.\n",
        "2. **Model Creation**:\n",
        "   - A matrix of random values (`random_matrix`) is initialized. This serves as the weights for a linear model.\n",
        "   - This matrix has dimensions 10x784, corresponding to 10 classes (digits 0-9) and 784 features (pixels).\n",
        "\n",
        "### Predictions and Accuracy\n",
        "- **Prediction**: For each test image, the dot product is computed between `X_test_flat` and the transpose of `random_matrix`. The index of the maximum value in the resulting vector is the predicted class.\n",
        "- **Accuracy Calculation**: Accuracy is calculated by comparing the predicted labels (`y_pred`) with actual labels (`y_test`).\n",
        "\n",
        "### Output\n",
        "- The accuracy of this randomly initialized model is printed.\n",
        "\n",
        "## Random Walk Model Training\n",
        "\n",
        "### Process\n",
        "1. **Initial Setup**:\n",
        "   - The best accuracy (`best_acc`) is initialized to 0.0.\n",
        "2. **Training Loop**:\n",
        "   - For 50 epochs, a random step is added to `random_matrix`.\n",
        "   - This step is a small random adjustment to the weights, simulating a \"random walk\".\n",
        "   - Predictions are made on the training set, and accuracy is calculated.\n",
        "   - If the current accuracy exceeds the best accuracy, it updates `best_acc`.\n",
        "   - The loop breaks if `best_acc` exceeds 75%.\n",
        "\n",
        "### Output\n",
        "- The best accuracy achieved by the random walk model is printed.\n",
        "\n",
        "## Conclusion\n",
        "\n",
        "This code demonstrates basic operations on the MNIST dataset, including loading, visualization, and implementation of a random model. The random model and the random walk model provide a simplistic approach to understanding machine learning concepts, particularly in the context of image classification. The purpose of these models is primarily educational, illustrating how random chance can influence model predictions and the concept of improving a model iteratively."
      ],
      "metadata": {
        "id": "ewuhTLU214TP"
      }
    },
    {
      "cell_type": "code",
      "source": [],
      "metadata": {
        "id": "fyaQ8Okt15Lk"
      },
      "execution_count": null,
      "outputs": []
    }
  ]
}