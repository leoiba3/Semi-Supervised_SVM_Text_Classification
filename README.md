# Semi-Supervised SVM Text Classification

## Overview
This project is designed to analyze public service request data from the City of Austin's 311 system using machine learning. The goal is to categorize service requests based on their descriptions. Approximately 150 rows were manually categorized and the model categorized the rest (approx. 2 Million rows). The project includes steps for data preprocessing, feature extraction using TF-IDF vectorization, and classification with a Support Vector Machine (SVM).
## Dependencies
- Python 3.x
- pandas
- numpy
- matplotlib
- scikit-learn
- re (Regular Expression library)

## Installation
To install the required packages, run the following command:
```bash
pip install pandas numpy matplotlib scikit-learn
```
## Dataset

The project uses the following datasets:
- Original dataset: `Austin_311_Public_Data_20231107.csv`
- Sample dataset: `100samples.csv`
- Labeled sample dataset (created after modifications in Excel): `100samples_labeled.csv`

## Dataset Sample

A snippet from the original dataset `Austin_311_Public_Data_20231107.csv`:

| Service Request (SR) Number | SR Description | Method Received      | ...  | Map Tile |
|------------|--------------------------|------------|---------| --- |
| 19-00090956 | Animal - Proper Care    | Phone | ...   | ML25 |
| 20-00135805 | Tree Issue ROW          | Mobile Device | ...  | MJ24 |
| ...        | ...                      | ...        | ...     | ... |


## Project Structure

- Data loading and sampling from `Austin_311_Public_Data_20231107.csv`
- Data preprocessing with a custom `BasicTextPreprocessor`
- Feature extraction using `TfidfVectorizer`
- Model training using a Support Vector Machine (SVM) with a linear kernel
- Model evaluation with classification report
- Prediction on new data and saving the results

## Usage

1. Prepare the original dataset in Excel and label it as `100samples_labeled.csv`.
2. Run the Python script to perform the following steps:
   - Data preprocessing
   - Model training
   - Model evaluation
   - Making predictions on new data
3. The script will output a classification report for the model and save the predicted categories in a new file.

## Output

- A classification report detailing the model's performance.
- The complete dataset with predicted categories, saved as `complete_data.csv`.


| Service Request (SR) Number | SR Description | Method Received      | ...  | Map Tile | Predicted Category |
|------------|--------------------------|------------|---------| --- | --- |
| 19-00090956 | Animal - Proper Care    | Phone | ...   | ML25 | Animal Services |
| 20-00135805 | Tree Issue ROW          | Mobile Device | ...  | MJ24 | Tree Issues ans trimming |
| ...        | ...                      | ...        | ...     | ... | ... |


## Contributing

Contributions to this project are welcome. You can contribute by forking the project, submitting pull requests, or suggesting improvements via issues.
