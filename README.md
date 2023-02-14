# Face_Mask_Detection
Face Mask detection using CNN, Haar Cascade frontal face algorithm

![218705098-1b8e247b-dfde-48cb-b04c-5a75f65f8010](https://user-images.githubusercontent.com/119114379/218714006-a18c0891-9ff3-4f5f-8426-3f9727f97379.png)

## About Dataset

### Link
https://www.kaggle.com/datasets/ashishjangra27/face-mask-12k-images-dataset?datasetId=675484&sortBy=voteCount

### Context
This dataset is used for Face Mask Detection Classification with images. The dataset consists of almost 12K images which are almost 328.92MB in size.This dataset is already divided into three chunks (train (80%), test (10%), validation (10%)). Data is divided equaly between the two classes.

### Acknowledgments
All the images with the face mask (~6K) are scrapped from google search and all the images without the face mask are preprocessed from the CelebFace dataset created by Jessica Li (https://www.kaggle.com/jessicali9530). Thank you so much Jessica for providing a wonderful dataset to the community.

### Inspiration
The inspiration behind creating this dataset is to create an algorithm that can directly detect is a person is wearing a face mask or not. So I've scrapped the images from google as well as from the CelebFace dataset created by Jessica Li (https://www.kaggle.com/jessicali9530) to make this happen.


## Code

### Data Visualization
1- 12k images divided equaly between two classes (with/without mask).   
2- Divided into three chunks (train (80%), test (10%), validation (10%)).   
3- Images are RGB.   

### Data preprocessing
1- Adujst brightness range.   
2- Rescale the Images pixel values to be between 0 and 1.   
3- Rescale the images dimensions to be fed into model (256, 256).   
4- group images into array to feed it into model (32, 256, 256, 3) were batch size = 32.   

### CNN Model
#### Model architecture
##### Sequential Model
1- 4 successive Sequences of Convolution (Relu) ,MaxPooling and Dropout(0.2) layers.   
2- Flattening layer.   
3- Dense (Relu) layer with a Dropout layer.   
4- Output (Sigmoid) layer.   
5- 800k parameters.
#### Model Compile
1- Optimizer Adam.   
2- Loss function Binary Cross Entropy.    
3- Metrics Accuracy.    
### Realtime prediction
1- Using Haar Cascade algorithm we can detect front faces.   
2- Crop the detected face from the rest of the image.      
3- Pass the cropped image to the model to predict the result.   
4- print the result in the image under the front face detected.   



