# Phishing Detection and Accuracy Evaluation on Emails Using DataMining 
This project uses data mining techniques to analyze email content for potential phishing and fraud attempts. By leveraging regular expressions (regex), it identifies suspicious patterns in email messages, classifies them as phishing or non-phishing, and evaluates the model's accuracy. The goal is to automate phishing detection in emails for enhanced security.

### Overview
Phishing attacks are a major threat to online security, often aiming to steal sensitive information from unsuspecting users. This project builds a phishing detection system using a dataset of emails. It applies regular expression patterns to identify phishing and fraud-related keywords within email content. The system classifies emails as phishing or not based on keyword matches, and then evaluates the model's accuracy.

### Dataset
The dataset used in this project is in CSV format, with the following columns:

message: The content of the email, which will be analyzed for phishing or fraud attempts.

label: Ground truth labels indicating whether the email is phishing (1) or not (0). If these labels are unavailable, synthetic labels will be generated for demonstration purposes.
Example of Dataset Structure:

message	               -                         label

"Urgent! Your account has been compromised..."	- 1

"Your invoice is attached. Please review."	    - 0

### Features
1. #### Regex-Based Detection
Two regex patterns are applied to detect phishing and fraud attempts:

##### phishing_regex: 
Identifies suspicious keywords related to phishing attempts, such as:
"password"
"security"
"account"
"urgent requests"

##### fraud_regex: 
Detects keywords typically associated with fraud or financial schemes, such as:
"payment"
"fraud"
"refund"
"unauthorized activity"

These patterns are used to create a new column, phishing_fraud_matches, which indicates whether any of the patterns were detected in the email content.

2. #### Predicted Labels
A new column, predicted_label, is generated based on regex matches:

1 for emails with phishing or fraud matches.
0 for emails with no matches.

3. #### Accuracy Calculation
The model's accuracy is calculated by comparing the predicted_label with the label (ground truth). If ground truth labels are not available, synthetic labels are generated for demonstration purposes.

The accuracy is computed as:
For demonstration, synthetic labels are used, and the model achieves an accuracy rate of 88.79%.

4. #### Visualization
The notebook includes visualizations to help analyze the results:

A bar chart displays the counts of phishing and fraud detections based on regex matches.

### Prerequisites
To run this project, you will need:

Python 3.x: Ensure you have Python 3.x installed on your system.

Required Libraries:
pandas (for data manipulation)
matplotlib (for creating visualizations)
scikit-learn (for machine learning models and evaluation metrics like accuracy)

### Results
Accuracy: The model's accuracy is evaluated and achieved an accuracy rate of 88.79%.

Visualization: The project generates a bar chart that displays the number of phishing and fraud email detections based on the regex-based approach.

### Conclusion
This project provides a basic yet effective phishing detection system using regex patterns to analyze email content. The accuracy of 88.79% demonstrates the potential of regex-based methods for detecting phishing and fraud attempts in emails. This approach can be extended by incorporating more advanced natural language processing (NLP) or machine learning techniques for improved accuracy.
