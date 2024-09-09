# SPAM-detection-in-SMS-and-Emails
Developed a spam detection model using Python, applying Naive Bayes, Random Forest, and SVM algorithms. Achieved over 97% accuracy on an SMS dataset through data cleaning, EDA, and feature engineering. Utilized Pandas, NLTK, Scikit-learn, and Seaborn for data manipulation, model training, and evaluation.

### 1. **Data Cleaning**:
   - Dropped unnecessary columns (`Unnamed: 2`, `Unnamed: 3`, `Unnamed: 4`).
   - Renamed columns `v1` and `v2` to `target` and `text`.
   - Removed duplicate entries (403 duplicates found and dropped).
   - Encoded `target` as 0 for ham (non-spam) and 1 for spam.

### 2. **Exploratory Data Analysis (EDA)**:
   - Visualized the class distribution (imbalanced dataset: 4516 ham vs. 653 spam).
   - Created new features:
     - `num_characters`: Number of characters in each message.
     - `num_words`: Number of words in each message.
     - `num_sentences`: Number of sentences in each message.
   - Visualized the data distribution for spam and ham using histograms and pair plots.
   
### 3. **Text Preprocessing**:
   - Tokenized and transformed text data:
     - Converted text to lowercase.
     - Removed stopwords and punctuation.
     - Applied stemming using the `PorterStemmer`.
   - Visualized common words in spam and ham using word clouds.
   - Created a corpus of words for spam and ham messages, showing word frequency distribution.

### 4. **Model Building**:
   - Vectorized the text data using `TfidfVectorizer` (max features set to 3000).
   - Split the data into training and testing sets.
   - Trained and evaluated several classifiers:
     - Naive Bayes (Gaussian, Multinomial, and Bernoulli).
     - Logistic Regression, SVM, Decision Trees, Random Forest, KNN, XGBoost, etc.
   - Calculated accuracy and precision for each classifier.

### **Current Results**:
- The Multinomial Naive Bayes model (`mnb`) performed exceptionally well with an accuracy of **97.2%** and precision of **1.0**.
- SVM with sigmoid kernel showed a similar high performance with **97.2%** accuracy and **97.4%** precision.
