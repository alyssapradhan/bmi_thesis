## Evaluation of bias in patient-friendly discharge summaries

#### Introduction
This project was part of my thesis for my NYU Vilcek Master of Biomedical Informatics in which I assessed for the presence of differences in accuracy and reability of patient-friendly discharge summaries between demographic groups.

An interactive, visual abstract can be found here: https://observablehq.com/d/5c25b304405ada4a

#### Process
The key steps for this project included:
1. Developing a workflow for calcuating the reability metrics for the patient-friendly discharge summaries - including Fleisch-Kincaid reading grade and reading level
2. Extract the demographic details for a subset of 50 patients (including race and ethnicity, gender) and then re-generate the discharge summaries with these details changed
3. Create the LLM-as-judge pipeline for assessment of accuracy of the patient-friendly 

#### Materials
The notebooks in this repository do the following components of the above tasks:
* **calculate_readability**: code for calculating the FK grade and level for the original, patient-friendly and perturbed discharge summaries
* **perturb_preprocessing**: code in which the original discharge summaries were perturbed (ie. race, gender changed)  
* **generate_dc**: code to re-generate the patient-friendly discharge summaries from the perturbed ones
* **llm_judge**: development of LLM-as-judge prompts and pipeline for evaluating accuracy of patient-friendly summaries
