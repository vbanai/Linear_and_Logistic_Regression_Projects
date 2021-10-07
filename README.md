|efe|sdfsd|
|---|-----|

1.) TABULAR DATA PREDICTION </br>

</br>
"Tabular playground 2021 linear regression" project presents a solution for a Kaggle competition assigment,  </br>
where you can use linear regression. Straight Line might only give "good" predictions, and not "great"   </br> 
predictions, but they will be consistently good predictions. Straight line has relatively low variance,   </br>
because the sum of squares are very similar for different datasets. Competitors has to predict a continuous   </br>
target based on a number of feature columns given in the data. All of the feature columns, cont1 - cont14   </br>
are continuous. The test set is realtively large with 200000 rows. I Used Pytorch libary for building the   </br>
linear regression model. I built an accuracy metric function into the modell giving -/+20% range leeway  </br>
for the predicted values compared to the target values. I reached more than 96% accuracy in this way after </br>
50 epochs.</br>
</br>
2.) MULTICLASS CLASSIFICATION BY WEBCAM</br>
</br>
The aim of the "Numbers_Logistic Regression_FeedForward" project is to identify hand-written single digits in a   </br>
white papper shown to the webcam of the computer. For training I used MNIST dataset, which contains single </br>
hand-written digits. The color of the MNIST digits is white while the background is black. When constructing </br>
the model I used Pytroch libary, softmax function to make the logits score into probability, and cross enthropy </br> 
for the loss function. I boosted the model for better result with 2 hidden linear layers and rectified linear </br> 
unit after a hidden layer to ignore the negative values to use non linear transformation to the inputs.</br> 
Accuracy after 20 epochs is around 95%, which is quite good result. For using the webcam for the test images </br>
I used a JavaScript code. The only trick I had to perform to get good predictions is to make the webcam image </br>
into inverse (1-values) as the training images had black background and white digits while I write the digits</br>
by a pen on a white paper. The model works with around 95% accuracy.

