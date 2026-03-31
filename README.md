Cats vs Dogs Image Classification using CNN


Overview


This project focuses on building a Convolutional Neural Network (CNN) to classify images of cats and dogs. The goal was to understand the complete workflow of an image classification problem, starting from data preprocessing to model evaluation.
The model was trained using TensorFlow and Keras, and achieved an accuracy of approximately 70% on the test dataset.
________________________________________
Motivation
Image classification is a fundamental problem in computer vision and has real-world applications such as surveillance systems, medical imaging, and automated content filtering.
I chose this project to gain practical experience with Convolutional Neural Networks and to understand how deep learning models process and learn from image data.
________________________________________
Dataset
The dataset consists of images of cats and dogs organized into three directories:
•	Training set
•	Validation set
•	Test set
The training and validation datasets contain labeled images, while the test dataset contains unlabeled images used for evaluation.
________________________________________
Approach
1. Data Preprocessing
•	Used ImageDataGenerator to load and preprocess images
•	Rescaled pixel values from [0, 255] to [0, 1]
•	Applied data augmentation techniques such as rotation, shifting, zooming, and flipping to improve generalization
2. Model Architecture
•	Convolutional layers (Conv2D) to extract image features
•	MaxPooling layers to reduce spatial dimensions
•	Fully connected Dense layer for classification
•	Dropout layer to reduce overfitting
•	Sigmoid activation for binary classification
3. Training
•	Optimizer: Adam
•	Loss Function: Binary Crossentropy
•	Metric: Accuracy
________________________________________
Results
The model achieved:
•	Training Accuracy: ~68%
•	Validation Accuracy: ~70%
The performance indicates that the model is able to generalize reasonably well on unseen data.
________________________________________
Challenges Faced
1. Environment Setup Issues
Initially, I faced issues installing TensorFlow locally due to Python version incompatibility. TensorFlow does not support the latest Python versions, which caused installation failures.
Solution:
I switched to Google Colab, which provides a pre-configured environment with TensorFlow installed, allowing me to proceed without setup issues.
________________________________________
2. Data Generator Errors
While creating the test data generator, I encountered errors where no images were detected.
Reason:
The test directory did not follow the expected structure required by flow_from_directory.
Solution:
I reorganized the test images into a subdirectory so that Keras could correctly interpret them.
________________________________________
3. Prediction Errors
During evaluation, I faced a type error when rounding prediction outputs.
Reason:
The model predictions were returned as arrays instead of scalar values.
Solution:
Extracted the scalar value from the array before applying the round() function.
________________________________________
Key Learnings
•	Understanding how CNNs extract features from images
•	Importance of data preprocessing and augmentation
•	Handling real-world debugging issues in ML workflows
•	Working with Keras data generators and model pipelines
________________________________________
How to Run
1.	Open the notebook in Google Colab
2.	Run all cells sequentially
3.	The model will train and display accuracy and loss graphs
4.	Final predictions will be evaluated automatically
________________________________________
Future Improvements
•	Improve accuracy using transfer learning (e.g., MobileNet, ResNet)
•	Reduce model complexity to avoid overfitting
•	Experiment with hyperparameter tuning
________________________________________
Conclusion
This project provided hands-on experience in building and training a CNN for image classification. It also helped in understanding practical challenges and how to debug them effectively.
The project serves as a strong foundation for more advanced deep learning tasks.

