# A Machine Learning Model for Text Classification and Topic Modeling
## Project Overview

This project builds a machine learning model that automatically applies a classification label to textual data, which is intended to represent the main topic of that data.

## Dataset

The model is trained on an excerpt from [DBPedia](https://www.kaggle.com/danofer/dbpedia-classes?select=DBP_wiki_data.csv), a collection that includes 342,782 wikipedia articles which each have 1 of 219 topical classification labels applied to them.

## Process Followed

1.	Preprocessed the text of the DBPedia articles and lemmatized it using the Python NLTK library

2.	Used three topic modeling algorithms—TruncatedSVD, Non-negative matrix factorization, and LatentDirichletAllocation, all from the Python scikit-learn library—to find the main topics of the documents. Using these main topics as features, along with the preprocessed raw text of the articles, trained a Random Forest Classifier from the Python scikit-learn library.

3.	Evaluated the efficacy of the model using the testing data. Tuned the hyperparameters of both the Random Forest Classifier and the three topic modeling algorithms as needed.

4.	Tested the final model on some text that is not part of the training/testing dataset


## Results and Assessment

The final accuracy of the model was 84%, an improvement of 36% in comparison with the benchmark model. What's more, the addition of the main topics identified by the 3 topic modeling algorithms as additional features along with the raw text of the articles improved the accuracy of the model by approximately 8%.

The model was then tested on four article excerpts that are not part of DBPedia. Admittedly, the articles chosen were encyclopedic and had fairly clear, unambiguous topics; nevertheless, the model succeeded in accurately classifying them.

