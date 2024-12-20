# README for Scripts

## Overview 
The **`src/`** folder contains scripts designed to implement the logic for selecting machine learning (ML) and deep learning (DL) models based on data characteristics and predefined rules. These scripts interact with the rules and configuration files located in the **`analysis/data/derivedData/`** folder to provide task-specific guidance for various data types.

The scripts are modular, allowing for easy extension, debugging, and integration with other components of the project. Each script is dedicated to a specific data type, ensuring clarity and maintainability.

***

## Purpose of the study 
To streamline model selection for different data types using structured knowledge and rule-based logic.

## File Structure
- **Audio.ipynb:** Focuses on audio data, supporting classification and feature extraction tasks.
- **Categorical.ipynb:** Deals with datasets containing categorical features, primarily for classification tasks.
- **Image.ipynb:** Processes image datasets for tasks like image classification and object detection.
- **Numerical.ipynb:** Handles datasets with numerical features, supporting tasks like regression and classification.
- **Tabular.ipynb:** Combines numerical and categorical data into a single workflow for structured data analysis.
- **Textual.ipynb:** Manages textual datasets, providing logic for NLP tasks such as text classification and sentiment analysis.
- **Time_series.ipynb:** Handles sequential datasets, offering solutions for forecasting and trend analysis.

***

## How the Scripts Work

1. **Loading Rules:** Each script imports task-specific rules from the corresponding JSON file in the analysis/data/derivedData/ folder. For example:
   ```
   with open("analysis/data/derivedData/rules_categorical.json", "r") as file:
       categorical_data_rules = json.load(file)
2. **Parameter Validation:** Scripts validate input parameters such as dataset type, task, and thresholds using utility functions. Example:
   ```
   def validate_parameters(data_type, task, rules):
       valid_tasks = rules["tasks"].keys()
       if task not in valid_tasks:
           raise ValueError(f"Invalid task: {task}. Choose from {', '.join(valid_tasks)}.")

3. **Logic Validation:** The scripts ensure that the recommended models meet the specified conditions, such as dataset size and real-time requirements.
   ```
   def validate_logic(models, condition=None, dataset_size=None):
       if not models:
           print(f"Warning: No models fit the condition '{condition}' for dataset size '{dataset_size}'.")
           return False
       return True
4. **Model Recommendation:** Based on the validated rules and conditions, the scripts suggest the most suitable ML or DL models for the task.

***

## Usage Instructions
### Step 1: Select the Relevant Script
Identify the script that matches your dataset type. For example:
   - For numerical datasets, use Numerical.ipynb.
   - For textual datasets, use Textual.ipynb.
### Step 2: Load Your Data
Ensure your dataset is properly formatted and accessible for analysis.
### Step 3: Run the Script
   - Open the script in Jupyter Notebook or your preferred IDE.
   - Follow the workflow to load rules, validate parameters, and obtain model recommendations.
### Step 4: Customize if Needed
Modify the script logic to meet your project-specific requirements.

***

## Future Directions

- Incorporate advanced ML/DL models as new algorithms emerge.
- Enhance error messages for more detailed debugging.
- Add scripts for additional data types or hybrid datasets.
