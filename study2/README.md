# Study 2

## Introduction
Study 2 explores GPT-4o's capability to generate tailored text advertising content and dynamically adjust communication tones of a chatbot agent on online shopping platforms, customized to each of the Big Five personality traits (OCEAN) except neuroticism. The study consists of two components: tailored advertising texts (Study 2a), assessing H3, H4, and H5, and chatbot interactions as an automated service agent (Study 2b), assessing H6.   A comprehensive copy of the survey is available in `study2/survey_materials/study2_survey_questions.pdf`.

## Study 2 Analysis
We utilized the `study2/notebooks/00_result_analysis/study_2_result_analysis.ipynb` notebook to analyze the results of Study 2 including both Study 2a and 2b.  This notebook performs comprehensive statistical analyses and visualizations of the collected data. The main processing steps include:

1. **Data Preparation**
   - Loading input files:
     * `study2a_data.xlsx`: Contains survey responses for the tailored advertising text experiment
     * `study2b_data.xlsx`: Contains survey responses for the chatbot interaction experiment
     * `big5_scores.xlsx`: Contains Big Five personality scores for participants
   - Merging datasets based on participant IDs
   - Cleaning data: Removing incomplete responses, handling missing values
   - Creating composite scores for perceived personalization, overall attitudes, and engagement
   - For Study 2a (Text Ads):
     * Calculating 'Overall Attitude towards the Ad' by averaging child constructs: favorability, persuasiveness, and increased interest in the product
   - For Study 2b (Chatbot Responses):
     * Calculating 'Overall Attitude towards the AI Agent' by averaging responses for trust, satisfaction, and positive emotions
     * Computing 'Trust' as the average of reliability and supportiveness
     * Calculating 'Engagement' as the average of interaction duration and likelihood of future use

2. **Descriptive Statistics**
   - Calculating means, standard deviations, and correlations for all variables
   - Generating summary tables for key variables (e.g., personality traits, perceived personalization)
   - Analyzing socioeconomic variables:
     * Calculating mean age and standard deviation
     * Computing gender distribution
     * Analyzing education levels, race/ethnicity, and employment status
     * Consolidating categories with small counts into an "Other" category for more effective regression analysis
   - Preparing data for Table 7.1, summarizing participant demographics

3. **Regression Analyses**
   - For Study 2a (Advertising Texts):
     * Model 1: Regression of personality traits on perceived personalization (and on perceived credibility, overall attitude towards the ad, and engagement)
     * Model 2: Regression of perceived personalization on perceived credibility
     * Model 3: Regression of perceived personalization and perceived credibility on overall attitude towards the ad
     * Model 4: Regression of overall attitude towards the ad on engagement
   - For Study 2b (Chatbot Interactions):
     * Model 5: Regression of personality traits on perceived personalization (and on overall attitude towards the AI agent and engagement)
     * Model 6: Regression of perceived personalization on overall attitude towards the AI agent
     * Model 7: Regression of perceived personalization on engagement
   - Quadratic regression to test for potential negative effects of over-personalization (H4)

4. **Advanced Statistical Techniques**
   - Implementing Ridge regression to handle potential multicollinearity among personality traits
   - Conducting bootstrapping (1000 iterations) for robust confidence interval estimation

5. **Visualization**
   - Creating scatter plots with regression lines to illustrate relationships between variables
   - Generating heatmaps to visualize correlation matrices of personality traits and outcome variables
   - Producing bar plots comparing means of perceived personalization across different personality types

6. **Model Diagnostics**
   - Checking assumptions of linear regression: normality (Q-Q plots), homoscedasticity (residual plots)
   - Analyzing residuals and identifying potential outliers using Cook's distance

This notebook provides a comprehensive analysis of Study 2 results, offering insights into the relationship between personality traits, perceived personalization, and user engagement with AI-generated content.  This notebook contains the original code for `Table 4.5`, `Figure 4.10`, `Figure 4.11`, `Table 4.6`, `Table 4.7`, `Figure 4.12`, `Figure 4.13`, `Table 4.8`, `Figure 4.14`, `Figure 4.15`, `Table 7.1`, `Figure 7.6`, and `Figure 7.7`.  


## Study 3 Data Preparation

We utilized two notebooks to generate the datasets for Study 3:
1. `study2/notebooks/00_result_analysis/study_2_result_analysis.ipynb`
2. `study2/notebooks/01_prep_for_Study3/study_2_big5_preparing_for_study3.ipynb`

### `study_2_result_analysis.ipynb`

This notebook produces two essential files used in Study 3 to extract relevant data for the 90 participants who continued to Study 3:
1. `big5_scores.xlsx`: Contains participant IDs and their corresponding Big Five personality scores.
2. `socioecono_scores.xlsx`: Contains participant IDs and their associated socioeconomic details.

### `study_2_big5_preparing_for_study3.ipynb`

This notebook generates a crucial file for establishing benchmark personality profiles in Study 3:
- `mixed_trait_scores.xlsx`: Contains benchmark blended personality scores derived from the 104 participants in Study 2. These scores serve as reference points for each personality trait in Study 3.

This notebook contains the original code for `Figure 3.7`