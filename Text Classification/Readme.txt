Title:
Text Classification with Pre-trained Models

Project Description:
This notebook demonstrates Text Classification and related NLP tasks using the spaCy library. The tasks include stop-word removal, lemmatization, part-of-speech tagging, named entity recognition, and training a custom text classification model.

Approach:
Environment Setup:

Installs the necessary spaCy model (en_core_web_sm) and associated utilities.
Text Preprocessing:

Stop-word Removal: Filters out common words (e.g., "the," "is") that do not add significant meaning.
Lemmatization: Reduces words to their base or root form.
Part-of-Speech Tagging: Annotates words with grammatical information.
Named Entity Recognition:

Identifies entities such as names, dates, or locations in the text and categorizes them (e.g., PERSON, DATE, ORG).
Text Classification:

Sets up a spaCy pipeline for text classification.
Adds custom labels (e.g., "POSITIVE") to train a model for sentiment analysis or categorization tasks.

Metrics:
Accuracy: Measures the proportion of correct predictions.
Precision & Recall: Assess the relevance and completeness of the predictions.
F1 Score: Balances precision and recall for imbalanced datasets.