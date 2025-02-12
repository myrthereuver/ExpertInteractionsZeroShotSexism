# Expert Interactions for Zero Shot Sexism Detection

This repository is contains the code, experiments, and data artifacts created for the paper 

#### "Tell Me What You Know About Sexism: Expert-LLM Interaction Strategies and Co-Created Definitions for Zero-Shot Sexism Detection", published at Findings of NAACL 2025.
[URL to the paper]()

This repository contains experimental software and is published for the sole purpose of giving additional background details on the respective publication. Please cite the respective work when using any of the software, artifacts, or experimental ideas. 

contact person: myrthe[dot]reuver[at]gmail[dotcom]


--------
Our folders represent the different parts of the pipeline, and in each is a software, data, and results subfolder with the following content:

## Folder PartI_Survey
**Software:** 

(1) Qualtrics templates for the survey are stored in the folder "qualtrics". These contain both .qsf files (importable in Qualtrics) and PDF files showing the overall survey flow for reimplementation in other platforms.

(2) A Python notebook used to analyze the data, using the following package versioning:

**Data:** 
An anonymized version of the survey results is called "xxxx.csv".

## Folder PartII_Interactions
**Software:** 
(1) Qualtrics templates for the interactive experiments with the GPT API are stored in the folder "qualtrics". These contain both .qsf files (importable in Qualtrics) and PDF files showing the overall survey flow for reimplementation in other platforms.

(2) A Python notebook used to analyze this data.

**Data:** 
An anonymized version of the LLM-expert interactions is called "xxxx.csv"

## Folder Part III_Definitions
**Software:** 
(1) Qualtrics templates for the interactive experiments with the GPT API are stored in the folder "qualtrics". These contain both .qsf files (importable in Qualtrics) and PDF files showing the overall survey flow for reimplementation in other platforms.

(2) A Python notebook used to analyze this data.

**Data:** 
An anonymized version of the definition versions, corresponding to the definition Table in the paper's appendix: xxxx.pkl

## Folder PartVI_Modelling
**Software:** 
Requires the definition dictionary from Part III. 

#### GPT: 
Running predictions: xxx.ipynb

Postprocessing of results + evaluation: xxx.ipynb

#### LLaMa:
Running predictions: xxx.ipynb

Postprocessing of results + evaluation: xxx.ipynb

**Results:**

A dictionary of predictions: xxx.pkl

A dictionary of the metrics of the classification results: xxxx.pkl

A notebook presenting in its output the modelling results over each dataset, by each expert: 
xxxx.ipynb
