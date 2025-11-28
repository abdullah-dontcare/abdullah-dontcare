# Handwritten Digit Recognition (28x20)

This project is a simple neural-network--based handwritten digit
recognition system built using **TensorFlow** and trained on custom
28×20 pixel grayscale images.\
The model takes a **PNG image** of a single handwritten digit as input
and outputs the predicted class (0--9).

The notebook also includes full visualization of the dataset, training
progress, and predictions using **Matplotlib**.

------------------------------------------------------------------------

## 🚀 Features

-   Simple Neural Network (fully connected) built with TensorFlow/Keras\
-   Input size: **28×20 pixel grayscale PNG images**\
-   Training + evaluation inside Google Colab\
-   Data and prediction visualizations using Matplotlib\
-   Model loading & prediction on external PNG images

------------------------------------------------------------------------

## 📁 Project Structure

    ├── notebook.ipynb            # Main Google Colab notebook
    ├── model/                    # (Optional) Saved model files
    ├── samples/                  # Example PNG digit images
    ├── README.md                 # Project documentation
    └── requirements.txt          # Package requirements

------------------------------------------------------------------------

## 🧠 Model Overview

-   Flatten → Dense → Dense architecture\
-   Softmax output layer for 10-class classification\
-   Trained on 28×20 pixel images normalized to \[0,1\]

------------------------------------------------------------------------

## 🖼️ Input Format

The model expects: - `.png` file\
- Grayscale or RGB (automatically converted)\
- Size **28×20** pixels

Example preprocessing used in the notebook:

``` python
import cv2
import numpy as np

img = cv2.imread("digit.png", cv2.IMREAD_GRAYSCALE)
img = cv2.resize(img, (20, 28))
img = img / 255.0
img = img.reshape(1, 28*20)
```

------------------------------------------------------------------------

## 📊 Visualizations

The notebook includes: - Sample images\
- Loss and accuracy curves\
- Prediction results\
- Confusion matrix (if enabled)

All visualizations are generated using **Matplotlib**.

------------------------------------------------------------------------

## ▶️ Running the Project

You can open the notebook directly in Google Colab:

1.  Upload your `notebook.ipynb` to Colab\

2.  Install dependencies:

    ``` bash
    pip install -r requirements.txt
    ```

3.  Run all cells\

4.  Add your own PNG digit images to test predictions

------------------------------------------------------------------------

## 📦 Dependencies

See `requirements.txt`.

------------------------------------------------------------------------

## ✨ Future Improvements

-   CNN architecture for improved accuracy\
-   Data augmentation\
-   Web UI for uploading digits\
-   Convert model to TensorFlow Lite (for mobile)

------------------------------------------------------------------------

## 📜 License

This project is open-source. Feel free to use or modify!
