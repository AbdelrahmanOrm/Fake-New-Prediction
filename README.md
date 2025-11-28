# Fake News Detection – Logistic Regression, SVC, and Passive Aggressive Classifier

##  Project Overview
This project is a machine-learning-based Fake News Detection system that classifies news articles as **Real** or **Fake**.  
The goal is to build a text-classification model trained on labeled datasets and then test it manually using user-provided input.

The project includes:
- Data preprocessing  
- Feature extraction using **TF-IDF**  
- Training 3 different models  
- Comparing their accuracy and performance  
- Real-time manual input testing  


## Dataset
The dataset consists of two large CSV files:

- `True.csv` → Contains real, verified news  
- `Fake.csv` → Contains fabricated or misleading news  

Each dataset contains around **21,000+ rows** with 4 columns.

They were combined and labeled as:
- `1` → True news  
- `0` → Fake news  


##  Data Preprocessing
Text data was cleaned using:
- Removing punctuation  
- Removing URLs  
- Lowercasing  
- Removing extra spaces  
- Removing content inside brackets  
- Tokenization  
- Stopword removal  

TF-IDF vectorization was used to convert text into numerical features.


##  Models Used

### 1-  Logistic Regression
A strong baseline for text classification, works extremely well with TF-IDF.

### 2- Linear SVC (Support Vector Classifier)
Often the best classical machine-learning model for text classification.

### 3- Passive Aggressive Classifier
Designed for large-scale news streams, fast, and highly accurate.



##  Model Training
Each model was trained on a **75/25 train-test split**.


All three models were evaluated and compared using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix



## Manual Testing (User Input Prediction)

The project includes a manual testing feature where the user can enter:

- A title
- A news body

 And the model predicts:

- **REAL NEWS**
- **FAKE NEWS**


## How to Run

- Install requirements
      
    If you are using VSCode, you have 2 options to run the notebook:
    
    - **First:** Use the existing dataset in the repo and write:
    
        ```python
        fake_df = pd.read_csv('Fake.csv')
        true_df = pd.read_csv('True.csv')
    
    - **Second:** Use KaggleHub, but make sure to pip install it first.
  
- Run the Notebook

- Use the manual testing block to classify custom text






























