# Face_Mask_Detection
In these tough COVID-19 times, wouldn’t it be satisfying to do something related to it? I decided to build a very simple and basic Convolutional Neural Network (CNN) model using TensorFlow with Keras library and OpenCV to detect if you are wearing a face mask to protect yourself.

To build this model, i m using the dataset for face mask provided by Prajna Bhandary. Here is the link to download it: https://drive.google.com/file/d/18R5-8T26ctmX8qDPhNmM2xU2WNj2xUr_/view, 
It contains 1376 images of people's faces : 686 without mask and 690 with mask.

Before you start : be sure that you are already installed the latest versions of opencv,tensorflow, keras and scikit.

Opencv : https://anaconda.org/conda-forge/opencv

Tensorflow and keras : https://medium.com/@margaretmz/anaconda-jupyter-notebook-tensorflow-and-keras-b91f381405f8

Scikit : https://anaconda.org/anaconda/scikit-learn
## Preprocessing
In the first step, i've done some processing to the data by transform all the images to gray, resize them to a shape of (100,100) and normalize them.
## Building and training the model 
- After the preprocessing of the data, i built a sequential CNN model with various layers such as Conv2D, MaxPooling2D, Flatten, Dropout and Dense.And in the last Dense layer i used a softmax activation function that gives a vector of the propability of the two classes.
- Then i compiled my model using 'adam' as an optimizer and 'categorical_crossentropy' as a loss function.
- I splitted the data using train_test_split function from the scikit library, to 90% of train data and 10% of test data.
- All we need now is to fit the model with the train data and evaluate it to the test data.
## Testing the model
To test the model, i used opencv to make a video capture and process it the same way we done in the preprocessing step and make a prediction using the model we built.
# References

https://www.pyimagesearch.com/

https://towardsdatascience.com/
