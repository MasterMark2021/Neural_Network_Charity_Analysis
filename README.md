# Neural_Network_Charity_Analysis
Neural_Network

**Data Pre_Processing**
After reading in the charity_data.csv file to a Pandas DataFrame, the "EIN" and "NAME" columns were dropped from the dataset. These identification columns did not contain any valuable information.

Columns with more than 10 unique values, such as the "CLASSIFICATION" and "APPLICATION_TYPE" columns, have had their rare categorical variables binned into a new "other" column. A list of categorical variables is generated and is then encoded using OneHotEncoder. These encoded variable names are added to a new Dataframe. After merging the one-hot encoded features, the originals are dropped.

The variable considered the target for this model is "IS_SUCCESSFUL," all other variables in the dataframe are  features. The numerical variables are standardized using Scikit-Learn’s StandardScaler module.

**Compiling, Training, and Evaluating the Model**
After pre_processing the data, a deep learning model is to create a binary classification model that can predict if an "Alphabet Soup" funded organization will be successful based on the features in the dataset we have created.

ReLU is used as the activation function for both the first and second hidden layers. For the output layer, a sigmoid activation function is used. While training the model, a callback saves the model's weights every 50 epochs. After training, the model's Loss and Accuracy values are evaluated, these values are visible in the output of the codes. See below output image.
![AlphabetSoupCharity_output](https://user-images.githubusercontent.com/93059601/159143258-4d1dada1-85a9-420d-a7f2-d277a313a081.PNG)






**Summary**
None of the optimization attempts in this analysis were able to produce a model with a predictive accuracy level of 75% or higher. The following methods were attempted:

Adding an additional hidden layer.
Adding more neurons to a hidden layer.
Using different activation functions.
Decreasing the number of epochs in the training.
There could be numerous reasons why this model did not reach the targeted predictive accuracy level of 75%. The number of neurons in the hidden layers may need to be adjusted. The number of epochs during trainiing may need to be increased. The input data may have outliers or variables that are confusing the model.

Instead of using a Deep Learning model in this binary classifiication project, it may be preferable to use a Random Forest Classifier. Whereas Deep Learning models are complex to setup and time consuming to train, Random Forest Classifiers are much simpler to setup and can be trained in a matter of seconds. Furthermore, the predictive accuracy level of these two models would most likely be similar. For its ease of implementation and applicability to this situation, it is recommended to use a Random Forest Classifier for future development on this project.
