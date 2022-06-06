# Covid19-Detection-Using-Chest-X-Ray
# Overview
There are several algorithms belonging to the Convolutional Neural Networks (CNN) that can be used to create a model that identifies and detects the possibility of lung infection with the Corona virus by applying some operations to the x-ray images of the chest.
As we mentioned, there are some algorithms such as VGG16, ResNet50, InceptionV3, Xception and others, and in this respect we have relied on the InceptionV3 algorithm, where the model is trained using the InceptionV3 algorithm over 500 epochs on about 2000 chest x-rays.
Inception-V3 is a convolutional neural network that is 48 layers deep, and you can load a pretrained version of the network trained on more than a million images from the ImageNet database, The pretrained network can classify images into 1000 object categories, such as keyboard, mouse, pencil, and many animals, as a result, the network has learned rich feature representations for a wide range of images, the network has an image input size of 299x299.
After we trained the model, we created a Flask API, an Android application, and a web application, the Flask API receives an image from the site or application of the chest x-ray in the form of Base64 and converts it to an image again and then performs the necessary operations to determine whether the lung is infected with the Corona virus or not, then it send the result to the application or website in the form of a Json file which contain the state and percentage value of the state.

# Dataset Used
The dataset for the project was gathered from two sources:
1-	Positive Covid-19 Chest X-ray images: https://github.com/ieee8023/covid-chestxray-dataset
2-	Negative Covid-19 Chest X-ray images:
https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia?resource=download


# Methodology of the project
**1-Building the Model:**
Three custom layers(input Tensor, Flatten, Dense Output) were added to the four different pre-trained models. Building the Model
**2-Training the Model:**
Defined an Image Data Generator to train the models at modified versions of the images, such as at different angles, flips, rotations or shifts.
**3-Making Predictions:**
Predictions were generated by running the trained models on images of the test set. 
**4-Evaluation of the Model:**
Estimating the accuracy of the models and get insights their performance.
**5-Building the Flask API and (Android-Web) Applications:**
Developing the API and making it capable of requesting and responding, then developing and designing Web and Android applications with a simple and light interface for ease of use.

# Evaluations and Results
  
### Classification Reports for Chest X-rays InceptionV3:  
![Classification Report](https://user-images.githubusercontent.com/58918060/172161110-632f2411-e3df-4fc6-8bfd-725f1763eca9.png)

### Model Accuracy for Training and Testing:
 ![Accuracy Graph](https://user-images.githubusercontent.com/58918060/172161114-f4c68581-6d76-4680-b19b-a3a0e8d0057d.png)

### The Model trained on 20 epoch and result 99% Accuracy:
 ![20 Epoch Report](https://user-images.githubusercontent.com/58918060/172161124-d37dabaf-e2cd-489b-8c39-8ac7957544a3.png)

### Covid19 Detection Android app screenshots:
![Android App  (1)](https://user-images.githubusercontent.com/58918060/172161253-1d5b9173-d227-4993-9d74-d56f3ab9decb.png)
![Android App  (2)](https://user-images.githubusercontent.com/58918060/172161259-e8b57430-5337-464c-9375-a0e3cedb18e8.png)
![Android App  (3)](https://user-images.githubusercontent.com/58918060/172161267-92cf732c-4753-4e45-b3c4-48820378480f.png)
![Android App  (4)](https://user-images.githubusercontent.com/58918060/172161270-d6da420b-68f1-4e9b-98a7-5053ff24b3f5.png)

### Covid19 Detection Web app screenshots:
![Web App (1)](https://user-images.githubusercontent.com/58918060/172161237-b4a6b293-8034-4bec-b50b-8f3c77654864.jpg)
![Web App (2)](https://user-images.githubusercontent.com/58918060/172161241-0bdd04ad-7623-48ca-951e-6b8cbcd62b66.jpg)
![Web App (3)](https://user-images.githubusercontent.com/58918060/172161244-8ee173e4-3657-4598-8da8-b0e2bd90d7a2.jpg)

### InceptionV3 Layer View with visualkeras library:
![Layerd View](https://user-images.githubusercontent.com/58918060/172161210-2ff32ec1-4668-4828-8641-679d936d5fff.jpg)


