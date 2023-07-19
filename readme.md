# NLP - Fake News Detection

## Goals and Scope:
**Description:** The aim of this NLP project is to create a classification model that can determine whether a given article is fake news, based on word content and structure.

**Models:** I have created two models, both trained on the popular ISOT dataset and differing only in the Word2Vec vectors used; Model A is custom-trained, while Model B simply uses Google's pre-trained Word2Vec to achieve similar results. Both models are tested on a remaining portion of the ISOT dataset, along with a Kaggle news dataset I chose at random.

**Hypothesis:** I expect these models to be better at picking up on differences in writing style rather than actual accuracy. Since the "True" news set is filled only with Reuters articles, I also expect my own trained vectors to perform worse on data outside of the ISOT dataset than Google's own pretrained vectors.

**Limitations:** The bulk of the data I used is locked to a certain period of time, from 2016 to early 2018, and covering a limited variety of subjects. This is by design, as in theory this would let me test the models on other kinds of articles (and even from other date ranges) and more effectively work out how to improve later iterations of the model.

## Instructions:
**Note:** "Notebook 2 - Model Creation" is crucial for packaging and later loading the models, which are pickled, for testing. Using these models along with the preprocessed datasets, one can skip Notebook 1 entirely when testing the models for themselves.

Otherwise, the notebooks should be executed in the following order:
    1. Notebook 1 - Setup & Data Preprocessing
    2. Notebook 2 - Model Creation
    3. Notebook 3 - Model Validation

Notebook X exists just to provide a handful of other visualisations for the presentation component of this project, and as such is largely optional.

## Conclusion
**Outcome:** The models appear capable of predicting fake news with some degree of success, accurately classifying a given article as fake over 60% of the time with the Kaggle dataset and around/over 70% with the remainder of the ISOT dataset. My central hypotheses also appear to have been proven true, at least in part; Model B was slightly more effective, overall, on a smaller test dataset that was not part of the ISOT training dataset, but because it had not been trained on the data from the article it wasn't as capable of working out word relevant patterns quite as well as Model A. 

**Challenges:** The biggest challenges to me completing this project were CPU/hardware constraints, paired with time. I had more ideas I wanted to try out but I simply did not have the means to do so before the deadline.

**Going Forward:** Ideally, I'd like to work out a reliable means of improving my models and having them be more accurate. Whether this means training them with a more robust dataset, or else trying a different NLP method entirely such as BERT, has yet to be determined.