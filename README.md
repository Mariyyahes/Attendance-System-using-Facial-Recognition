# Attendance-System-using-Facial-Recognition
This project implements an attendance system using facial recognition. A deep learning model is built from scratch to identify faces in a video stream from a webcam. The model is trained on a dataset of images of people to be recognized and validated on a separate dataset. The attendance of recognized people is recorded in an Excel worksheet. 

# Dependencies
This project requires the following Python libraries to be installed:
<br />- cv2
<br />- numpy
<br />- tensorflow
<br />- keras
<br />- datetime
<br />- openpyxl

# Model Architecture
The facial recognition model in this project is a deep learning model based on the VGG-Face architecture. It consists of 7 layers, including 2 convolutional layers, 1 max pooling layer, 1 flatten layer, 2 dense layers, and 1 dropout layer. The model is trained using stochastic gradient descent with L2 regularization, and techniques such as data augmentation, early stopping, regularization, and dropout layers are used to avoid overfitting. The model is trained on a dataset of images of people to be recognized and validated on a separate dataset. However, the quality and clarity of the input images can significantly impact the performance of the model.
<br />- The facial recognition model in this project is built from scratch, meaning that it is not a pre-trained model but rather a custom model architecture designed specifically for the task of facial recognition.

# Overfitting
Overfitting is a common issue when training deep learning models from scratch. To avoid overfitting, several techniques are used, including data augmentation, early stopping, regularization, and dropout layers.

# Usage
To use the attendance system using facial recognition, follow these steps:
<br />1. Install the necessary dependencies listed in the README file.
<br />2. Collect images of the people you want to recognize and store them in a folder on your local machine. Ensure that the images are high-quality and resolution for facial recognition.
<br />3. Modify the code to include the new faces. To do this, you can use transfer learning to fine-tune the pre-trained model on the new faces. First, load the pre-trained VGG-Face model using load_model(). Then, add new layers to the model and train it on the new faces using the fit() method. Note that it is important to avoid overfitting by using techniques such as data augmentation, early stopping, regularization, and dropout layers when training the model on new faces.
<br />4. Save the trained model using model.save() for use in the attendance system.
<br />5. Run the attendance system code by executing the Python script. The system will capture a video stream from your webcam and recognize people in the frame. If a recognized person's class probability is above the threshold, the system will record their attendance in an Excel worksheet.

### Note 
that the threshold for recognizing a person may need to be adjusted depending on the quality of the images and the specific use case.
<br />- It is important to note that the performance of the facial recognition model is highly dependent on the quality and clarity of the input images. Clear and high-quality images will generally improve the performance of the model, while blurry or low-quality images may decrease accuracy.
<br />-It is also recommended to train the model on a large and diverse dataset to improve its ability to generalize to new images. However, in the case of this project, as the model is trained on personal laptops, there is no guarantee on the quality of the predictions. Therefore, it is important to keep in mind the limitations of the data used to train the model and to continuously monitor its performance in real-world scenarios.

# Credits
This code's facial recognition model architecture is based on the VGG-Face model. The Excel worksheet is created and updated using the openpyxl library.
