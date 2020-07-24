# Movie-Genre-Prediction
Computer Vision models to predict movie genre from poster

Posters are of English movies post 1980. They are split between the en_90 and images folder.

3 different models have been tested for this multi-label classification tasks.
**Model 1** is a simple 6 layer Convolutional Neural Network.
**Model 2** uses a VGG19 model as a base network and the intermediate features are extracted before the fully connected layers. The model has been initialised with imagenet prediction weights.
**Model 3** is a combination of VGG19 and a CNN network. Intermediate features are extracted from both of them, and are concatenated and then used for prediction.

All the models have a softmax followed by binary cross entropy (BCE) loss applied on the output layer, which ensures that each genre is predicted independent of each other.

For measuring the accuracy of these, 2 methods have been proposed. One method chooses the top-3 confident confident genres as output, while the other method chooses a threshold value of 0.5 to be predicted.

Some sample posters along with their predicted outputs have been shown below.



