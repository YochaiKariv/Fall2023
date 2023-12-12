{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": [],
      "authorship_tag": "ABX9TyPhiotSAfSYe5fgC29xv3kK",
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
        "<a href=\"https://colab.research.google.com/github/YochaiKariv/Fall2023/blob/main/problem%20set%202%20md.ipynb.md\" target=\"_parent\"><img src=\"https://colab.research.google.com/assets/colab-badge.svg\" alt=\"Open In Colab\"/></a>"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "aToPUuFw4aYl"
      },
      "outputs": [],
      "source": [
        "# Detailed Report on Image Processing and Convolution Operation\n",
        "\n",
        "## Introduction\n",
        "\n",
        "The provided code demonstrates several key operations in image processing using Python, including image loading from a URL, resizing, converting to grayscale, and applying convolution with random filters. These operations are fundamental in computer vision and image analysis.\n",
        "\n",
        "## Image Loading and Display\n",
        "\n",
        "### Code Overview\n",
        "- The Python Imaging Library (PIL) and requests library are used.\n",
        "- An image is fetched from a specified URL and displayed.\n",
        "\n",
        "### Process\n",
        "1. **Image Fetching**: The image is downloaded from the given URL using `requests.get(url)`.\n",
        "2. **Image Opening**: The downloaded image is opened using `Image.open(BytesIO(response.content))`.\n",
        "3. **Display and Size Info**:\n",
        "   - The original image is displayed.\n",
        "   - The size (dimensions) of the original image is printed.\n",
        "\n",
        "## Image Resizing\n",
        "\n",
        "### Process\n",
        "1. **Resizing**: The image is resized to 224x224 pixels using `img.resize((224, 224))`.\n",
        "2. **Display**: The resized image is displayed.\n",
        "\n",
        "## Conversion to Grayscale\n",
        "\n",
        "### Process\n",
        "1. **Grayscale Conversion**: The resized image is converted to grayscale using `img_resized.convert('L')`.\n",
        "2. **Display and Size Info**:\n",
        "   - The grayscale image is displayed.\n",
        "   - The size of the grayscale image is printed.\n",
        "\n",
        "## Convolution with Random Filters\n",
        "\n",
        "### Process\n",
        "1. **Image Array Conversion**: The grayscale image is converted to a NumPy array.\n",
        "2. **Convolution Loop**:\n",
        "   - For 10 iterations, a 5x5 random filter is generated.\n",
        "   - Each filter is applied to the image array using `convolve2d` from the `scipy.signal` module.\n",
        "   - The convolution operation combines the filter with the image, creating a feature map.\n",
        "   - Both the random filter and the resulting feature map are displayed side by side.\n",
        "\n",
        "### Convolution Operation\n",
        "- Each random filter interacts differently with the image, highlighting various features.\n",
        "- The 'same' mode in `convolve2d` ensures the output feature map has the same size as the input image.\n",
        "\n",
        "### Display\n",
        "- For each iteration, two subplots are created:\n",
        "   - The left subplot shows the random filter.\n",
        "   - The right subplot shows the feature map resulting from applying the filter to the image.\n",
        "\n",
        "## Conclusion\n",
        "\n",
        "This code effectively demonstrates fundamental image processing techniques such as resizing, color space conversion, and convolution. The convolution with random filters illustrates how different patterns and textures in an image can be emphasized, a concept crucial in advanced image processing and machine learning applications in computer vision."
      ]
    }
  ]
}