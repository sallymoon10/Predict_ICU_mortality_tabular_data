# Predict patient mortality based on patient's tabular data collected during ICU visit

### Highlights:
- Predict ICU mortality based on tabular data (ie. patient information, vitals, etc) by training SVM, random forests, and logistic regression model on tabular data. 
- Obtained 0.78 AUC in mortality prediction using SVM and Random forest model and 0.77AUC using logistic regression model
- Tech: Python (SkLearn, Scipy, Numpy, Pandas), matplotlib)
- Work completed: Data processing (feature scaling, hyperparameter tuning, feature selection) and model evaluation (AUC) 

![Alt text](/assets/results.png?raw=true=50x50  "AUC results on test dataset")

### Dataset:
- MIMIC-III, a freely accessible critical care database. Johnson AEW, Pollard TJ, Shen L, Lehman L, Feng M, Ghassemi M, Moody B, Szolovits P, Celi LA, and Mark RG. Scientific Data (2016). DOI: 10.1038/sdata.2016.35. Available from: http://www.nature.com/articles/sdata201635

### SVM:
- SVM is a binary classification algorithm commonly used during supervised learning
- SVM calculates the best decision boundary (eg. hyperplane) between data with different labels
- To work with non-linear data, SVM models use the kernel trick. The kernel trick is to apply a kernel function (eg. dot product of feature vectors) to the original feature space, so that the original data can be transformed into a higher dimension where datapoints are more linearly separable. 
- The kernel trick is used as opposed to manually mapping data to a higher dimension because it is much more cost efficient

### Random Forest:
- Random forest models are an ensemble of many weak decision trees. Each the prediction output of each weak decision tree is combined together to make the final prediction in a random forest. 
- Each decision tree in a random forest model considers a random subset of features when forming decision questions and only has access to a random subset of training data points
- Random forest is useful because it reduces overfitting problem of a single decision tree and reduces the variance, ultimately improving accuracy. It can also handle missing values well, robust to outliers, handles non-linear parameters well (ie. not a curve-based algorithm) and does not require any feature scaling. 

### Logistic Regression:
- Logistic regression is a linear classifier based on the logistic function (ie. sigmoid function). The model combines the input values lienarly using weights and coefficient values to predict an output value.
- Unlike linear regression that predicts continuous outputs, a logistic regression predicts binary values for binary classification
- Logistic regression model outputs probabilities of a sample belonging to a certain class, and depending on a given threshold, we can classify the sample 

### TFIDF features:
- TF-IDF evaluates how relevant a word token is to a document in a set of documents. This is calculated by multiplying how frequently the word appears in a document and the inverse document frequence of the word across a set of documents. 
- This allows us to rank words that appear numerously in all documents (eg. and, or, etc) lower and rank higher the words that are relevant to understanding the context of the document
- Clinician's notes can be transformed to TF-IDF features and be used to train models to predict variables given text data


### References:
- Course project: CSC2541 (Machine Learning in Healthcare), University of Toronto
