# CodeClause_BreastCancerClassification
Python Code for Breast Cancer Classification

1. IMPORTING MODULES
   - pandas: This library is used to manipulate and analyse datasets in the form of structured data frames such as 'CSV' files.
   - NumPy: This library is used for scientific computation such as numerical arrays, functions and multi-dimensional arrays.
   - tkinter: This is used to create a basic user interface in Python
   - filedialog: This helps with providing dialogue boxes for selecting files.
   - messagebox: This displays message boxes for showing information or asking the user for input.
   - train_test_split: This is used for splitting the dataset into training and testing subsets.
   - RandomForestClassifier: This machine learning algorithm is used to make predictions.
   - accuracy_score: This is used to find the accuracy of the predicted model with the help of training and testing subsets and models.
     
2. SETTING GLOBAL VARIABLES
   - We declare dataset, training subsets, testing subsets and classifier as global variables and initialize them to 'None.
   - Setting the values to 'None' helps the program to assign other values to these variables during the program execution.
     
3. FUNCTION FOR UPLOADING DATASET
   - We declare a function named 'upload_dataset' for handling dataset uploadation.
   - The function first accesses the global variables that were declared earlier.
   - Then it displays a dialogue box asking the user to select the file they wish to upload.
   - The function then checks if a file was selected or not, if selected we upload it into 'dataset' in CSV format and then print a success message.
   - If not selected an error message is displayed.
     
4. FUNCTION FOR STARTING CLASSIFICATION
   - We create a function named 'start_classification' that performs the classification process which first accesses the global variables.
   - If no dataset has been uploaded the function displays an error message if not the selected columns are stored in 2 data frames 'X' and 'Y'.
   - We then create the training and testing subsets based on these created data frames with 20% for training and 80% for testing and a random state of 42.
   - We then create an instance of the Random Forest Classifier and fit the training data and a success message is printed at the end.
     
5. FUNCTION TO FIND THE ACCURACY OF THE CLASSIFICATION SYSTEM
    - We then create a function named 'find_accuracy' to find the accuracy of the model.
    - We first access the global variables. If the dataset, training subsets and testing subsets are not available an error message is displayed.
    - If all variables are already available we create a predict variable which predicts the labels using the training subset and testing subset.
    - The accuracy score is then calculated to the precision of 2 decimals and displayed as a message box.
      
6. FUNCTION FOR ENTERING USER INPUT VALUES
    - We first access all the global variables that were declared and show an error message if the dataset or the classifier is none.
    - If all conditions satisfy, then we create a window for the user to enter the values.
    - We then add and pack all the elements of this window where the column names are accessed from the dataset provided for the model.
    - This function helps the user to enter the respective values and the entered data is stored in a dictionary.
    - Once the user clicks the classify button the classify function will be called to perform the required classification on the user's input.
      
7. FUNCTION FOR FINDING THE CLASSIFICATION FOR ENTERED VALUE SET
    - The global variables are accessed and if found to be none, an error message is displayed.
    - We first initialize an empty list to store user data starting from the 3rd column of the dataset.
    - The dictionary that was created earlier is then converted to a list of float values and then reshaped to a NumPy array.
      
8. MAP CLASS LABELS TO NUMERIC VALUES
     - We then map the values of 'B' and 'M' to numeric values 0 and 1.
    - We then use the trained classifier to predict the classification type as well as the probability.
    - The required message is then printed with the classification and probability.
      
9. UI WINDOW
    - We then create an object for Tkinter to represent the main application window.
    - We assign the title for the window along with its size and the background colour configuration
      
10. BUTTONS
    - We then initialize all the buttons for execution.
    - The upload_button calls the upload dataset function and we pack this button.
    - The classification_button calls the start classification function and we pack this button.
    - The accuracy_button calls the find accuracy function and we pack this button.
    - The user_data_button calls the enter user data function and we pack this button.
    - When each of these buttons is clicked the respective functions are executed.
      
11. INITIALIZING THE APPLICATION
    - We then start the Tkinter event loop which is used for continuous events such as buttons or other clicks.
    - The program enters the event loop and remains open until the user exits the program/window.
    - It is important to use this so that the window remains interactive and responsive.
    - Without the mainloop statement the window will be open only for a short time and will close immediately.
