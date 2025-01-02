
# Email classification.

# Objective.
The goal of this project was to develop a robust machine learning model capable of accurately predicting whether an email is spam or not. This is a classic supervised classification task, leveraging labeled data to distinguish between spam and non-spam emails.

# Data cleaning.
The dataset was already free of missing values, allowing me to focus primarily on preprocessing the text data. I employed a range of techniques to transform and normalize the textual content into a clean, usable format. To reduce the complexity of words, I utilized the Snowball Stemmer (English version) to reduce words to their root forms.

I also created a custom function that performed the following essential preprocessing tasks:

- Lowercasing all text for uniformity.
- HTML tag removal to ensure clean data for analysis.
- Punctuation elimination to avoid noise in the dataset.
- Replacement of email addresses and numeric values with placeholders, ensuring sensitive information was anonymized.
- Removal of non-alphanumeric characters to clean up irrelevant symbols.
- Additionally, I performed tokenization, breaking the text into individual words (tokens), which simplified the analysis. After processing, I saved the transformed data into a new CSV file for model training.



# Modelling the algorithim.
Once the data was cleaned and ready, I proceeded to split it into training and testing sets. For the classification task, I chose the Gaussian Naive Bayes algorithm, a well-suited model for text classification tasks.

To evaluate the model’s performance, I used a learning curve to visualize its accuracy during training, allowing me to track overfitting or underfitting. I also performed cross-validation to assess the model’s generalizability, ensuring it performs well on unseen data.

Several performance metrics were used to evaluate the model, including F1 score, providing a balance between precision and recall. To gain a deeper understanding of the model’s behavior, I generated a correlation matrix to analyze the confusion matrix components (True Positives, True Negatives, False Positives, False Negatives).

The final model achieved an impressive accuracy of approximately 90%, demonstrating excellent performance in identifying spam emails.

# Deployment.
To ensure the model can be efficiently deployed into a production environment, I saved it as a Pickle file. This enables seamless integration for real-time email classification, allowing the model to make predictions in production without any issues.