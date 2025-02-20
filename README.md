# Vijayi-WFH-Tech_Assignment_AI-internship_Jan-2025
# Task A: Task Extraction and Categorization
Insights:
-> Effective Rule-Based Extraction:
Used regex patterns for modal verbs like should, must, needs to e.t.c.. and time-related phrases allowed model for accurate task extraction.
Preprocessing of text helped in filtering irrelevant words and enhancing the focus on actionable items.

-> Categorization Logic:
Tasks were correctly categorized into personal, work-related and miscellaneous based on given text.
NLP techniques like POS tagging and stopword removal were crucial in refining task extraction.

Challenges:
-> Contextual Ambiguity:
Some tasks are contextually ambiguous (e.g., "review the proposal") — could be personal or work-related without explicit context.
Solution: Incorporating Named Entity Recognition (NER) or training other small classification model could help.

-> Dependency on Pre-trained Tokenizers:
NLTK’s punkt tokenizer dependency caused issues some issues like lookup error and error for downloding punkt_tab.
Solution: Using spaCy for tokenization of words, sentences and sentence splitting could offer better reliability.

-> Complex Sentences:
Tasks buried in compound sentences will sometimes be missed.
Solution: Implement dependency parsing for better understanding of sentence structure

# Task B: Sentiment Classification (IMDb Reviews)
Insights:
Model Performance:
Achieved 78% accuracy with Logistic Regression and TF-IDF vectorizer.We can increase the model performance by utilizibg the hyper-parameters.

Why TF-IDF Worked:
TF-IDF prioritized unique terms over the common ones, helping differentiate between positive and negative sentiments of users.
It reduced the noise compared to simple Bag-of-Words.

Challenges:
Overfitting with Logistic Regression:
Logistic Regression tended to overfit when the TF-IDF features were increased without proper regularization.
Solution: Tuning hyperparameters like  switching to SVM or using naive bayes mitigates this.

Handling Negations:
Phrases like “not good” were sometimes misclassified as positive due to more token separation.
Solution: Incorporating bi-grams in TF-IDF helped the model to capture negations better (“not good” as a single feature).
Imbalanced Sentiments:

Code Walkthrough links:
# Task - 1 : https://www.loom.com/share/4512459f0d044817b2189da9cad9d412?sid=d705b854-f165-4178-911d-67ebff56e5e0
# Task - 2 : https://www.loom.com/share/168dcae9638c4a2b93726b222111f906?sid=4033b4c7-4af9-46c6-b29d-d2609ef04c50
