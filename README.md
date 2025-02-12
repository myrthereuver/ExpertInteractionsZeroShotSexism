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

(1) Qualtrics templates for the survey AND interactive experiments are stored in the folder "qualtrics". 
This is provided both in .qsf file (importable in Qualtrics) and a PDF file showing the overall survey flow for reimplementation in other platforms.

(2) Python notebook xxxx.ipynb used to analyze the data, using the following package versioning:

**Data:** 
An anonymized version of the survey results is called "xxxx.csv".

## Folder PartII_Interactions
**Software:** 

(1) Interactions with LLM: see Qualtrics files in Folder part I
(2) Python notebook xxxx.ipynb used to analyze this data.

**Data:** 
"xxxx.csv" is an anonymized version of the LLM-expert interactions is called 

## Folder Part III_Definitions
**Software:** 

(1) Interactions with LLM: see Qualtrics files in Folder part I

(2) xxxx.ipynb is a Python notebook used to analyze this data.

**Data:** 
xxxx.pkl is anonymized version of the definition versions, corresponding to the definition Table in the paper's appendix

## Folder PartVI_Modelling
**Software:** 
Requires the definition dictionary from Part III. 

Requirements:
[software packages]

#### GPT: 
(1) Python notebook xxxx.ipynb for running predictions

(2) Python notebook xxxx.ipynb for post processing of results + evaluation

#### LLaMa:
(1) Python notebook xxxx.ipynb for running predictions

(2) Python notebook xxxx.ipynb for post processing of results + evaluation

**Results:**

(1) Dictionary xxxx.pkl dictionary of predictions

(2) Dictionary xxxx.pkl of the metrics (F1, accuracy, classification report) of the classification results per dataset and participant

(3) Python notebook xxxx.ipynb presenting in its output the modelling results over each dataset, by each expert
