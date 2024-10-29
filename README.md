# sms_spam_detector
## Module 21 - Transformers
#### Due Nov 5, 2024
Carolyn Scheese

### Acknoweldgements
I used Google Colab's AI -Tool to create much of the code within this project (see comments within the code). I found the code to be about 90% correct. I also had two tutoring sessions which helped me correct some code. Finially, I attended before and after class office hours and my instructor, Bill 
was able to identify and help me correct the final piece of code that needed to be fixed. 

### Background and Purpose 
You'll be refactoring code from an SMS text classification solution into a function that constructs a linear Support Vector Classification (SVC) model. Once the model is created and trained, you will create a Gradio app to host the application, enabling users to test text messages. The application will provide feedback to users, indicating whether the text is classified as spam or not, based on the model's performance.

### Files 
https://static.bc-edx.com/ai/ail-v-1-0/m19/lms/datasets/attrition.csv
attrition.ipynb from Module 21

## Import
- import pandas as pd
- from sklearn.model_selection import train_test_split
- from sklearn.pipeline import Pipeline
- from sklearn.feature_extraction.text import TfidfVectorizer
- from sklearn.svm import LinearSVC

#### Set the column width to view the text message data.
pd.set_option('max_colwidth', 200)


### Before you Begin 
- Create a new repository in GitHub called _`sms_spam_detector`_
- Add the starter files from Module 21: gradio_sms_text_classification.ipynb, sms_text_classification_solution.ipynb, and SMSSpamCollection.csv

### Note
>I used Google Colab to complete this assignment.

### Instructions 
This challenge consists of the following steps:
#### Create the SMS Classification Function 
1. Using the code in the sms_text_classification_solution.ipynb file, create the sms_classification function in the gradio_sms_text_classification.ipynb by doing the following:
- Set the features variable to the text message column of the DataFrame.
- Set the target variable to the "label" column of the DataFrame.
- Split data into training and testing and set the test_size to 33%.
- Build a pipeline to transform the test set to compare to the training set.
- Fit the model to the transformed training data and return model.
2. Load the SMSSpamCollection.csv into a DataFrame and call the sms_classification function with the DataFrame, and set the result to the "text_clf" variable.

#### Create the SMS Prediction Function
Use the sms_prediction function to predict the classification of a new text by doing the following:
- Create a variable that will hold the prediction of a new text.
- Use a conditional statement that determines if the text message is "ham" or “spam”.
-- If the message is “ham”, the function should return the following message: f'The text message: "{text}", is not spam.'
-- If the message is spam, the function should return the following message: f'The text message: "{text}", is spam.'

#### Create the Gradio Interface Application
1. Create a Gradio Interface application that takes a textbox for the inputs and has a textbox for the output. The textboxes should have labels that describe what each textbox contains.
2. Launch the application and provide the URL to share the application. Your application should look like the following:


3. Use the following text messages to test your application.