# Age,Gender and Ethnicity Detection Using CNN
 
The age and gender detection dataset is a large-scale collection of over 23,704 face images annotated with age, gender, and ethnicity labels. The dataset spans a wide age range from 0 to 116 years old and includes images with variations in pose, expression, illumination, occlusion, and resolution. This diverse dataset enables the models to learn and generalize from a wide range of facial characteristics. The ethnicity labels encompass various ethnic groups, ensuring the models can capture and classify different ethnicities accurately

DatasetLink:  https://www.kaggle.com/datasets/nipunarora8/age-gender-and-ethnicity-face-data-csv


## Model Architecture and Training:
The age, gender and Ethnicity classification model is built using a CNN architecture. The model consists of multiple layers, including convolutional layers, pooling layers, and dense layers. These layers are designed to extract features from the facial images and learn representations that are discriminative for classification.
The model architecture is as follows:

The first layer is a 2D convolutional layer with 32 filters and a filter size of 3x3. It uses the ReLU activation function and takes input images of size 48x48 pixels.
A max-pooling layer with a pool size of 2x2 is added to downsample the feature maps.
Another convolutional layer with 64 filters and a filter size of 3x3 follows the max-pooling layer.
Another max-pooling layer is added.
The feature maps are then flattened to a 1D vector.
A dense layer with 64 units and ReLU activation is added to capture higher-level features.
The final dense layer consists of 5 units with softmax activation, representing the age categories.

The model is compiled with the Adam optimizer, using sparse categorical cross-entropy loss as the objective function. It is trained for a fixed number of epochs using a batch size of 32.
