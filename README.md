# Large Language Models in Marketing: A Dual-Phase Assessment of Personality Detection and Content Personalization

## Abstract
This study provides an in-depth analysis of the capabilities and limitations of large language models (LLMs), such as GPT-4o and Claude 3.5 Sonnet, in psychological targeting and personalized marketing. We assess these models across two critical phases: the processing phase, which focuses on customer profile construction through text-based personality detection, and the content personalization phase, where targeted advertisements and chatbot responses are generated. Our results demonstrate that LLMs outperform traditional state-of-the-art (SOTA) models in detecting Myers-Briggs Type Indicator (MBTI) personality traits, especially under zero-shot learning conditions, although they exhibit significant biases in predicting dimensions like Sensing and Judging due to inherent linguistic and behavioral complexities. In the personalization phase, LLMs effectively enhance user engagement and perceived personalization in single-trait ad targeting for traits like Extraversion and Agreeableness from the Big Five Personality traits (OCEAN). However, the models show notable limitations in handling blended personality profiles, often resulting in a reduced effectiveness compared to single-trait approaches. This highlights a critical gap in their ability to integrate multiple personality dimensions into a cohesive marketing strategy. The findings underscore the transformative potential of LLMs in advancing personalized marketing, while also pointing to the need for further refinement to overcome current challenges and ethical concerns associated with AI-driven personalization. Future research should focus on incorporating behavioral data, optimizing multi-trait targeting strategies, and ensuring transparent, ethical implementations in marketing practices. 

## Purpose of this repository
This repository contains all the materials and code developed for this master’s thesis. It is provided to ensure transparency and reproducibility of the study.

## Folder structure
```
master_thesis/
├── .gitignore
├── README.md
├── common_presentation_materials/
│   └── ...
├── study1/
│   ├── README.md
│   ├── notebooks/
│   │   ├── 00_pre-processing/
│   │   │   └── pre_processing.ipynb
│   │   ├── 01_MBTI_predictions/
│   │   │   ├── claude_mbti_generation.ipynb
│   │   │   └── gpt_mbti_generation.ipynb
│   │   └── 02_analysis/
│   │       ├── 00_overall_performance_review/
│   │       │   └── performance_assessment.ipynb
│   │       └── 01_justification_analysis/
│   │           ├── justification_analysis.html
│   │           └── justification_analysis.ipynb
│   ├── presentation_materials/
│   │   └── ...
│   ├── raw/
│   │   ├── claude_result_raw.xlsx
│   │   ├── claude_result_raw_exactDist.xlsx
│   │   ├── gpt35_result_raw.xlsx
│   │   ├── gpt35_result_raw_exactDist.xlsx
│   │   ├── gpt4o_result_raw.xlsx
│   │   ├── gpt4o_result_raw_exactDist.xlsx
│   │   ├── result_Claude.xlsx
│   │   ├── result_claude_exactDist.xlsx
│   │   ├── result_GPT35.xlsx
│   │   ├── result_GPT35_exactDist.xlsx
│   │   ├── result_GPT4.xlsx
│   │   ├── result_GPT4o.xlsx
│   │   ├── result_GPT4o_exactDist.xlsx
│   │   ├── sample (2).xlsx
│   │   ├── sample.xlsx
│   │   ├── sample1.png
│   │   ├── sample2.png
│   │   ├── sample3.png
│   │   ├── sample_forFeeding.xlsx
│   │   ├── sample_forFeeding_exactDist.xlsx
│   │   ├── sample_forFeeding_exactDist_for_claude_2nd_half.xlsx
│   │   ├── sample_forFeeding_exactDist_for_claude_3rd_half.xlsx
│   │   ├── sample_forFeeding_for_claude_2nd_half.xlsx
│   │   └── sample_forFeeding_pilot.xlsx
│   └── transformed/
│       ├── claude_result_accuracy.xlsx
│       ├── claude_result_accuracy_exactDist.xlsx
│       ├── claude_result_justification.xlsx
│       ├── claude_result_justification_exactDist.xlsx
│       ├── gpt35_result_accuracy.xlsx
│       ├── gpt35_result_accuracy_exactDist.xlsx
│       ├── gpt35_result_justification.xlsx
│       ├── gpt35_result_justification_exactDist.xlsx
│       ├── gpt4o_result_accuracy.xlsx
│       ├── gpt4o_result_accuracy_exactDist.xlsx
│       ├── gpt4o_result_justification.xlsx
│       └── gpt4o_result_justification_exactDist.xlsx
├── study2/
│   ├── README.md
│   ├── notebooks/
│   │   ├── 00_result_analysis/
│   │   │   └── study_2_result_analysis.ipynb
│   │   └── 01_prep_for_Study3/
│   │       └── study_2_big5_preparing_for_study3.ipynb
│   ├── presentation_materials/
│   │   └── ...
│   ├── tmp/
│   │   ├── study2a_1_results.csv
│   │   ├── study2a_2_results.csv
│   │   ├── study2a_2_results_linear.csv
│   │   ├── study2a_2_results_quadratic.csv
│   │   ├── study2a_3_credibility_results.csv
│   │   ├── study2a_3_personalization_results.csv
│   │   ├── study2a_3_personalization_results_quadratic.csv
│   │   ├── study2a_4_results.csv
│   │   ├── study2b_2_results.csv
│   │   └── study2b_3_results.csv
│   ├── raw/
│   │   ├── Study2_June_14_2024_17.29.csv
│   │   └── Study2_June_14_2024_17.29_final.xlsx
│   └── survey_materials/
│       ├── study2_survey_questions.pdf
│       └── ...
├── study3/
│   ├── README.md
│   ├── notebooks/
│   │   └── 00_result_analysis/
│   │       └── study_3_result_analysis.ipynb
│   ├── presentation_for_paper/
│   │   └── ...
│   ├── raw/
│   │   ├── big5_scores.csv
│   │   ├── mixed_trait_scores.csv
│   │   ├── socioecono_scores.csv
│   │   ├── Study3 - final_July 18, 2024_02.35.csv
│   │   └── Study3 - final_July_18_2024_02_35_final.xlsx
│   └── survey_materials/
│       ├── study3_survey_questions.pdf
│       └── ...
└── thesis_latex/
    └── Thesis title (1).zip
```

## Details for each study
- [Study1](study1/README.md)
- [Study2](study2/README.md)
- [Study3](study3/README.md)







