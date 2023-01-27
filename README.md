# Text Representation: TF-IDF

This code is using the TF-IDF text representation method to classify news articles. It starts by importing the necessary libraries, including pandas for data manipulation, numpy for numerical operations, and sklearn for machine learning. The code then imports a dataset, "news.csv", and drops unnecessary columns. The data is then loaded into a dataframe and the dimensions are checked for missing or NaN values, which are then removed. The missing values are then filled with the mean, median, or mode of the dataset using the fillna() function.

The code then splits the data into a training and testing set using the train_test_split function from sklearn. The content column is used as the input variables and the source column is used as the output variable. The shape of the training and testing sets are then printed.

The code then uses the sklearn pipeline module to create a classification pipeline to classify the news data. Three attempts are made, using different classifiers: KNN, MultinomialNB, and Random Forest. For each attempt, the pipeline object is created with the TfidfVectorizer() function as the first step, followed by the chosen classifier. The pipeline is then fit to the training data and predictions are made for the test data. The classification report is then printed for each attempt, which includes metrics such as precision, recall, and f1-score.


# Methodology

 The methodology in this code is using the TF-IDF (term frequency-inverse document frequency) text representation method to classify news articles. The TF-IDF method is used to convert text data into numerical values that can be used as input for machine learning algorithms.
 
 # Table (Selected Top-6)
 
 

|   | Original Content                                   | New Content                                       | Removed Words                                     | Further Metrics                                    |
|---|----------------------------------------------------|---------------------------------------------------|---------------------------------------------------|----------------------------------------------------|
| 0 | After reaching his hotel in the city, RM revea...  | reach hotel city RM reveal stay day add step d... | [After, his, in, the, ,, that, his, would, be,... | precision,    recall,  f1-score,  Confusion Matrix |
| 1 | RM aka Kim Namjoon was the first member to joi...  | RM aka Kim Namjoon member join BTS group relea... | [was, the, first, to, ., The, their, on, ,, .,... | precision,    recall,  f1-score,  Confusion Matrix |
| 2 | Billie Eilish's concert was held in Seoul, Sou...  | Billie Eilish concert hold Seoul South Korea a... | ['s, was, in, ,, and, it, was, by, ', and, -, ... | precision,    recall,  f1-score,  Confusion Matrix |
| 3 | BTS ARMY y'all would be missing the members a ...  | BTS ARMY you miss member lot right BTS member ... | [all, would, be, the, a, ,, ?, Well, ,, one, o... | precision,    recall,  f1-score,  Confusion Matrix |
| 4 | BTS member Kim Seokjin aka Jin has the capacit...  | bts member Kim Seokjin aka Jin capacity create... | [has, the, to, ., This, has, through, so, in, ... | precision,    recall,  f1-score,  Confusion Matrix |
| 5 | BTS member J-Hope aka Jung Hoseok has reached ...  | bts member J Hope aka Jung Hoseok reach Chicag... | [-, has, ., He, is, there, for, the, of, the, ... | precision,    recall,  f1-score,  Confusion Matrix |
