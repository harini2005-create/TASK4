#Task 4: Breast Cancer Prediction with Logistic Regression

What’s This Project About?
This project is my solution for Task 4. I created a program to predict whether a breast tumor is cancerous (malignant) or not (benign) using a machine learning technique called logistic regression. The program uses the Breast Cancer Wisconsin Dataset (data.csv) to learn from medical data and make predictions. It also shows results with graphs to make the findings clear.

About the Dataset:
The dataset (data.csv) contains measurements from images of breast tumors. The goal is to predict the diagnosis column, which tells us:

M (malignant, cancerous) = 1
B (benign, not cancerous) = 0
The dataset has 32 columns, including id, diagnosis, and 30 measurement columns. There’s also an empty column (Unnamed: 32) that I removed since it’s not useful.

What I Did:
Here’s what my program does in simple steps:

 ->Got the Data Ready:
Loaded the dataset and removed id and Unnamed: 32 since they don’t help predict anything.
Changed M to 1 and B to 0 so the model can understand the labels.
Filled in any missing numbers with the average for that column.
Adjusted the measurements so they’re all on the same scale (this helps the model work better).

 ->Trained the Model:
Split the data: 80% to train the model, 20% to test how well it works.
Used logistic regression to teach the model how to predict if a tumor is malignant or benign.
 
 ->Checked How It Did:
Made a confusion matrix to show how many predictions were right or wrong (like correctly spotting cancerous tumors or mistakes).
 
 ->Calculated three scores:
*Precision: How often the model’s “cancerous” predictions were correct.
*Recall: How many actual cancerous tumors the model found.
*ROC-AUC: A score showing how well the model separates cancerous from non-cancerous tumors (closer to 1 is better).
Drew a ROC curve to show how the model balances catching cancers versus avoiding wrong alarms.

->Tried a Different Cutoff:
Normally, the model says “cancerous” if the probability is over 0.5. I tested a lower cutoff (0.3) to catch more cancerous tumors, even if it means more false alarms. This is important in medicine to avoid missing any cancers.

->Showed the Sigmoid Curve:
Made a graph of the sigmoid function, which is how the model turns numbers into probabilities (like a score between 0 and 1).

What’s in This Repository
task4.py: The Python code that does all the work (loads data, trains the model, shows results, makes graphs).
data.csv: The dataset I used.
README.md: This file, explaining what I did.
plots/ folder: Pictures of the graphs:
confusion_matrix.png: Shows correct and incorrect predictions.
roc_curve.png: Shows how well the model tells apart cancerous and non-cancerous tumors.
sigmoid_function.png: Shows the sigmoid curve used by the model.
