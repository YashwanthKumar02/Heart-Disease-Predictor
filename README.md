
# Heart Disease Prediction

The code starts by importing necessary Python modules such as numpy, pandas, scikit-learn's train_test_split, LogisticRegression, and accuracy_score from metrics.

Then, it loads a CSV file called "heart_disease_data.csv" into a pandas DataFrame using the read_csv() method. The code then prints the first five and last five rows of the DataFrame using the head() and tail() methods, respectively. It also displays the number of rows and columns in the DataFrame using the shape attribute.

Next, the code displays some information about the DataFrame, such as the data type of each column and the number of non-null values in each column using the info() method. The isnull() and sum() methods are used to check if there are any missing values in the DataFrame.

The describe() method provides some statistical measures about the data, such as mean, standard deviation, minimum, maximum, and quartiles. The code also checks the distribution of the target variable using the value_counts() method.

Then, the independent variables are separated from the target variable using the drop() method and assigned to the variable X, and the target variable is assigned to the variable Y. The code then prints X and Y to check if the separation was done correctly.

The code splits the data into training and testing sets using the train_test_split() method from scikit-learn. The training set contains 80% of the data, and the testing set contains the remaining 20% of the data. The stratify parameter is set to Y to ensure that the distribution of the target variable is the same in both the training and testing sets. A random state of 2 is set for reproducibility.

Next, a logistic regression model is created using the LogisticRegression() method from scikit-learn, and it is trained using the fit() method with the training data. The accuracy score of the model is calculated using the accuracy_score() method from the metrics module for both the training and testing data.

Finally, the code creates an input_data tuple with some values, converts it into a numpy array using np.asarray(), reshapes it using reshape() method, and uses the predict() method of the model to make a prediction for a single instance. The prediction is printed, and if the prediction is 0, it is interpreted as "The Person does not have a Heart Disease," and if it is 1, it is interpreted as "The Person has Heart Disease."

