# Expert Interactions for Zero Shot Sexism Detection

This repository is contains the code, experiments, and data artifacts created for the paper 

#### "Tell Me What You Know About Sexism: Expert-LLM Interaction Strategies and Co-Created Definitions for Zero-Shot Sexism Detection", published at Findings of NAACL 2025.
[URL to the paper]()

This repository contains experimental software and is published for the sole purpose of giving additional background details on the respective publication. Please cite the respective work when using any of the software, artifacts, or experimental ideas. 

contact person: myrthe[dot]reuver[at]gmail[dotcom]


--------
Our folders contain the software, each part of our pipeline: 

## Part I: Survey
**Software:** 
(1) Qualtrics templates for the survey are stored in the folder "qualtrics". These contain both .qsf files (importable in Qualtrics) and PDF files showing the overall survey flow for reimplementation in other platforms.
(2) A Python notebook used to analyze the data, using the following package versioning:

**Data:** 
An anonymized version of the survey results is called "xxxx.csv".

## Part II: Interactive Experiments
**Software:** 
(1) Qualtrics templates for the interactive experiments with the GPT API are stored in the folder "qualtrics". These contain both .qsf files (importable in Qualtrics) and PDF files showing the overall survey flow for reimplementation in other platforms.
(2) A Python notebook used to analyze this data.

**Data:** 
An anonymized version of the LLM-expert interactions is called "xxxx.csv"

## Part III: Definition Experiments
**Software:** 
(1) Qualtrics templates for the interactive experiments with the GPT API are stored in the folder "qualtrics". These contain both .qsf files (importable in Qualtrics) and PDF files showing the overall survey flow for reimplementation in other platforms.
(2) A Python notebook used to analyze this data.

**Data:** 
An anonymized version of the definition versions, corresponding to the definition Table in the paper's appendix, called "xxxx.pkl"

## Part VI: Modelling
**Software:** 
Requires the definition dictionary from Part III. 

### GPT: 
Running predictions:
Postprocessing of results + evaluation:

### LLaMa:
Running predictions:
Postprocessing of results + evaluation:

**Data:** 

**Results:**
We provide a dictionary of the metrics of the classification results. 
We also present a notebook presenting in its output the modelling results over each dataset, by each expert.
