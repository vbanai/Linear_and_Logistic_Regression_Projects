In this section you can find two projects which works with linear regression and logistic regression technics.</br>
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

