# Study 3

## Introduction
Study 3 extends Study 2a by investigating GPT-4o's ability to create tailored advertising content based on a blended model of the OCEAN, excluding Neuroticism, consistent with our previous scope. In this study, we compare participants' perceptions of ads tailored to one of their personality traits with those tailored to a blended personality profile, which in this context refers to the mixed scores of BFI-2S for four target traits. Aligning with H5, we focus on the potential effects to perceived personalization. A comprehensive copy of the survey is available in `study3/survey_materials/study3_survey_questions.pdf`.

## Study 3 Analysis
We utilized the `study3/notebooks/00_result_analysis/study_3_result_analysis.ipynb` notebook to analyze the results of Study 3. This notebook performs comprehensive statistical analyses and visualizations of the collected data. The main processing steps include:

1. **Data Preparation**
   - Loading input files:
     * `big5_scores.xlsx`: Contains participants' Big Five personality scores from Study 2
     * `socioecono_scores.xlsx`: Contains participants' socioeconomic details from Study 2
     * `mixed_trait_scores.xlsx`: Contains benchmark blended personality scores from Study 2
     * `study3_response.xlsx`: Contains survey responses for Study 3
   - Merging datasets based on participant IDs
   - Cleaning data: Removing incomplete responses, handling missing values
   - Creating composite scores for perceived personalization and other key variables
   - Calculating distance measures: Single Trait Distance and Blended Average Distance
   - Normalizing scores using z-score standardization

2. **Descriptive Statistics**
   - Calculating means, standard deviations, and distributions for key variables
   - Generating summary tables and visualizations for personality traits, perceived personalization scores, and distance measures
   - Analyzing socioeconomic variables

3. **Hypothesis Testing**
   - H5.1: GPT-4o's Capability in Blended Personality Interpretation and Ad Generation
     * Linear regression analysis of 'Perceived Personalization' scores against 'Personality Description and Ad Preference' scores
   - H5.2: Consumer Preference for Blended Personality-Based Ads
     * Multiple regression analyses using different patterns of independent variables
     * Segmentation analysis based on Single Trait Distance and Blended Average Distance
     * One-sample t-tests and binomial tests to assess preferences within segments

4. **Advanced Statistical Techniques**
   - Implementing bootstrapping (10,000 iterations) for robust confidence interval estimation
   - Conducting interaction analysis in regression models

5. **Visualization**
   - Creating scatter plots with regression lines to illustrate relationships between variables
   - Generating box plots and violin plots to show distributions of key variables
   - Producing heatmaps and section plots to visualize segmentation analysis results

This notebook provides a comprehensive analysis of Study 3 results, offering insights into the effectiveness of GPT-4o in generating personality-tailored content for advertising. The analyses directly address the research questions and hypotheses related to blended personality-based personalization in AI-generated content.

This notebook contains the original code for `Figure 4.16`, `Figure 4.17`, `Table 4.9`, `Figure 4.18`, `Figure 4.19`, `Table 4.10`, `Figure 4.20`, and `Table 4.11`.