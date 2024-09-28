Larvae Behavior Analysis & Classifier Prediction

This project analyzes larvae behavior and classifies it using pre-trained models. It consists of two main scripts: one for behavior analysis and another for prediction based on pre-extracted features.
1. Larvae Behavior Analysis

Install the required Python packages:


pip install -r requirements.txt


Run the analysis with the following command:


python3 main_df.py --name <line_name> --behav <behavior>

    --name: The name of the line to analyze.
    --behav: Behavior to analyze, e.g., "hunch_large", "bend_large", "hunch_weak".

Output

Results are saved as .pkl files in output/t7/{behav}/Data_t7_{behav}_{Line}.pkl.
Notes

Ensure the .mat files are placed in the appropriate directories (path_ in the code).


2. Classifier Prediction

python3 Code_prediction.py --name <line_name> 


This script uses pre-trained models (CLF_HCSO, CLF_CHT) to classify larvae behavior based on extracted features.
Functions

    used_classifier(CLF_HCSO, CLF_CHT, DF): Predicts labels and probabilities for the given DataFrame.
    load_and_concat_files(path_pattern): Loads and concatenates .pkl feature files.

Workflow

    Load pre-trained models from Random_forest_22_11.pkl.
    Load and concatenate feature data.
    Run predictions using used_classifier().
    Save results as DF_prediction.csv.

Notes

Ensure that feature files and pre-trained models are in place before running the script.
