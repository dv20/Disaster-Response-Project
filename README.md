# Disaster-Response-Project

This project aims to provide a good response by calculating the score for different categories using Machine learning. The top 10 categories are plotted to summarize the visual results.

# Project Summary

•	Data processing and cleaning: The script takes two .csv files as input. It converts string data present in messages into categorical data and then converts the categorical values into numerical. After that, the script removes the duplicate data, merges the clean data in one data frame, and saves it into the database.

•	Build ML Model: After getting the clean data from the above step, the data gets tokenized using Countvectorizer. After then TfidfTransformer is used, and in the last, we use RandomForestClassifier to create the model. The Gridsearchcv is then used to tune the model.

•	Save and Run: The tuned model is then saved in the pickle file, which is then used by the web application to predict the relevance for the different categories.

•	Output: The web application shows the relevance of each category and the top 5 and top 10 categories.

## Instructions to run the Python scripts

In any suitable python environment, copy or download all the folders, and execute the below-given command. Open terminal in the project directory. 

•	Run the process_data.py to process and clean the data use:

python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db 

•	Create the ML pipeline, execute the train_classifier.py using the following command:

python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl

•	Run the following command in the app's directory to run your web app.
python run.py

Once the app is running, go to http://localhost:3001 to see the web app.

## File Description

The data folder consists of three files:

•	The CSV files used for process (disaster_messages.csv, disaster_categories.csv).

•	process_data.py - Python file which carries out the ETL processing.

•	DisasterResponse.db - The output file generated by running the process_data.py file.

The model folder consists of 2 different file.

•	DisasterResponse.db - The input file for the train_classifier.py. It is used to load the clean data.

•	train_classifier.py - It creates the ML model to predict the categories of the input message.

•	classifier.pkl - The output file generated by running the train_classifier.py file.

The folder app consists of a folder named template and run.py file. The run.py helps to port the plot using plotly on the website.

## References

During this course I got help from Udacity mentors as well as previously asked question from other candidates.
