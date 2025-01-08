# Pneumonia Detection Using Deep Learning

## Overview
This project is a web application designed to detect pneumonia from chest X-ray images using a deep learning model. The model is built on the VGG19 architecture and is served through a Flask-based web interface. Users can upload chest X-ray images, and the application predicts whether the image shows signs of pneumonia or is normal.

## Features
- **Deep Learning Model**: Utilizes a VGG19 convolutional neural network (CNN) pretrained on ImageNet, fine-tuned for pneumonia detection.
- **Web Application**: A Flask web app allows users to upload images and receive predictions.
- **Data Preprocessing**: Includes resizing images to 128x128 pixels and augmenting training data.

## Project Structure
- **app.py**: The main Flask application script that handles image uploads and predictions.
- **model_weights/vgg19_model_01.h5**: Pre-trained model weights for the VGG19 network.
- **templates/index.html**: The front-end template for the web application.
- **uploads/**: Directory for storing uploaded images.
- **Pneumonia_detection_DL.ipynb**: Jupyter notebook detailing the data preprocessing, model training, and evaluation.

## Installation

### Prerequisites
- Python 3.6 or higher
- Flask
- TensorFlow  2.18.0
- Keras  3.7.0
- OpenCV
- NumPy
- Pillow

### Steps
1. Clone the repository:
   ```bash
   https://github.com/MAhad01/pneumonia_prediction_project.git
   cd pneumonia_prediction_project
   ```
2. Create and activate python environment using:
   ```bash
   python -m venv {environment name}
   {environment name}\Scripts\activate
   ```
3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the Flask app:
   ```bash
   python app.py
   ```
5. Access the application at `http://127.0.0.1:5000/`.

## Usage
1. Launch the web application.
2. Upload a chest X-ray image using the provided interface.
3. Click the predict button to receive the classification result.

## Model Training
The model was trained on the [Chest X-Ray Images (Pneumonia) dataset](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia) from Kaggle. The dataset includes training, validation, and test sets.

### Steps
1. **Data Loading**: The dataset is downloaded and loaded using OpenCV.
2. **Data Augmentation**: Augmentations such as horizontal and vertical flips, rotation, and shearing are applied.
3. **Model Architecture**: A VGG19 model is used with added dense layers for classification.
4. **Training**: The model is compiled using SGD optimizer and trained with callbacks for early stopping and learning rate reduction.
5. **Evaluation**: The model is evaluated on the validation and test sets for accuracy and loss.


## Contributing
Contributions are welcome! Please fork the repository and submit a pull request.

## Acknowledgements
- The dataset used in this project was provided by Paul Mooney on Kaggle.
- The VGG19 architecture is from the Keras library.

---

Feel free to open an issue if you have any questions or suggestions!

