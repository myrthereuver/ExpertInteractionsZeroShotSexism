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

For the implementation of the interactions with LLM: see Qualtrics files in the folder of part I. 

**Data:** 

`Knowledge_interaction_ds.csv` is an anonymized csv file with the LLM-expert knowledge interactions.

**Code:** 

Python notebook `xxxx.ipynb` used to analyze this interaction data.


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


#### Zero Shot Classification and Data Processing

###### GPT
Code for GPT zero shot classification is in the notebook `ZeroShot_Classification_with_Definitions.ipynb`
This folder also contains a `requirements.txt` with requirements, but the most important versioning is `openai==1.51.2`

Python notebook `Raw_to_metrics.ipynb` for post processing of results + getting to evaluation metrics. 

Python notebook `GPT_Plots.ipynb` for plotting the results: requires as input the cleaned dataframes with metrics (F1 etc) as stored under `PartVI_Modelling/Results`.

###### LLaMa

Python notebook `LLaMa_ZeroShot_with_Definitions.ipynb` for running predictions.

Python notebook `Plot_llama.ipynb` for post processing + evaluation + plotting results

**Results:**

Raw results: Dictionaries `results_GPT.pkl` and `results_GPT07.pkl` of predictions of 
GPT's first and second run, and dictionary `results_llama.pkl` of predictions of LLaMa. 
NOTE: These have three "results" columns, one for each of the three definition types: "results" is for the participant definition, "results_GPT10" for the co-created definition, and "Results_GPT1" for the GPT definition. 

Performance dataframes (with F1, accuracy, etc. per participant for each definition and each dataset): Dictionary  `metrics_df_llama.pkl` for LLaMa and `metrics_df_gpt07.pkl` and `metrics_df_gpt_cleaned_data.pkl` for GPT runs.

The raw results can be used to obtain the performance dataframes with the notebook `Code/Raw_to_metrics.ipynb`.

The performance dataframes are the input for the plotting script `Code/GPT_Plots.ipynb`.


