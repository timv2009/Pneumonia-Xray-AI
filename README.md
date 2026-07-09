## Explainable Deep Learning for Pneumonia Detection

## Project Overview

This project uses deep learning to classify chest X-ray images as either **NORMAL** or **PNEUMONIA**. I built the model using transfer learning with ResNet18 and created an interactive web application that allows users to upload an X-ray and receive a prediction.

To help users understand how the model makes decisions, I also implemented Grad-CAM, which generates a heatmap showing the areas of the X-ray that had the greatest influence on the prediction.

The goal of this project was not only to build an accurate image classification model, but also to learn more about explainable artificial intelligence and how machine learning can be applied to medical imaging.
<img width="1408" height="793" alt="homepage" src="https://github.com/user-attachments/assets/cc12f806-f6a3-4fd3-90c0-ebe2ef26b20d" />



## What I Learned

Throughout this project I learned how to:

- Build a deep learning model using PyTorch
- Apply transfer learning with ResNet18
- Preprocess medical image datasets
- Evaluate a model using accuracy, precision, recall, and F1 score
- Implement Grad-CAM to visualize model attention
- Build an interactive application using Gradio
- Organize a machine learning project using GitHub


## Model Information

- Model: ResNet18
- Framework: PyTorch
- Training Method: Transfer Learning
- Classes:
  - NORMAL
  - PNEUMONIA


## Image Processing

Each uploaded chest X-ray goes through the following steps:

1. Resize the image to 224 × 224 pixels
2. Convert the image into a PyTorch tensor
3. Normalize pixel values using ImageNet statistics
4. Run the image through the trained ResNet18 model
5. Generate a Grad-CAM heatmap to explain the prediction


## Results

Metric---Score 
Test Accuracy: 83.81% 
Precision: 0.87 
Recall: 0.84 
F1 Score: 0.83 

### Confusion Matrix

The confusion matrix below summarizes the model's performance on the test dataset.
<img width="438" height="341" alt="confusion_matrix" src="https://github.com/user-attachments/assets/c0514772-6e24-4e8b-bef9-2e61c7fc2959" />


## Repository Files

**Model_Training.ipynb**

Contains the complete model development process, including preprocessing, training, evaluation, Grad-CAM implementation, and error analysis.

**Demo_Application.ipynb**

Contains the interactive Gradio application used to upload chest X-rays, generate predictions, and display Grad-CAM visualizations.

## Example Predictions

Below are examples of the application classifying chest X-ray images.

### Pneumonia Prediction
<img width="1408" height="795" alt="prediction_pneumonia" src="https://github.com/user-attachments/assets/f46b95b4-9c07-4950-993a-4032dc468c60" />

### Normal Prediction
<img width="1408" height="786" alt="prediction_normal" src="https://github.com/user-attachments/assets/f904b5ef-2cad-4f9d-b6ff-87af4c98ea66" />

## Grad-CAM Visualization

To make the model more interpretable, I implemented Grad-CAM, which highlights the image regions that most influenced each prediction. This helps visualize what the neural network is focusing on instead of treating it as a complete "black box."

<img width="1404" height="791" alt="gradcam" src="https://github.com/user-attachments/assets/b0d25d5f-d6fb-4d1e-b320-64b3514dd447" />


## Future Improvements

Some improvements I would like to make include:

- Training on a larger dataset
- Improving overall accuracy
- Adding support for additional lung diseases
- Deploying the application online for public use
- Continuing to improve the user interface


## Disclaimer

This project was created for educational purposes. It is not intended to diagnose medical conditions or replace professional medical advice.
