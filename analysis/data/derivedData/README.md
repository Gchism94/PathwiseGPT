This repository contains JSON files that define rules and configurations for selecting appropriate machine learning and deep learning models based on data types, tasks, and specific conditions. These files serve as a framework for practitioners to streamline model selection and decision-making processes in various AI applications.

# Overview
The files in this repository are categorized by data type and contain rules that map specific tasks to recommended models or algorithms. Each rule considers factors such as dataset size, interpretability, real-time requirements, and computational complexity to help users select the most suitable approach for their use case.

# Files and Structure
The repository is organized as follows:

## Rules Files:

Each JSON file corresponds to a specific data type (e.g., time series, textual, tabular, etc.).
Defines tasks and conditions relevant to the data type and recommends appropriate models or algorithms.
## Configuration File:

config.json provides customizable parameters, such as dataset size thresholds, that influence model selection.
## File Descriptions
Rules Files: Contain task-specific rules and recommendations for model selection based on different conditions. These files support a wide range of data types, including:

- Audio
- Categorical
- Image
- Numerical
- Tabular
- Textual
- Time Series

Configuration File: The config.json file defines general parameters, such as thresholds for small and large datasets, which can be adjusted to meet the specific needs of your project.
# Key Features
- Task-specific Guidance: Provides tailored recommendations for various ML and DL tasks, ensuring that the models align with specific requirements.
- Flexible and Extensible: Rules and thresholds can be modified or expanded to accommodate new tasks, algorithms, or conditions.
- Unified Framework: Standardizes model selection across different data types, reducing the complexity of choosing the right approach.
# Usage Instructions
- Select the Relevant File: Identify the JSON file that matches your data type (e.g., for tabular data, use rules_tabular.json).
- Identify Your Task: Determine the task you are working on, such as classification, regression, clustering, etc.
- Evaluate Conditions: Review the conditions (e.g., dataset size, real-time requirements) applicable to your task.
- Follow Recommendations: Use the suggested models or algorithms that best suit your task and conditions.
- Customize if Necessary: Modify the rules or thresholds in the JSON files or config.json as needed for your specific use case.
# Customization
The repository is designed to be adaptable to different projects:

- Adding New Rules: Extend the existing JSON files to include additional tasks or conditions.
- Adjusting Thresholds: Update the dataset size thresholds in config.json to reflect your project's requirements.
- Task-specific Modifications: Modify the rules to account for emerging algorithms or specialized needs.