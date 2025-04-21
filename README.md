# Expert Interactions for Zero Shot Sexism Detection

This repository is contains the code, experiments, and data artifacts created for the paper 

#### "Tell Me What You Know About Sexism: Expert-LLM Interaction Strategies and Co-Created Definitions for Zero-Shot Sexism Detection", published at Findings of NAACL 2025.
[URL to the paper]()

This repository contains experimental software and is published for the sole purpose of giving additional background details on the respective publication. Please cite the respective work when using any of the software, artifacts, or experimental ideas. 

contact person: myrthe[dot]reuver[at]gmail[dotcom]

![Figure 1 of the paper, displaying the pipeline](https://github.com/myrthereuver/ExpertInteractionsZeroShotSexism/blob/main/Fig1_ModelSexism.png?raw=true)

--------

## Folder PartI_Survey
See below for the artifacts in the specific subfolders. 

**Qualtrics**

Qualtrics templates for the survey AND interactive experiments are stored in the folder `qualtrics`. These are provided both in .qsf file (importable in Qualtrics) and a PDF file showing the overall survey and experimental flow for reimplementation in other platforms. 

Implementation details: The OpenAI API is called in an embedded Web Service block, the arguments to it are given in JSON format and by reading user input and earlier in/output pairs, after which the loop is obtained by having different Web Service blocks connect to the user is an if/then fashion: if the user indicates not wanting to continue prompting, the user is not refer to a new block.

**Data** 

An anonymized version of the survey results is provided in `Data/Questionnaire_ds.csv`.

**Code**

Python notebook `Show_heatmaps.ipynb` used to analyze and visualize the Likert scale results.

## Folder PartII_Interactions
See below for the artifacts in the specific subfolders.

For the implementation of the interactions with LLM: see Qualtrics files in Folder Part I. 

**Data:** 

`Knowledge_interaction_ds.csv` is an anonymized csv file with the LLM-expert knowledge interactions.

**Code:** 

Python notebook `xxxx.ipynb` used to analyze the interaction data.


## Folder Part III_Definitions

For Qualtrics implementation of the interactions with LLM: see Qualtrics files in Folder Part I. 

**Data:** 
`dict_of_defs.pkl` is anonymized version of the definition versions, corresponding to the definition Table in the paper's appendix.
`Definitions_Interaction_ds.csv` contains anonymized data on the definition interactions. 

**Code:**

`xxxx.ipynb` is a Python notebook used to analyze this data.


## Folder PartVI_Modelling
**Code:** 

Input: Requires `dict_of_defs.pkl` (dictionary of definitions) that is the output from Part III, and the sexism detection benchmark datasets outlined below. 

EXTERNAL DATASETS:

'Call me sexist but' Dataset (CMSB): https://search.gesis.org/research_data/SDN-10.7802-2251

EXIST: https://github.com/fhstp/EXIST2022/tree/main/data/EXIST2022_orig

GUEST ET. AL.: https://github.com/ellamguest/online-misogyny-eacl2021/tree/main/data

EDOS: https://github.com/rewire-online/edos

Hatecheck (HC): https://github.com/paul-rottger/hatecheck-data


#### GPT: 
Code for GPT zero shot classification is in the notebook `ZeroShot_Classification_with_Definitions.ipynb`
This folder also contains a `requirements.txt` with requirements, but the most important versioning is `openai==1.51.2`

Python notebook `xxxx.ipynb` for post processing of results + evaluation

#### LLaMa:
Python notebook `xxxx.ipynb` for running predictions

Python notebook `xxxx.ipynb` for post processing of results + evaluation

**Results:**

Dictionary `xxxx.pkl` of predictions of 
GPT and Dictionary `xxxx.pkl` of predictions of LLaMa

Dictionary `xxxx.pkl` for LLaMa and Dictionary `xxxx.pkl`  of the metrics (F1, accuracy, classification report) of the classification results per dataset and participant.

Python notebook `xxxx.ipynb` presenting in its output the modelling results over each dataset, by each expert.
