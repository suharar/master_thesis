# Study 1

## Introduction
Study 1 investigates the capability of large language models (LLMs) to accurately identify personality traits from written texts extracted from an online social forum. We employed three LLMs to perform classification tasks, aiming to determine the appropriate Myers-Briggs Type Indicator (MBTI) type for the authors of each text set. The models' performance was evaluated using accuracy, recall, precision, and F1 score, and compared against state-of-the-art (SOTA) models and among the selected LLMs. This study addresses hypotheses H1 and H2.

## Procedure
### 1. Data Preparation and Model Predictions
#### 1.1. Dataset Import and Transformation
We utilized the public MBTI dataset from [Kaggle](https://www.kaggle.com/datasets/datasnaek/mbti-type). Two separate Kaggle notebooks were created to transform the original dataset according to our Resampling Strategies 1 and 2:
- [Notebook for Resampling Strategy 1](https://www.kaggle.com/code/rsuhara/reflecting-dist-mbti-data-filtering-for-gpt3-5)
- [Notebook for Resampling Strategy 2](https://www.kaggle.com/code/rsuhara/mbti-data-filtering-for-gpt3-5)

These notebooks contain the original code for `Table 3.1` and `Figure 3.1`.

The output `sample.xlsx` files were downloaded from each notebook. We then created a new 'text_only' sheet, removing the true MBTI label column. These modified files, `sample_forFeeding.xlsx` (Resampling Strategy 1) and `sample_forFeeding_exactDist.xlsx` (Resampling Strategy 2), were saved in the `study1/raw` directory for use with the LLMs.

#### 1.2. MBTI Predictions Using LLMs
We used the `study1/notebooks/01_MBTI_predictions/LLMs_mbti_predictions.ipynb` notebook to prompt GPT-3.5, GPT-4o, and Claude 3.5 Sonnet for MBTI label classification tasks using both prepared datasets.

##### Configuration Settings
The `LLMs_mbti_predictions.ipynb` notebook requires the following variable settings:
1. `llm_type`: Select the language model ("gpt4o", "gpt35", or "claude")
2. `sampling_type`: Choose the sampling method ("normal" or "exact_dist")
3. `mode`: Set the execution scope ("pilot" for first 10 rows, "full" for entire dataset)

Results are saved in the `study1/raw/` folder as `{llm_type}_result_raw{'_exactDist' if sampling_type == 'exact_dist' else ''}.xlsx`

#### 1.3. Result File Finalization
The raw output files require manual formatting. Open each generated Excel file and copy the relevant columns into new files named `result_{llm_type}` or `result_{llm_type}_exactDist`, depending on the resampling strategy. Use `result_GPT4o` as a reference for the correct format.

#### 1.4. Pre-processing
The `study1/notebooks/00_pre-processing/pre_processing.ipynb` notebook is used to finalize the `result_{llm_type}` and `result_{llm_type}_exactDist` files. This process includes adding new columns with boolean values for each of the 4 MBTI dimensions, facilitating performance calculations in later steps.

##### Pre-processing Configuration
To run `pre_processing.ipynb`, set the following variables:
1. `version`: Choose the sampling strategy
     - Options: "original" or "exactDist"
2. `run_flag`: Dictionary of models to run (True) or skip (False)


### 2. Assessing Prediction Performance

#### 2.1. Overall Assessment Results
We utilized the `study1/notebooks/02_analysis/00_overall_performance_review/performance_assessment.ipynb` notebook to evaluate the performance of each target model. This analysis included:
- Calculating accuracy for individual MBTI types
- Determining overall accuracy
- Computing recall, precision, and F1 scores

This notebook contains the original code for `Table 4.1`, `Table 4.2`, `Figure 4.2`, and `Table 4.3`.

##### Configuration Settings
To run `performance_assessment.ipynb`, configure the following variables:
1. `version`: Specify the sampling strategy
   - Options: "original" or "exactDist"
2. `run_flag`: Set a dictionary of models to include (True) or exclude (False) from the analysis

#### 2.2. In-depth Analysis of S-N and J-P Dimensions
We utilized the `study1/notebooks/02_analysis/00_overall_performance_review/justification_analysis.ipynb` notebook for an in-depth analysis of the S-N and J-P dimensions. This analysis included:
- Extracting and preprocessing justifications for the S-N and J-P dimensions from model outputs
- Calculating frequencies of specific keywords and phrases associated with each dimension
- Visualizing keyword frequency distributions using bar plots and heatmaps
- Comparing keyword usage across different models (GPT-4, GPT-3.5, and Claude)
- Analyzing correlations between keyword usage and correct predictions
- Examining common phrases and patterns in the justifications
- Identifying potential biases or tendencies in the models' reasoning processes
- Evaluating consistency of justifications across different personality types
- Assessing quality and depth of justifications provided by each model
- Exploring relationships between justification length and prediction accuracy

This notebook contains the original code for `Figure 4.3`, `Figure 4.4`, `Figure 4.5`, `Figure 4.6`, `Figure 4.7`, `Figure 4.8`, `Figure 4.9`, and `Figure 7.3`.