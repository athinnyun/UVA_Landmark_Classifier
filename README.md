# UVA Landmark Classifier

In this project, I trained and evaluated three different CNN-based models via transfer learning to classify different landmarks at the University of Virginia. The first model was based on ResNet50 and it achieved a test accuracy of 85.11%. The second one was based on InceptionV3 and it achieved a test accuracy of 74.61%. The final one was based on Xception and it achieved a test accuracy of 86.94%, the highest of all three. For all three I used the same method of training, using a SGD optimizer with a fairly high learning rate to train just the output layer and then an Adadelta optimizer with default values to train the whole net. I tried a few different optimizers and this configuration worked well for me. Additionally, my initial models suffered from bad overfitting so for each model I applied some Elastic Net regularization to the output layer and included a Dropout layer with a rate of 40% just before the fully connected layer. Overall these are pretty good results but I would like to do further experimentation to achieve a higher accuracy. Credits to Rich Nguyen for providing the dataset and preprocessing code.

![UVA Landmarks](https://i.imgur.com/TXWTfWx.png)

![Classifier Accuracy](https://i.imgur.com/YDxCl0Q.png)
