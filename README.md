

1.) TABULAR DATA PREDICTION </br>

</br>

The "Tabular playground 2021 linear regression" project presents several solution for a Kaggle competition assigment. </br>
Competitors had to predict a continuous target based on a number of feature columns given in the data. All of the </br>
feature columns, cont1 - cont14 are continuous. The dataset is quite approachable to achieve relatively good results </br>
in the begining, but it is tough to improve the predictions. I used several technics to improve the results. The</br>
following table presents the result of each method.</br>

|                            | Mean Absolute Error|Mean Squared Error |R2 Score|Accuracy with +/- 20% range| 
|----------------------------|--------------------|-------------------|--------|---------------------------|      
|        Statsmodels         |        0.61        |       0.53        |  0.019 |          98.08%           |
|          SKlearn           |        0.61        |       0.53        |  0.019 |          98.08%           | 
|   Improved Sklearn model   |        0.60        |       0.52        |  0.036 |          98.18%           |
| Feed-forward neural network|        0.60        |       0.52        |        |          97.26%           |
|         XGBoost            |        0.60        |       0.51        |  0.057 |          98.25%           |

</br>
2.) MULTICLASS CLASSIFICATION BY WEBCAM</br>
</br>
The aim of the "Numbers_Logistic Regression_FeedForward" project is to identify hand-written single digits in a   </br>
white papper shown to the webcam of the computer. For training I used MNIST dataset, which contains single </br>
hand-written digits. The color of the MNIST digits is white while the background is black. When constructing </br>
the model I used Pytroch libary, softmax function to make the logits score into probability, and cross enthrophy </br> 
for the loss function. I boosted the model for better result with 2 hidden linear layers and rectified linear </br> 
unit after a hidden layer to ignore the negative values to use non linear transformation to the inputs.</br> 
Accuracy after 20 epochs is around 95%, which is quite good result. For using the webcam for the test images </br>
I used a JavaScript code. The only trick I had to perform to get good predictions is to make the webcam image </br>
into inverse (1-values) as the training images had black background and white digits while I write the digits</br>
by a pen on a white paper. The model works with around 95% accuracy.

