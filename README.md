**Face Mask Detection using CNN**

A Convolutional Neural Network (CNN) that classifies face images as wearing a mask or not wearing a mask, built and trained on Google Colab using TensorFlow/Keras.

**📌 Overview**

This project uses a custom CNN (trained from scratch, no pre-trained model) to detect whether a person in an image is wearing a face mask. The model is trained on the Face Mask Dataset from Kaggle.

**🗂️ Dataset**

Source: Kaggle
Classes:
with_mask → label 1
without_mask → label 0
Images are resized to 128x128 and normalized (pixel values scaled to 0–1) before training.

**🧠 Model Architecture**

A CNN built with the following layers:

Conv2D(32, 3x3, ReLU) → MaxPooling2D
Conv2D(64, 3x3, ReLU) → MaxPooling2D
Conv2D(128, 3x3, ReLU) → MaxPooling2D
Flatten
Dense(128, ReLU)
Dropout(0.3)
Dense(1, Sigmoid)
Optimizer: Adam
Loss: Binary Crossentropy
Metric: Accuracy
Epochs: 10
Batch size: 32
10% of training data held out for validation during training.

**⚙️ Setup & Usage**

Open the notebook (Face_Mask_Detection_using_CNN.ipynb) in Google Colab.
Get your Kaggle API key:
Go to Kaggle → Account → API → Create New Token
This downloads a kaggle.json file.
Run the notebook cells in order:
Install Kaggle CLI and upload kaggle.json when prompted.
Download and extract the dataset.
Preprocess images (resize + normalize).
Train the CNN model.
Evaluate on the test set.
To test on a new image, run the last cell and provide the image path when prompted.

**📊 Results**

Metric	Value
Test Accuracy	fill in after training
Test Loss	fill in after training

**🛠️ Tech Stack**

Python
TensorFlow / Keras
OpenCV
NumPy
Matplotlib
scikit-learn
Google Colab

**📁 Files**

Face_Mask_Detection_using_CNN.ipynb — main notebook (data prep, training, evaluation, prediction)
face_mask_detection_using_cnn.py — Python script export of the notebook

