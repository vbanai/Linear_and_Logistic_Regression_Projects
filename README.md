

1.) TABULAR DATA PREDICTION </br>

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
2.) SENTIMENT ANALYSIS</br>
</br>
Sentiment Analysis is the most common text classification method that analyses an incoming message and tells </br>
whether the underlying sentiment is positive, or negative. The data I am analyzing is downloaded from Kaggel </br>
and having been scraped from Booking.com. This dataset contains 515,000 customer reviews and scoring of 1493 </br>
luxury hotels across Europe. I tried several methods and cleaning technics to improve the predictions, and I </br>
evaluated the models by accuracy , f-score, and precision metrics. I made my judgement on performances on the  </br>
basis of the f-score as in binary classification it shows the overall health of the model the best. Best performing </br>
models are the 1D convolutional neural network model and the LSTM DNN on not preprocessed dataset. The worst performing</br>
model is the Bag of Words Gaussian Naive Bayes technic on preprocessed dataset.Used models and their results are presented</br>
in the following table: </br>
</br>
<table>
    <thead>
        <tr>
            <th>Method</th>
            <th>Model</th>
            <th>Dataset</th>
            <th>Accuracy</th>
            <th>F-Score</th>
            <th>Precision</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=8>Positive/Negative<br> Frequency</td>
            <td rowspan=2>Logistic Regression<br> (Sklearn)</td>
            <td>No Preprocessing</td>
            <td>92.82%</td>
            <td>96.27%</td>
            <td>95.83%</td>
        </tr>
        <tr>          
            <td>Preprocessed</td>
            <td>93.33%</td>
            <td>96.54%</td>
            <td>95.81%</td>
        </tr>
        <tr>
           <td rowspan=2>Gaussian Naive Bayes</td>
           <td>No Preprocessing</td>
           <td>92.94%</td>
           <td>96.32%</td>
           <td>96.00%</td>
        </tr>
        <tr>
           <td>Preprocessed</td>
           <td>92.98%</td>
           <td>96.35%</td>
           <td>95.96%</td>
        </tr>
        <tr>
           <td rowspan=2>Decision Tree</td>
           <td>No Preprocessing</td>
           <td>92.07%</td>
           <td>95.86%</td>
           <td>95.85%</td>
        </tr>
        <tr>
           <td>Preprocessed</td>
           <td>92.06%</td>
           <td>95.85%</td>
           <td>95.90%</td>
        </tr>
        <tr>
           <td rowspan=2>XGBoost</td>
           <td>No Preprocessing</td>
           <td>95.67%</td>
           <td>97.79%</td>
           <td>95.67%</td>
        </tr>
        <tr>
           <td>Preprocessed</td>
           <td>95.67%</td>
           <td>97.79%</td>
           <td>95.67%</td>
        </tr>      
        <tr>
            <td rowspan=8>Bag of Words</td>
            <td rowspan=2>Logistic Regression <br>(Sklearn)</td>
            <td>No Preprocessing</td>
            <td>96.14%</td>
            <td>98.01%</td>
            <td>96.91%</td>
        </tr>
        <tr>          
            <td>Preprocessed</td>
            <td>96.11%</td>
            <td>97.99%</td>
            <td>96.78%</td>
        </tr>
        <tr>
           <td rowspan=2>Gaussian Naive Bayes</td>
           <td>No Preprocessing</td>
           <td>85.04%</td>
           <td>91.69%</td>
           <td>97.90%</td>
        </tr>
        <tr>
           <td>Preprocessed</td>
           <td>84.25%</td>
           <td>91.21%</td>
           <td>97.85%</td>
        </tr>
        <tr>
           <td rowspan=2>Decision Tree</td>
           <td>No Preprocessing</td>
           <td>93.60%</td>
           <td>96.65%</td>
           <td>96.66%</td>
        </tr>
        <tr>
           <td>Preprocessed</td>
           <td>93.62%</td>
           <td>96.66%</td>
           <td>96.80%</td>
        </tr>
        <tr>
           <td rowspan=2>XGBoost</td>
           <td>No Preprocessing</td>
           <td>95.92%</td>
           <td>97.79%</td>
           <td>95.67%</td>
        </tr>
        <tr>
           <td>Preprocessed</td>
           <td>95.94%</td>
           <td>97.92%</td>
           <td>96.02%</td>
        </tr>
        <tr>
            <td rowspan=8>Term Frequency - Inverse <br>Document Frequency</td>
            <td rowspan=2>Logistic Regression <br>(Sklearn)</td>
            <td>No Preprocessing</td>
            <td>96.22%</td>
            <td>98.05%</td>
            <td>96.62%</td>
        </tr>
        <tr>          
            <td>Preprocessed</td>
            <td>96.22%</td>
            <td>98.05%</td>
            <td>96.64%</td>
        </tr>
        <tr>
           <td rowspan=2>Gaussian Naive Bayes</td>
           <td>No Preprocessing</td>
           <td>69.70%</td>
           <td>81.32%</td>
           <td>99.12%</td>
        </tr>
        <tr>
           <td>Preprocessed</td>
           <td>70.70%</td>
           <td>82.06%</td>
           <td>99.05%</td>
        </tr>
        <tr>
           <td rowspan=2>Decision Tree</td>
           <td>No Preprocessing</td>
           <td>93.71%</td>
           <td>96.72%</td>
           <td>96.59%</td>
        </tr>
        <tr>
           <td>Preprocessed</td>
           <td>94.06%</td>
           <td>96.90%</td>
           <td>96.70%</td>
        </tr>
        <tr>
           <td rowspan=2>XGBoost</td>
           <td>No Preprocessing</td>
           <td>95.87%</td>
           <td>97.89%</td>
           <td>95.94%</td>
        </tr>
        <tr>
           <td>Preprocessed</td>
           <td>95.92%</td>
           <td>97.91%</td>
           <td>95.98%</td>
        </tr>     
        <tr>
            <td rowspan=5>Deep Neural Network (5 epochs)</td>
            <td rowspan=1>One embedding and <br> hidden layer</td>
            <td>Not converging</td>
        </tr>
        <tr>
           <td rowspan=2>One embedding, one conv1D<br>and one hidden layer</td>
           <td>No Preprocessing</td>
           <td>96.43%</td>
           <td>98.13%</td>
           <td>97.05%</td>
        </tr>
        </tr> 
           <td>Preprocessed</td>
           <td>96.30%</td>
           <td>98.05%</td>
           <td>96.98%</td>
               </tr>
        <tr>
           <td rowspan=2>One embedding, and one <br>bidirectional LSTM layer</td>
           <td>No Preprocessing</td>
           <td>96.46%</td>
           <td>98.14%</td>
           <td>96.98%</td>
        </tr>
        </tr> 
           <td>Preprocessed</td>
           <td>96.44%</td>
           <td>98.13%</td>
           <td>96.97%</td>
    </tbody>
</table>
</br>



</br>
3.) MULTICLASS CLASSIFICATION BY WEBCAM</br>
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

