# Scrapping-Google_Playstore_Reviews-Sentimental-Analysis-BERT

![image](https://user-images.githubusercontent.com/68136798/95117417-2fee1200-070e-11eb-9d10-af0d57f4f069.png)

## Overview
This project covers three parts:  
**1)** Web scrapping of Google playstore reviews.  
**2)** Predicting the Sentiments using Machine Learning models and using BERT.   
**3)** Use FastAPI to build web framework.

### Part 1: Web Scrapping of Google Playstore reviews.
- Web scrapping plays a vital role in collecting the data if there are no API's available. However, web scrapping should be done carefully and only when the data is made public by the owner.
- Keeping these things in mind, we have used google play scraper package to perform the task of data collection.
- We have scraped about 16000 reveiws from Google app play store.
- This data will be further utilized for our next step.
- Scrapping file can be found by the name **"Google Playstore reviews scrapping.ipynb"**

### Part 2: Predicting the Sentiments using Machine Learning models and using BERT
- Sentiment analysis refers to the use of natural language processing, text analysis, computational linguistics, and biometrics to systematically identify, extract, quantify, and study affective states and subjective information.
- Used NLTK and re(regular expression) for text pre processing. File can be found with name **"Sentiment_analysis_Google_playstore_reviews_.ipynb"**
- For generating the labels (Sentiments) we have used ratings as a base. For eg.(Ratings 1-2 : Negative | Ratings 3 : Neutral | Ratings 4-5 : Positive)
- Models applied are ML classification models: Logistic Regression, SVM Classifier, KNN Classifier, Naive Bayes, Random Forest Classifier, Decision Tree Classifier to predict the sentiments.
- Moreover, to improve the classifier we are training the data using BERT (Bi-directional Encoding Representations from Transformers) transformer through Hugging Face.

**How did the ML Models performed?**  
- Multinomial Logistic Regression - 0.579047619047619  
- Naive Bayes - 0.4552380952380952  
- KNN Classifier - 0.36  
- SVM - 0.7066  
- Decision Tree Classifier - 0.6819  
- Random Forest Classifier - 0.7187301587301588  

**How did NLP Model performed?**
- BERT (Training accuracy) - 0.9880036694658105
- BERT (Validation accuracy) - 0.8932655654383737

As it can be seen clearly BERT has outperformed every model.

### Part 3: Use FastAPI to build web framework
- FastAPI is a modern, fast (high-performance), web framework for building APIs with Python 3.6+. Which is why we are using it to build a web framework for our trained model. We have tested it using various reviews from Google playstore.
- A zip file can be found which have all the necessary files.
- Want to know ore about FastAPI? Check out: https://fastapi.tiangolo.com/
- Run FastAPI using: http://127.0.0.1:8000/docs

**NOTE: While installing transformers into your system kindly make sure to download the version 2.6.0 and not 3.6. New version gives error.**

**Snapshot of the working FastAPI**  
![image](https://user-images.githubusercontent.com/68136798/95124985-f02d2780-0719-11eb-85cc-2e9b1c11eea8.png)

![image](https://user-images.githubusercontent.com/68136798/95124994-f3c0ae80-0719-11eb-9757-09b1f673d695.png)
