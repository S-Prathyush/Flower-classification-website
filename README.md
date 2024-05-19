# Flower Type Prediction Using CNN

This project involves training a deep learning model using Convolutional Neural Networks (CNN) to predict the type of flower from an image. The model is then deployed as a web application, allowing users to upload an image and receive a prediction of the flower type.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Training](#training)
- [Web Deployment](#web-deployment)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)

## Introduction

This project aims to leverage the power of Convolutional Neural Networks (CNN) to accurately classify images of flowers into five categories: daisy, dandelion, rose, sunflower, and tulip. The trained model is integrated into a web application, enabling users to upload images and get predictions directly through their browser.

## Dataset

The dataset used for training the model consists of images of five different types of flowers. The images are preprocessed and augmented to enhance the model's performance and robustness.

## Model Architecture

The CNN model is built using the following architecture:

- **Conv2D**: 32 filters, kernel size (3,3), ReLU activation
- **MaxPooling2D**: Pool size (2,2)
- **Conv2D**: 64 filters, kernel size (3,3), ReLU activation
- **MaxPooling2D**: Pool size (2,2)
- **Conv2D**: 128 filters, kernel size (3,3), ReLU activation
- **MaxPooling2D**: Pool size (2,2)
- **Conv2D**: 128 filters, kernel size (3,3), ReLU activation
- **MaxPooling2D**: Pool size (2,2)
- **Flatten**
- **Dense**: 512 units, ReLU activation
- **Dense**: 5 units, Softmax activation

The model is compiled with the Adam optimizer and categorical cross-entropy loss function.

## Training

The model is trained using an augmented dataset to prevent overfitting and improve generalization. The ImageDataGenerator class from Keras is used for data augmentation, including operations such as rotation, width/height shift, shear, zoom, and horizontal flip.

## Web Deployment

The trained model is deployed as a web application using Flask. Users can upload an image file, and the application will return the predicted flower type. The web interface is styled for a modern and user-friendly experience.

## Installation

To run this project locally, follow these steps:

1. Clone the repository:

2. Create a virtual environment and activate it:

3. Install the required packages:

4. Ensure the `static/uploads` directory exists:

5. Place the trained model file `flower_model.h5` in the project root directory.

## Usage

1. Run the Flask application:
    ```sh
    python app.py
    ```

2. Open your web browser and go to `http://127.0.0.1:5000/`.

3. Upload a JPG image of a flower and click the "Predict" button to see the predicted flower type.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
