# NLP-Fake_Job_Posting_prediction-PySpark :detective:
Using NLP techniques in pyspark to detect the fake job postings on hiring websites like indeed.com.
## The data
### Source: https://www.kaggle.com/shivamb/real-or-fake-fake-jobposting-prediction
This dataset contains 18K job descriptions out of which about 800 are fake. The data consists of both textual information and meta-information about the jobs.
## Steps followed:
  ### 1) Preprocessing 
  - Cleaning the target column
  - Handling Nulls
  - Feature Selection
  - Feature Extraction
  - Cleaning text:
       - Removig hashtags and links
       - Removig un wanted charachters and numbers
       - Removig multiple spaces
       - Lower casing all text
       - Tokenization
       - Removig stop words
  ### 2) Feature Vectorization
  - Using string indexer for categorical columns.
  - Using each of the following for vectorizing the textual columns:
      - Hashing TF Vectorizer
      - TFIDF Vectorizer
      - WordtoVec Vectorizer
  ### 3) Training and Evaluating
  After preparing our data for the model, we will try different models and parameters to find the best one for classification of our label, on the 3 datasets which were encoded by different ways, the different models are:
  - Logistic regression
  - One Vs Rest
  - Linear SVC
  - Naive Bayes
  - Multilayer Perceptron Classifier
  
  ### We see that Multilayer Perceptron Classifier with tfidf vectorization has the highest accuracy which is 97%.
