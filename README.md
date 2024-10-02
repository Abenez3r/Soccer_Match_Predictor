# English Premier League Match Analysis and Prediction System
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)




This project leverages machine learning techniques to predict the outcomes of soccer matches. The system processes match data to extract relevant features, applies rolling averages to track team performance trends, and uses a Random Forest Classifier to make predictions.

## Features
- **Match Data Processing**: Converts various match attributes (venue, time, opponent) into numerical formats suitable for machine learning.
- **Rolling Averages**: Calculates the rolling averages of key match statistics (e.g., goals scored, shots) over the last 3 matches for each team to capture team form.
- **Random Forest Model**: Trained on pre-2022 matches to predict post-2022 match results.
- **Evaluation Metrics**: Includes precision and accuracy metrics to evaluate the model's performance.
- **Custom Team Mapping**: Maps team names to their shortened forms for consistency in analysis.

## Workflow
1. **Data Preprocessing**:
   - Convert categorical and time-related fields into numerical values.
   - Compute rolling averages of match statistics for each team.
   
2. **Model Training**:
   - Train a Random Forest Classifier using pre-2022 match data.
   
3. **Prediction**:
   - Test the model on post-2022 match data.
   - Evaluate performance using precision and accuracy scores.

4. **Team Mapping**:
   - Apply custom mapping to standardize team names.


## Example
Here’s a snippet of how the predictions and actual results are presented:

```plaintext
     actual_x  prediction_x       date        team_x  opponent_x result_x
0           0             1 2022-01-23      Arsenal      Burnley        D
1           1             0 2022-02-10      Arsenal      Wolves         W
2           1             0 2022-02-19      Arsenal      Brentford      W
```

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Abenez3r/soccer-match-prediction.git
   ```
2. Navigate to the project directory:
   ```bash
   cd soccer-match-prediction
   ```
3. Set up a Python virtual environment (recommended). Creating a virtual environment helps manage project-specific dependencies without affecting your global Python installation: 
   
   1. Create the Virtual Environment: Run the following command to create a virtual environment named `venv`:
         ```bash
         python -m venv venv 
         ```
   2. Activate the Virtual Environment:
   
      - On Windows  
         ```bash
         venv\Scripts\activate
         ```
      - On macOS/Linux  
         ```bash
         source venv/bin/activate
         ```
         You should see `(venv)` at the beginning of your terminal prompt, indicating that the virtual environment is active.

4. With the virtual environment activated, install the necessary packages specified in `requirements.txt`:
   ```bash
   pip install -r requirements.txt
   ```
5. Now, you can run the main script for the project:
   ```bash
   python EPL_Prediction_Model.ipynb
   ```
6. Once you are done working in the virtual environment, deactivate it by running:
   ```bash
   deactivate
   ```
   The will return you to your system's default python environment.
7. Remove the Virtual Environment (Optional). If you no longer need the virtual environment, you can remove it by deleting the environment folder. Simply delete the `venv` directory:
   ```bash
   rm -rf venv  # macOS/Linux
   rmdir /s /q venv  # Windows
   ```
   This will completely remove the virtual environment and all its associated files.




## Requirements
- Python 3.7+
- Pandas
- Scikit-learn
- Requests
- BeautifulSoup4

## Files
- `matches.csv`: The dataset containing soccer match details.
- `EPL_Prediction_Model.ipynb`: The main script to preprocess data, train the model, and make predictions.
- `README.md`: Instructions and project overview.
- `requirements.txt`: The necessary dependencies for the project.

