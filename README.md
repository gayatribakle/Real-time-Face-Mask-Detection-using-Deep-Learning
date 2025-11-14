# **Real-time-Face-Mask-Detection-using-Deep-Learning**
This project focuses on detecting whether a person is wearing a mask or not using Deep Learning Techniques.

## Features  
- Real-time face mask detection using a webcam/camera feed  
- Detects whether a person is wearing a mask or not  
- Displays bounding boxes with labels on detected faces  
- High accuracy with lightweight model for quick inference



## Demo( RealTime)  



https://github.com/user-attachments/assets/bf649ce0-62d9-4aba-8f2e-bc9cdabec431

## Demo (Static Image)
<img width="591" height="798" alt="Screenshot 2025-11-14 132025" src="https://github.com/user-attachments/assets/14e68703-af7d-4cdb-b03d-ea67452182d0" />


## Dataset Link [
(https://www.kaggle.com/datasets/omkargurav/face-mask-dataset)

## Implementation Steps

This project detects whether a person is wearing a mask or not using a trained deep learning model and real-time webcam input.
Below is the overall flow of how the system works:

### Prepare the Dataset
Create two folders:
WithMask/ (images of people wearing masks)
WithoutMask/ (images of people without masks)
Place both folders inside: DataSet/Data/.

### Load and Preprocess Data
Use ImageDataGenerator to load images.
Resize images, normalize pixel values, and split into training and validation sets.

### Build and Train the Model
Construct a CNN model using Keras/TensorFlow.
Train the network on the prepared dataset.
Save the trained model as best_mask_model.h5.

### Perform Predictions on Images
Load the trained model.
Pass an input image.
Model outputs whether it is With Mask or Without Mask.

### Real-Time Detection Using Webcam
Use OpenCV to open the camera.
Detect faces using Haar Cascade.
For each detected face:
Extract face region
Preprocess
Predict using the trained model
Display result on the video screen with bounding box.

### Run and Test
Run the Python script.
The camera window will show live mask detection.
Press q to exit.
