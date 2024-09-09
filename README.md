# Large Language Models in Marketing: A Dual-Phase Assessment of Personality Detection and Content Personalization

## Abstract
This study critically examines the potential and limitations of large language models (LLMs), such as GPT-4o and Claude 3.5 Sonnet, in the realm of psychological targeting and personalized marketing. We evaluate these models across two key phases: the processing phase, which involves constructing customer profiles through text-based personality detection, and the personalization phase, where targeted advertisements and chatbot responses are generated. Our findings indicate that LLMs outperform traditional state-of-the-art (SOTA) models in detecting Myers-Briggs Type Indicator (MBTI) personality traits, particularly under zero-shot learning (ZSL) conditions where fine-tuning is impractical. However, notable biases are observed, especially in predicting Sensing-Intuition and Judging-Perceiving dimensions, reflecting the limitations of text-based analysis in fully capturing human personality nuances. In the personalization phase, LLMs show effectiveness in single-trait ad targeting, enhancing perceived personalization and engagement for traits like Extraversion. However, their ability to generate content for blended personality profiles is limited, often reducing effectiveness compared to single-trait approaches. Similarly, in chatbot interactions, personalized responses tailored to different personality traits did not significantly enhance perceived personalization, underscoring the challenges in achieving nuanced and authentic consumer engagement through AI. These findings highlight the transformative potential of LLMs in personalized marketing, while also pointing to critical gaps that require further refinement. Future research should focus on integrating behavioral and multi-modal data, optimizing multi-trait targeting and chatbot strategies, and ensuring ethical AI implementation in marketing practices. 

## Purpose of this repository
This repository contains all the materials and code developed for this master’s thesis. It is provided to ensure transparency and reproducibility of the study.

## Details for each study
- [Study1](study1/README.md)
- [Study2](study2/README.md)
- [Study3](study3/README.md)

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
│   │   ├── result_GPT4o.xlsx
│   │   ├── result_GPT4o_exactDist.xlsx
│   │   ├── sample_forFeeding.xlsx
│   │   ├── sample_forFeeding_exactDist.xlsx
│   │   ├── sample_forFeeding_exactDist_for_claude_2nd_half.xlsx
│   │   ├── sample_forFeeding_exactDist_for_claude_3rd_half.xlsx
│   │   ├── sample_forFeeding_for_claude_2nd_half.xlsx
│   │   ├── sample_forFeeding_pilot.xlsx
│   │   └── ...
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
│   │   └── ...
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
│   ├── presentation_materials/
│   │   └── ...
│   ├── raw/
│   │   ├── 20240721_prolific_export.csv
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

