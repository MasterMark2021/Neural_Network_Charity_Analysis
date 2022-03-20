# Neural_Network_Charity_Analysis
Neural_Network

**Data Pre_Processing**
After reading in the charity_data.csv file to a Pandas DataFrame, the "EIN" and "NAME" columns were dropped from the dataset. These identification columns did not contain any valuable information.

Columns with more than 10 unique values, such as the "CLASSIFICATION" and "APPLICATION_TYPE" columns, have had their rare categorical variables binned into a new "other" column. A list of categorical variables is generated and is then encoded using OneHotEncoder. These encoded variable names are added to a new Dataframe. After merging the one-hot encoded features, the originals are dropped.

The variable considered the target for this model is "IS_SUCCESSFUL," all other variables in the dataframe are  features. The numerical variables are standardized using Scikit-Learn’s StandardScaler module.

**Compiling, Training, and Evaluating the Model**
After pre_processing the data, a deep learning model is to create a binary classification model that can predict if an "Alphabet Soup" funded organization will be successful based on the features in the dataset we have created.

ReLU is used as the activation function for both the first and second hidden layers. For the output layer, a sigmoid activation function is used. While training the model, a callback saves the model's weights every 50 epochs. After training, the model's Loss and Accuracy values are evaluated, these values are visible in the output of the codes.

