# Covid-19-cases-predicition-with-LSTM-cells

A deep learning project based on Recurrent neural networks in order to predict the number of new Covid-19 cases in Canada.
Since Canada has borders with only one country, The united states of america, we decided to take into consideration 3 variables:
Number of cases in the world, Canada and the United States.

* Uploaded and prepared Covid-19 Data.
* Created custom tensors from the pictures using Pytorch (250 batches of 16 tensors).
* Built initial RNN model (2 LSTMs of 64 units) to forecast the number of coronavirus cases, achieved MSE =  123.324.
* Performed model optimization with Tensorboard using 36 combination of LSTM and Dense layers.
* Built final model (1 LSTMs of 128 units, 1 Dropout (20%), 1 Flatten and 1 Dense layer) with MSE = 106.181 (Mean error reduction = 14 %).


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
* Model architecture: 2 LSTMs of 64 units.

![image 1](https://github.com/YoussefAithaddou/Covid-19-cases-predicition-with-LSTM-cells/blob/main/Initial_model.PNG)

* Model results: MSE =  123.324.

![image 2](https://github.com/YoussefAithaddou/Covid-19-cases-predicition-with-LSTM-cells/blob/main/Initial_result.png)


# Model optimization with Tensorboard:
* Trying 4x3x3=36 different combinations of LSTM cells and dense layers and 4x5 =20 combinations of batch sizes and epochs:
* Dense layers: 0, 1, 2, 3.
* Number of units: 32, 64, 128.
* LSTM cells: 1, 2, 3.
* Batches: 8, 16, 32, 64.
* Epochs: 20, 40, 60,80,100.

# Final model:
* Model architecture: 1 LSTMs of 128 units, 1 Dropout (20%), 1 Flatten and 1 Dense layer .

![image 3](https://github.com/YoussefAithaddou/Covid-19-cases-predicition-with-LSTM-cells/blob/main/Final_model.PNG)

* Model results: MSE =  106.181.
* Mean error reduction: 14 %

![image 4](https://github.com/YoussefAithaddou/Covid-19-cases-predicition-with-LSTM-cells/blob/main/Final_result.png)


