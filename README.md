

1.) TABULAR DATA PREDICTION I. </br>

The "Tabular playground 2021 linear regression" project presents several solutions for a Kaggle competition  </br>
assigment. Competitors had to predict a continuous target based on a number of feature columns given in  </br>
the data. All of the feature columns, cont1 - cont14 are continuous. The dataset is quite approachable  </br>
to achieve relatively good results in the begining, but it is tough to improve the predictions. In this </br>
project I am focusing on trying out different models and not on data cleaning and visualization methods.</br>
I used several technics to improve the results. Random Forest with Yeo-Johnson Transformation and </br> 
K-fold (3 splits) cross validation produced the best result. I think there can still be little room for</br> 
improvement in case of this model if I'd used for example 10 splits for CV, applied outlier removal and  </br>
performed feature selection and parameter tuning (with RandomizedSearchCV, GridSearchCV). The reason   </br> 
I didn' build these techincs into this model is that it would have been very time-consuming to get the  </br>
final results. The following table presents the result of each method.</br>

|           Models           | Mean Absolute Error|Mean Squared Error |R2 Score|Accuracy with +/- 20% range| 
|----------------------------|--------------------|-------------------|--------|---------------------------|      
|        Statsmodels         |        0.61        |       0.53        |  0.019 |          98.08%           |
| Linear Regression (SKlearn)|        0.61        |       0.53        |  0.019 |          98.08%           | 
| Linear Regression with K-fold cross validation |        0.61        |       0.52        |  0.016 |          98.21%           |
| Polynomial Regression with feature selection, Yeo-Johnson transformation and outlier removal |        0.60        |       0.52        |  0.036 |          98.18%           |
| Feed-forward neural network|        0.60        |       0.52        |  0.009 |          97.26%           |
|         XGBoost with cross-validation and YJ transformation          |        0.60        |       0.50        |  0.055 |          98.32%           |
| RandomForest Model with Random Grid (on reduced dataset to save time) |   0.60 | 0.50 | 0.06 |97.34% |

</br>
2.) TABULAR DATA PREDICTION II.</br>
</br>
The reason why I chose "Predict NYC Airbnb Rental Prices" assignment from Kaggle is, that I considered this  
dataset to be quite tough to reach good results by using traditional data scientist methods. I saw on the 
Kaggle competition page that the best models reached only approx. 0,5 R2 score. I was intrested in if I can  
achieve better results. The dataset contains almost 50 thousand airbnb listings in NYC. The purpose of this 
task  is to predict the price of NYC Airbnb rentals based on the data provided. Check my results.</br>
</br>

|           Models           | Mean Absolute Error|Mean Squared Error |R2 Score|Accuracy with +/- 20% range| 
|----------------------------|--------------------|-------------------|--------|---------------------------| 
| Feature Crosses - Keras |        70        |       11000        |  0.14 |          24.06%           |
|        Linear Regression (SKlearn) with Stratified-Shuffle-Split technic     |        53.81        |       8038.27        |  0.38 |          36.44%           |
| Deep Embeddings - Keras + Random Forrest Regressor|        0.01        |       0.07        |  1.0 |          99.97%           | 



3.) SENTIMENT ANALYSIS</br>
</br>
Sentiment Analysis is the most common text classification method that analyses an incoming message and tells </br>
whether the underlying sentiment is positive, or negative. The data I am analyzing is downloaded from Kaggel </br>
and having been scraped from Booking.com. This dataset contains 515,000 customer reviews and scoring of  </br>
1493 luxury hotels across Europe. I tried several methods and cleaning technics to improve the predictions,  </br>
and I evaluated the models by accuracy , f-score, and precision metrics. I made my judgement on performances  </br>
on the basis of the f-score as in binary classification it shows the overall health of the model the best.  </br>
Best performing models are the 1D convolutional neural network model and the LSTM DNN on not    </br>
preprocessed dataset. The worst performing model is the Bag of Words Gaussian Naive Bayes technic  </br>
on preprocessed dataset. The models' results are presented in the following table: </br>
 </br>
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
4.) MULTICLASS CLASSIFICATION BY WEBCAM</br>
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

