

1.) TABULAR DATA PREDICTION </br>
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
            <td rowspan=8>Positive/Negative Frequency</td>
            <td rowspan=2>Logistic Regression (Sklearn)</td>
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
           <td rowspan=2>Gaussian Naive Bayes Model</td>
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
            <td>96.54%</td>
        </tr>
        <tr>
            <td>96.27%</td>
        </tr>
        <tr>
            <td>95.81%</td>
        </tr>
        <tr>
            <td>95.83%</td>
        </tr>
        <tr>
            <td rowspan=2>L2 Name B</td>
            <td>L3 Name C</td>
        </tr>
        <tr>
            <td>L3 Name D</td>
        </tr>
    </tbody>
</table>
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
2.) SENTIMENT ANALYSIS</br>
</br>
Sentiment Analysis is the most common text classification method that analyses an incoming message and tells </br>
whether the underlying sentiment is positive, or negative. The data I am analyzing is downloaded from Kaggel </br>
and having been scraped from Booking.com. This dataset contains 515,000 customer reviews and scoring of 1493 </br>
luxury hotels across Europe./br> I tried several method and cleaning technics to improve the predictions. The </br>
model and results are the followings: </br>

|                            | Model                         |Clened reviews     |Accurycy|F-Score | Precision |
|----------------------------|-------------------------------|-------------------|--------|--------|-----------|      
|Positive/Negative Frequency | Logistic Regression (Sklearn) |      Yes          | 93.33% | 96.54% |   95.81%  |
|                            |                               |       No          | 92.82% | 96.27% |  95.83%   | 
|   Improved Sklearn model   |        0.60        |       0.52        |  0.036 |          98.18%           |
| Feed-forward neural network|        0.60        |       0.52        |        |          97.26%           |
|         XGBoost            |        0.60        |       0.51        |  0.057 |          98.25%           |



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

