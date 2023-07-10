# CodeClause_BreastCancerClassification
Python Code for Breast Cancer Classification

1. IMPORTING MODULES
   - pandas: This library is used to manipulate and analyse datasets in the form of structured data frames such as 'CSV' files.
   - numpy: This library is used for scientific computation such as numerical arrays, functions and multi-dimensional arrays.
   - tkinter: This is used to create a basic user interface in Python
   - filedialog: This helps with providing dialogue boxes for selecting files.
   - messagebox: This displays message boxes for showing information or asking the user for input.
   - train_test_split: This is used for splitting the dataset into training and testing subsets.
   - RandomForestClassifier: This machine learning algorithm is used to make predictions.
   - accuracy_score: This is used to find the accuracy of the predicted model with the help of training and testing subsets and models.
     
3. SETTING GLOBAL VARIABLES
   - We declare dataset, training subsets, testing subsets and classifier as global variables and initialize them to 'None.
   - Setting the values to 'None' helps the program to assign other values to these variables during the program execution.
     
5. FUNCTION FOR UPLOADING DATASET
   - We declare a function named 'upload_dataset' for handling dataset uploadation.
   - The function first accessess the global variables that were declared earlier.
   - Then it displays a dialogue box asking the user to select the file they wish to upload.
   - The function then checks if a file was selected or not, if selected we upload it into 'dataset' as csv format and then prints a success message.
   - If not selected an error message is displayed.
     
7. FUNCTION FOR STARTING CLASSIFICATION
   - We create a function named 'start_classification' that performs classification process which first accesses the global variables.
   - If no dataset has been uploaded the function displays an error message if not the selected columns are stored into 2 data frames 'X' and 'Y'.
   - We then create the training and testing subsets based on these created data frames with 20% for training and 80% for testing and a random state of 42.
   - We then create an instance of the Random Forest Classifier and fit the training data and a success message is printed at the end.
     
9. FUNCTION TO FIND THE ACCURACY OF THE CLASSIFICATION SYSTEM
    - We then create a function named 'find_accuracy' to find the accuracy of the model.
    - We first access the global variables. If the dataset, training subsets and testing subsets are not available an error message is displayed.
    - If all variables are already available we create a predict variable which predicts the labels using the training subset and testing subset.
    - The accuracy score is then calculated to the precision of 2 decimals and displayed as a message box.
      
11. FUNCTION FOR ENTERING USER INPUT VALUES
12. FUNCTION FOR FINDING THE CLASSIFICATION FOR ENTERED VALUE SET
13. MAP CLASS LABELS TO NUMERIC VALUES
14. UI WINDOW
15. BUTTONS
16. INITIALIZING THE APPLICATION
