# Covid-19-cases-predicition-with-LSTM-cells

A deep learning project based on Recurrent neural networks in order to predict the number of new Covid-19 cases in Canada.
Since Canada has borders with only one country, The united states of america, we decided to take into consideration 3 variables:
Number of cases in the world, Canada and the United States.

* Uploaded and resized +4000 frames of videos from personal travels using OS and openCV.
* Created custom tensors from the pictures using Pytorch (250 batches of 16 tensors).
* Built a deep neural network (2 CNN and 3 Linear) to identify the location images.
* Achieved 98.31% accuracy on training set and 96.5% on testing set.
* Visualized a batch of testing data with Matplotlib and Mathematical methods.


# Resources Used
* Python Version: 3.7
* CUDA Toolkit 11.5.119 
* Packages and Libraries: pandas, numpy, matplotlib, sklearn, keras, math.
# Data used
* Data on COVID-19 (coronavirus) by Our World in Data from 24/2/2020 to 2021-12-06 (https://github.com/owid/covid-19-data/tree/master/public/data)

# Data preparation
* Select related locations: World, Canada and United States.
* Transformed features by scaling data with MinMaxScaler.
* Split and reshaped training and testing sets to be used in the Deep Neural networks.

# Initial model:
* 2 LSTMs of 64 units:

![image 1](https://github.com/YoussefAithaddou/Covid-19-cases-predicition-with-LSTM-cells/blob/main/Initial_model.PNG)

###### Model layers:
* 2x CNNs
* 2x Pooling layers
* 3x Linear neurons
###### Hyper parameters:
* Batch size: 16
* Epochs: 3
# Model Evaluation:
* Accuracy on training set is 98.28 %
* Accuracy on testing set is 93.50 %
# Sample visualization:
* I used a batch of test data (4 images from each location) to asses how the model predict the location of each frame:

![image 2](https://github.com/YoussefAithaddou/CNN-to-predict-locations-of-my-previous-trips/blob/main/result%20sample.png)

* This model achieved a high accuracy rate with a small training sets due to the fact that all pictures are relatively similar to each other (frames of the same video). In this particular sample, the model manages to accurately identify each location the frames belong to. That is, on average we can accurately identify pictures at a ratio of 14.96 frames in each batch of 16.
