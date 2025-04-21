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
These are provided both in .qsf file (importable in Qualtrics) and a PDF file showing the overall survey and experimental flow for reimplementation in other platforms. 

Implementation details: The OpenAI API is called in an embedded Web Service block, the arguments to it are given in JSON format and by reading user input and earlier in/output pairs, after which the loop is obtained by having different Web Service blocks connect to the user is an if/then fashion: if the user indicates not wanting to continue prompting, the user is not refer to a new block.

(2) Python notebook xxxx.ipynb used to analyze the data.

Implementation details: using the package versioning in 

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
xxxx.pkl is anonymized version of the definition versions, corresponding to the definition Table in the paper's appendix.


## Folder PartVI_Modelling
**Software:** 
Requires the definition dictionary from Part III. 

LINKS TO EXTERNAL DATASETS

ID https://search.gesis.org/research_data/SDN-10.7802-2251

OOD1 https://github.com/fhstp/EXIST2022/tree/main/data/EXIST2022_orig

OOD2 https://github.com/ellamguest/online-misogyny-eacl2021/tree/main/data

OOD3 https://github.com/rewire-online/edos

Hatecheck (HC) https://github.com/paul-rottger/hatecheck-data


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
