# Face Mask Detection

to get the data for this project 'https://www.kaggle.com/datasets/omkargurav/face-mask-dataset' to get the right directory download the data in your local machine and in your project.

you can run this code as jupyter notebook using visual studio code or anaconda and download the data from the previous link.

In this problem I use Transfere Learning to make the model classify if the person wearing mask or not so I used MobileNetV2 based on ImageNet pretrained model.

firs I start to prepar the data so I crate function called create_training_data() reads each image file into an array using openCV library then resize the image and append it to the 'training_Data' list.
Overall, this function reads and resizes images from a directory and creates training data in the form of a list of arrays and numerical labels, which can be used to train a machine learning model.

then I shuffle the data and separate it to features and label and normalize the images.

then I save all changes and preproccessing using pickle library.

then I implement the MobileNetV2 and set the weight to ImageNet and freez the top layer and define the input shape.
and I compile the model I used Adam optimizer and sparse_categorical_crossentropy loss and accuracy metric.

then convert both label and features to numpy array.

Fit the model to data and get result 0.99% accuracy score for training and 0.95% accuracy score for validation set.
and I save this trained model to make prediction on unknown images.

