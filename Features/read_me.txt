How to Run the Code

    Prepare Your Environment: Make sure the necessary Python packages are installed, and your data files are correctly placed in the expected directories.
    pip install -r requirements.txt


    Command Line Arguments: The script accepts the following command-line arguments:
        --name:  The name of the line to analyse
        --behav:  The behavior to analyze (string). "hunch_large" "bend_large" or "hunch_weak"


    Example

    To run the script, use the following command structure:

    python3 script_name.py --name your_line_name --behav hunch_large

    Output

    The processed data will be saved in the output/ directory as a pickle file in the following format:
    output/t7/{behav}/Data_t7_{behav}_{Line}.pkl

    Notes
    Ensure that the input .mat files (e.g., trx.mat) are properly located under the specified Line directory. (path_ in the code)

    