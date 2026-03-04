# LW3_Custom_Image_Classifier


GoogleDrive : https://drive.google.com/drive/folders/1EX4q0m2PXxom7mkq0DKd0qww_4OPCw3R?usp=drive_link

GoogleColab : https://colab.research.google.com/drive/1y0sOitPAqN0aJBKZFxla2o-NOSqXpsa0?usp=sharing

Part 2: Training and Evaluating the Image Classification Model

Guide Questions (Student Reflection & Explanation)

Students must answer the following:

1. Dataset Preparation
○ How did you organize your dataset in Google Drive?
  -  MyDrive/
   WILD GRASS PLANT PROJECT/
       ImageDataset/
           Barnyard Grass/
           Bermuda Grass/
           Carabao Grass/
           Carpet Grass/
           Crab Grass/
           Crowfoot Grass/
           Cyperus Grass/
           Giant Reed Grass/
           Goose Grass/
           Itch Grass/
Each folder represents one class, and each folder contains images of that specific grass type.
    
○ Why is folder structure important for TensorFlow image loading?
  - TensorFlow’s image_dataset_from_directory() automatically assigns labels based on folder names.


2. Model Training
○ What is the role of convolutional layers in image classification?
  - Conv2D layers find important features in images like edges, shapes, and textures. In a grass model, they learn leaf shapes and patterns. Early layers find simple edges, while deeper layers find complex plant patterns.

○ Why do we split data into training and validation sets?
  - It split the data into training and validation sets so the model can learn from the training set and be tested on new images to prevent overfitting.

3. Performance Analysis
○ What accuracy did your model achieve?
  - My model achieved about 99% training accuracy and 97–98% validation accuracy, showing strong performance with little overfitting.
    
○ How did the number of images affect the model’s performance?
  - The number of images affects model performance: more images improve generalization, while fewer increase overfitting. A balanced dataset ensures the model can classify all grass classes accurately.

4. Critical Thinking
○ What challenges did you encounter while using your own dataset?
  - Challenges I faced included reading the .zip dataset, fixing folder structure errors, ensuring enough images per class, long training times, and input shape warnings, all of which needed debugging.

○ How can data augmentation improve your model?
  - Data augmentation increases dataset diversity by rotating, flipping, zooming, or shifting images, helping reduce overfitting, improve generalization, and make the model robust to real-world variations like different angles or lighting.

5. Application
○ Suggest a real-world application for your trained model.
  - This model can help farmers identify harmful grasses, use herbicides efficiently, and support research and smart farming.

○ How can this system be integrated into a mobile or web application?
  - The system can be integrated via TensorFlow Lite for mobile apps or TensorFlow.js for web apps, letting users take or upload a grass image, get its type, and see results with treatment suggestions, creating a smart plant recognition tool.


Guide Questions (Student Explanation & Reflection)

Visualization & Overfitting
1. What signs indicated overfitting in your first model?
  - First model had high training accuracy (~99%) but lower validation accuracy (~91%), showing overfitting.
2. How did data augmentation affect validation accuracy?
  - Helped the model see more varied images and improved validation accuracy (~97–98%).

Model Improvement
3. What is the purpose of dropout layers?
  - It prevent overfitting by randomly turning off neurons during training.
4. Why does data augmentation improve generalization?
  - Augmentation helps the model handle new, unseen images better.

Performance Comparison
5. Compare accuracy before and after improvements.
  - Validation accuracy improved from ~91% to ~97–98% after improvements.
6. Which technique contributed most to improvement?
  - Data augmentation contributed the most in improvement.

Deployment & Application
7. Why is saving the model important?
- It allows the trained model to be reused or deployed without retraining.
8. How can this model be deployed in a real-world system?
    - The model can be deployed in a mobile or web app where users upload or take a photo of it, and the system predicts its type in real time.
