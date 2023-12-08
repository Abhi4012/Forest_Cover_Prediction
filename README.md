# Forest_Cover_Prediction
### <center>The goal of the Project is to predict seven different cover types in four different wilderness areas of the Roosevelt National Forest of Northern Colorado with the best accuracy
#### <span style="font-size: 20px; background-color: yellow; padding: 10px;">libraries import</span>
--------------------------------------------------------------
- imported all libraries
-----------------------------------------------------------------
#### <span style="font-size: 20px; background-color: yellow; padding: 10px;">Dataset import</span>
-----------------------------------------------------------------------------------
-   Imported Dataset 'train.csv'
------------------------------------------------------------------------------------------------------
#### <span style="font-size: 20px; background-color: orange; padding: 10px;">Basics check</span>
- We did basics check about dataset. Here we found one unnecessary column 'Id' then we dropped it.
- During geneerate summary statics of dataset we find 'Soil_Type7' and 'Soil_Type15' have a constant standard deviation, indicating they are constant columns.
------------------------------------------------------------------------------------------------------------
<span style="font-size: 20px; background-color: pink; padding: 10px;">Domain Analysis</span>
- We did domain analysis and got many information about every feature of dataset
------------------------------------------------------------------
<span style="font-size: 20px; background-color: pink; padding: 10px;">Dataset Cleaning</span>
- Data has large column so first we creat a copy of original data
- **Wilderness_Area** and **Soil_type** were already one-hot encoded and it has large feature so I sqeez all unique value in single column. then we dropped all column which is seperated by unique value.
- We used to replace by original name of every feature of **Wilderness_Area** and **Soil_type** column which is all features name provided by dataset.
- also we replace target features value by it's original value.
-----------------------------------------------------------------

<span style="font-size: 20px; background-color: pink; padding: 10px;">EDA</span>
- Dataset target is multiclass classification so we perform Univariate analysis , Bivariet analysis and multivariate and plot graph then  analyse and visilize the graph and get insight about every features.
--------------------------------------------------------------------------------------------------
#### <span style="font-size: 20px; background-color: orange; padding: 10px;">Data preprocessing</span>
- MISSING VALUE
    - Not get missing value.
- DUPLICATE VALUE
    - Duplicate value was not there.
- OUTLIERS
    - During outliers checking we found outliers in many cloumn then by using IQR method we we try to removed outliers of every column one-by-one. aagain i check outliers of column but outliers were showing.
- NORMALIZATION CHECKING
    - WE use to check on numerical column of dataset that value of column is normalized or not then we found all column were not normalize it was looking skewed.
- Data transformation
    - Data was not normalize and it has skewness and not well distrubute so we perform **Power Transformer** it maked our data normalize, again i check normalization and we saw our column was normalized
 ------------------------------------------------------------------------------
<span style="font-size: 20px; background-color: blue; padding: 10px;">Feature Selection</span>
----------------------------------------------------------------------------------------------
 - During feature selection we used to check coorelation on input variable only and we found the no high coorelated data.
----------------------------------------------------------------
<span style="font-size: 20px; background-color: blue; padding: 10px;">Encoding </span>
- we did one-hot-encoding on **Wilderness_Area** and **Soil_type** column becsue we have done Sqeez on this both column so we need to do one-hot-encoding.
-----------------------------------------------------------------
<span style="font-size: 20px; background-color: green; padding: 10px;">Balancing data</span>
--------------------------------------------------------------------------------------------------
- We check wheather target variable is balance or not then we saw target variable and it's all features were balanced. 
--------------------------------------------------------------------------------------
    
<span style="font-size: 20px; background-color: gray; padding: 10px;">Model creation</span>
---------------------------------------------------------------
   -First we seprated the independent and dependent variable in **X** and **y**.
- TRAIN TEST SPLIT
    - Imported train test split 
- MODEL CREATED
 **The Output feature colum heve Multiclass classification feature so for this reason we have chosen this problem statement as multiclass class classification and then we use diffrent Algorithm to check the performance of the diffrent Algorithm this can be checked using f1_score and compare it down by with diffrent model accracy , so whichever model showing highest accuracy score we have chosen that model predction.**
  
  ### I used diffrent ML algorithm

  - 1. Logistic Regression
  - 2. RandomForest Classifier
  - 3. SVM Classifier
  - 4. Decision Tree Classifier
  - 5. AdaBoostClassifier
  - 6. Gradient Boosting Classifier
  - 7. KNeighborsClassifier
  - 8. Naive Bayes Classifier BernoulliNB
  - 9. NaiveBayes classifier GaussianNB
   
#### Out of these Algorithm there is performed some algorithm better than other:

 - RandomForest classifier
 - SVC Classifier
 - DecisionTree Classifier
 - Gradient Descent Classifier
 - KNeighborsClassifier

**After Hyperparameter Tuning some model has performed good there was some variation compare to before and after hyperparmeter tuning it's accuracy decrease in model like in Random forest before tuning it has lhigher accuracy but after uning accuracy is decreased, but in SVM Classifier performance increased after tuning so I selected SVM Classifier Because it is performing well and accuracy is higher than other**
 
 - SVM classifier

**After Hyperparameter tuning I found that some model has  giving well accuracy on data as compare to all model so We have choosen SVM classifier model for future prediction**
