# Image-Classification-Pneumonia-Detection
Project Overview:
This project is focused on detecting pneumonia in chest X-ray images using machine learning techniques. The core of the project involves building a model that can classify X-rays as either "Healthy" (no pneumonia) or "Pneumonia".

Key Steps:
Data Loading & Preprocessing:

Image Loading: Images are loaded from two directories, one for healthy X-rays and one for pneumonia X-rays.
Preprocessing: Each image is converted to grayscale, resized to 150x150 pixels, and normalized (values scaled between 0 and 1).
Labeling: Images are labeled with 0 for healthy and 1 for pneumonia.
Dimensionality Reduction with PCA:

PCA (Principal Component Analysis): This technique reduces the dimensionality of the flattened images, retaining 95% of the variance. This helps speed up the model training and reduce overfitting.
Model Training:

Random Forest Classifier: A Random Forest model, an ensemble method combining multiple decision trees, is used.
Hyperparameter Tuning: GridSearchCV finds the best hyperparameters, optimizing the model’s performance.
Training: The best model is trained on the processed data.
Model Saving and Loading:

The trained model is saved using both joblib and pickle for future use. This allows the model to be reloaded and used without retraining.
Prediction Functionality:

A function is implemented to allow the user to input the path to a chest X-ray image during runtime. The image is preprocessed, PCA is applied, and the model predicts whether the X-ray indicates pneumonia or not.
Evaluation:

Accuracy and Confusion Matrix: The model’s performance is evaluated on a test set, and metrics like accuracy and the confusion matrix are generated.
Feature Importance: The importance of the top features used by the Random Forest model is visualized.
Conclusion:
This project effectively uses machine learning and image processing to classify chest X-rays as healthy or pneumonia, providing a practical application of AI in healthcare. The use of PCA for dimensionality reduction and Random Forest for classification ensures the model is both efficient and interpretable, making it suitable for real-world deployment.

