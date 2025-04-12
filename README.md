# housing-mlops-basic
import joblib

import pandas as pd

 

# Load model

model = joblib.load("model.pkl")

 

# Test data

test_data = pd.DataFrame({"area": [7500], "bedrooms": [3], "bathrooms": [2]})

prediction = model.predict(test_data)

 

print(f"Predicted price: {prediction[0]}")

Add a commit message like:
Copy code

Added test_model.py script

Ensure "Commit directly to the main branch" is selected.
Click "Commit new file".
 

Step 5: Add the README.md File

Click "Add file" > "Create new file".
Name the file README.md.
Paste the following content into the editor:
Content of README.md:

# Housing Price Prediction - MLOps Workflow

 

This repository demonstrates a simple MLOps workflow for predicting housing prices based on features like area, bedrooms, and bathrooms.

 

## Repository Contents

- `Housing.csv`: The dataset used for training the model.

- `train.py`: A script to train the linear regression model and save it as `model.pkl`.

- `test_model.py`: A script to test the trained model by predicting prices for sample inputs.

 

## Usage Instructions

To run this project, you will need Python installed on your local machine. Follow these steps:

 

Clone the repository:
   ```bash

   git clone https://github.com/<your-username>/housing-mlops-basic.git

   cd housing-mlops-basic

Install the required Python libraries:
pip install pandas scikit-learn joblib

Run the training script:
python train.py

Run the test script:
python test_model.py

This will train a linear regression model and use it to predict housing prices.
