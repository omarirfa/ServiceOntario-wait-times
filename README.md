# ServiceOntario-wait-times
Due to the COVID-19 pandemic, [unemployment] level is on the rise. However, even during these troubling times, the amount of fake job postings have also increased in [Canada] and in [North America] as a whole. This project aims to create a classification model to help users identify fraudulent job postings.   

### Objectives
- Devise a method to combine all the useful columns.
- Create a classification model to differentiate between fraudulent and real jobs.
- Produce insights on how fake jobs differ from real job postings.



### Dataset
The [dataset] is available on the ServiceOntario website. It contains 18K job postings where 866 are fake job postings and 17014 are real job postings. In the fraudulent column, 0 represents real job postings while, 1 represents fake job postings.


### Method
Method can be divided into three stages:
- Preprocessing: NaN values were replaced with blanks. Since we wanted to evaluate the different aspects of a job posting, a new column was created which consists of the title, location, company profile, description, requirements and benefits. Since it is an imbalanced dataset, undersampling was utilized for the majority class (real jobs) to balance out against the minority class (fake jobs). A train and test split was done on the texts to create training and testing sets.
  - Since machine learning models can only process numerical data, we have to convert the input text. To do so Term frequency-inverse document frequency (TFIDF) vectorizer was utilized to create training and testing vectors. Countvectorizer was not used since it only counts the number of times a word appears in the document which will skew the results. While, TFIDF sees the overall document weightage of each word.

- Models: Multinomial Naive-Bayes, RandomForest, Logistic Regression and Support Vector machine were utilized to evaluate the set. F1 score was utilized to determine the efficiency of each model.

- Visualisation: Confusion matrix were made for each model to show how effectively did it classify. Graphs were made for required experience, function, industry, employment type, countries, and required education. NA was replaced for NaN values for better visualisation.

Please refer to the results folder for insights and metrics utilized.

### Improvements
This project can be improved in several ways, in terms of data preprocessing, data visualisation and models.


[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)


   [Seaborn]: <https://seaborn.pydata.org/>
   [Pandas]: <https://pandas.pydata.org/>
   [NumPy]: <https://numpy.org/>
   [Scikit-learn]: <https://scikit-learn.org/>
   [Matplotlib]: <https://matplotlib.org/>
   [Bokeh]: <https://docs.bokeh.org/en/latest/index.html>
   [Plotly]: <https://plotly.com/> 
   [Nlppreprocess]: <https://github.com/gaganmanku96/nlppreprocess>
   [Gensim]: <https://pypi.org/project/gensim/>
   [SpaCy]: <https://spacy.io/>
   [NLTK]: <https://www.nltk.org/>
   [Imbalanced-learn]: <https://imbalanced-learn.readthedocs.io/en/stable/>
   [techniques]:<https://towardsdatascience.com/data-augmentation-in-nlp-2801a34dfc28>
   [dataset]:<https://data.ontario.ca/dataset/serviceontario-wait-times-and-call-volumes-contact-centres>
   [North America]:<https://www.forbes.com/sites/ashleystahl/2020/05/11/job-hunting-scams-amid-covid-19-pandemic/#694498c3c57d>
   [Canada]:<https://globalnews.ca/news/7046534/scammers-target-online-job-seekers-during-covid-19-pandemic/>
   [unemployment]:<https://www.nytimes.com/interactive/2020/05/08/business/economy/april-jobs-report.html>
   
   
   
  
