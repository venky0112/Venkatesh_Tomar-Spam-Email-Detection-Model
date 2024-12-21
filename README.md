# Realtime Spam Detection using Logistic Regression

This repository not only houses Python code for detecting spam emails using Logistic Regression but also incorporates real-time email collection functionality. Upon receiving an email from a specified email address, the system promptly collects the body of the message. This allows for dynamic and up-to-date training of the model. The model itself is trained on a comprehensive dataset comprising email messages that have been meticulously labeled as either spam or ham (non-spam). By continuously gathering new email data in real-time, the system ensures that the model remains robust and adept at discerning between legitimate and unsolicited messages, thus enhancing its effectiveness in combatting spam.

## Dependencies

- numpy
- pandas
- scikit-learn

## Installation

You can install the required dependencies using pip:

```bash
pip install numpy pandas scikit-learn
```

## Working

1. Ensure you have a CSV file containing email data. By default, the code assumes the file is named `spam.csv` and contains columns named `Message` and `Category` (spam or ham).

### Data Collection & Pre-Processing

- Load the data from the CSV file into a pandas DataFrame.
- Replace null values with an empty string.
- Label encode the categories: spam as 0, ham as 1.

### Splitting the Data

- Split the data into training and test sets.

### Feature Extraction

- Convert text data into feature vectors using TF-IDF vectorization.

### Training the Model

- Train a Logistic Regression model using the training data.

### Evaluating the Model

- Evaluate the accuracy of the model on both training and test data.

### Building a Predictive System

- Connect to a Gmail account using IMAP.
- Fetch emails from the inbox.
- Predict whether each email is spam or not using the trained model.

## Configuration

- Update the file path in the code to point to your CSV file if it's not named `spam.csv`.
- Adjust the IMAP settings (`user`, `password`, `imap_url`) according to your email provider.
