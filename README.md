# Dataset Description

> We trained our model using the Brain Tumor MRI Dataset from Kaggle, which is a compilation of data from three sources: Figshare, SARTAJ, and Br35H. The final dataset contains a total of 7022 MRI images, divided into four distinct classes:
* Glioma: 1321 MRI images for training and 300 MRI images for testing.
* Meningioma: 1339 MRI images for training and 306 MRI images for testing.
* Pituitary: 1457 MRI images for training and 300 MRI images for testing.
* No Tumor: 1595 MRI images for training and 405 MRI images for testing.
  
The dataset provided a comprehensive and diverse set of images, facilitating robust training for accurate tumor classification. You can find the dataset used for training the model [https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset/data]
Additionally, you can explore the individual datasets that were combined to create this comprehensive collection:
1.	The Figshare dataset can be found [https://figshare.com/articles/dataset/brain_tumor_dataset/1512427/5]
2.	The SARTAJ dataset can be found [ https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri]
3.	The Br35H dataset can be found[https://www.kaggle.com/datasets/ahmedhamada0/brain-tumor-detection?select=no]

# Preprocessing

> The preprocessing script crops MRI images to remove background noise, resizes them to a uniform size of 256x256 pixels, and organizes the processed images into cleaned directories for both training and testing datasets. This ensures that the images are clean and consistently sized for effective deep learning model training.
Data augmentation involves applying random transformations such as
* Rotation Randomly rotate the image within the range [-15, 15] degrees
* Randomly shift the width of the image by up to 10%
* Randomly shift the height of the image by up to 10%
*	Shearing Shear transformation
*	Zooming Randomly zoom in/out up to 20%
*	Flipping Randomly flip the image horizontally
*	Don't flip vertically (as MRI scans are typically acquired from one direction)
*	Fill in empty areas using the nearest pixel value
  
This process increases the diversity of the training dataset, helping to improve the performance and robustness of machine learning models by providing more varied training examples.

# Responsibilities
* Implemented MobileNet for accurate classification of brain tumor types.
* Utilized CNN for effective feature extraction from medical images.
* Integrated SEBlock to enhance the representational power of the neural network.
* Applied Grad-CAM for explainable AI (XAI), providing visual explanations for model predictions.

# Models

> We built 5 deep learning models for detection and classification of brain tumors from medical imaging data, and we selected the model with highest accuracy

# 1. CNN

  ![image](https://github.com/user-attachments/assets/b52883c4-83a6-4602-aa64-3bdea5cdaa0b)

  | Model | Training Accuracy | Test Accuracy | Precision | Recall | F1-Score | AUC  |
  |-------|-------------------|---------------|-----------|--------|----------|------|
  | CNN   | 0.996             | 0.965         | 0.95      | 0.95   | 0.95     | 0.980|

  ![image](https://github.com/user-attachments/assets/0f8f58e4-46f9-4f3f-bd59-164147f67aa8)

# 2. SE-CNN Model
   
  ![image](https://github.com/user-attachments/assets/77110c42-4219-45c9-bbaf-8a00199d989b)

| Model    | Training Accuracy | Test Accuracy | Precision | Recall | F1-Score | AUC  |
|----------|-------------------|---------------|-----------|--------|----------|------|
| SE & CNN | 0.999             | 0.976         | 0.94      | 0.93   | 0.93     | 0.985|

  ![image](https://github.com/user-attachments/assets/dbf31a44-150b-494c-bd4b-e5c674ad7762)

# 3. SECNN-LSTM

  ![image](https://github.com/user-attachments/assets/7bd0a909-c45f-4d9b-b0f4-fbd3427d1873)

| Model       | Training Accuracy | Test Accuracy | Precision | Recall | F1-Score | AUC  |
|-------------|-------------------|---------------|-----------|--------|----------|------|
| CNN SE LSTM | 0.994             | 0.976         | 0.95      | 0.95   | 0.95     | 0.989|

  ![image](https://github.com/user-attachments/assets/4f6a64bb-5c51-49df-a20e-febd4a118e90)

# 4. SECNN-MNet 1 Model

  ![image](https://github.com/user-attachments/assets/a6fc494e-d685-4404-883e-a2bf9412fbb7)

| Model         | Training Accuracy | Test Accuracy | Precision | Recall | F1-Score | AUC  |
|---------------|-------------------|---------------|-----------|--------|----------|------|
| MNet SE CNN 1 | 0.991             | 0.986         | 0.97      | 0.97   | 0.97     | 0.993|

  ![image](https://github.com/user-attachments/assets/ec0989c1-bd2d-4306-9691-f60bddc9dfb0)

# 5. SECNN-Mnet 2 Model

  ![image](https://github.com/user-attachments/assets/ad7cde2c-84ff-4295-8170-6df1bbe338e3)
  ![image](https://github.com/user-attachments/assets/3ef9b47f-7950-4d8c-b8b4-2c2ecbb92815)
  ![image](https://github.com/user-attachments/assets/5cddb27d-8dd6-42fc-9288-360e5b9c9f1f)

# Explainability Analysis (Grad Cam)
 
![image](https://github.com/user-attachments/assets/3fb30fa5-e11c-4df6-a001-c4a8b79fa978)
![image](https://github.com/user-attachments/assets/b185af16-6328-4ad4-b469-28188e673f12)
![image](https://github.com/user-attachments/assets/7e835a44-f9d0-40d1-aa22-e3e7f4a323bb)
![image](https://github.com/user-attachments/assets/8fd2263c-70a8-4f8c-acce-8a737d7706e9)
@ offwitt0
