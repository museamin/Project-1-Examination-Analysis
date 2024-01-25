# Project-1-Examination-Analysis
# An analysis of GCSE examination results in England  

![Students celebrating examination results](https://i2-prod.dailyrecord.co.uk/incoming/article27697944.ece/ALTERNATES/s810/1_Park-Mains-High-school-pupils-in-Erskine-celebrate-their-success-in-this-years-exam-results-Photo.jpg)
  
This was a group project by six [contributors](#Contributors). The purpose was to to analyse UK government data on GCSE examinations in England to see whether there were any trends based on various characteristcs.
  
# Contents
- [Dataset](#Dataset)
- [Project Outline](#Project-Outline)
- [Presentation](#Presentation)
- [Dependencies](#Dependencies)
- [How to Run the Code](#How-to-Run-the-Code)
- [Jupyter Files Guide](#Jupyter-Files-Guide)
- [Processed Data Files](#Processed-Data-Files)
- [Graphs](#Graphs)
- [Repository Structure](#Repository-Structure)
- [Contributors](Contributors)
  
## Dataset
  
We used the GCSE examination results from (https://www.gov.uk/government/collections/statistics-gcses-key-stage-4)  
The downloaded CSV files are in the folder [Data_original](Data_original) along with a folder ([data-guidance](Data_original/data-guidance)) which contains a file ([data-guidance.txt](Data_original/data-guidance/data-guidance.txt)).  
data-guidance.txt explains the variables in the CSV files.
  
## Project Outline
  
The aim of the project was to discover whether GCSE examination results had any inherent dependencies on factors such as gender,   
ethnicity etc.  
  
Six questions were formulated to discover whether such dependencies existed. The questions are as follows:  
  
Q1. Does gender, ethnicity and social class affect GCSE outcomes and which has the biggest influence?  
Q2. Is there a gender difference in the subjects that students take for their GCSEs?  
Q3. Does the type of school attended affect GCSE outcomes?  
Q4. Does geographical location affect students GCSE outcomes?  
Q5. Was there a difference in GCSE outcomes between state and independent schools during COVID?  
Q6. Are some subjects easier to get a Grade 9 in than others?  
    
The key to this analysis is understanding the educational measures of comparison i.e understanding what is meant by attainment8 and progress8. An explanation of these can be found [here](https://blog.teamsatchel.com/hubfs/attainment-8-progress-8/understanding-progress-8-and-attainment-8-guide-updated.pdf?_hsenc=p2ANqtz--mMC7EY3_ViZu0TCTPKC__Rl8OVLuyLcMRsrv2VUM3QvoVA1eKjrIhnl_gjPAvLt4LQplTBzfUXm3IfiW_9pZZs2FBkw&_hsmi=73553619&hsCtaTracking=ee55283f-6588-4711-8425-3f54f663067c%7Cd685e0f9-2208-40fd-afda-adfdebc83226#:~:text=Progress%208%20has%20been%20introduced,of%20Attainment%208%20is%20necessary.). They are also explained in the presentation powerpoint [here](Project%201%20Presentation.pptx) and pdf [here](Project%201%20Presentation.pdf).
  
## Presentation
    
There are two files in which the findings have been shown:
- [Project 1 Presentation.pptx](Project%201%20Presentation.pptx)
- Project 1 Presentation.pdf
  
## Dependencies

In order to run the files you will need to install the following packages:    
- pandas:                pip install pandas  
- seaborn:               pip install seaborn  
- matlibplot:            pip install matlibplot  
- scipy:                 pip install scipy  
- jupyter notbook:       pip install notebook  
- gmaps:                 pip install gmaps  
  
A gmaps api key will also be required.   

## How to Run the Code
  
1. Clone the repository  
2. Run the Jupyter notebook file Data_extraction_from_gov_files.ipynb to extract all the data to be used from the Department of Education files in the folder Data_original. The extracted csv files will be placed in the folder Data_processed.
3. Run the Jupyter notebook files label Q*.ipynb where * is the number and name of the question being looked at. The Jupyter files are described in more detail in the Jupyter Files Guide section.
4. To view png files of the graphs produced look in the folder [Graphs](Graphs/).
  
## Jupyter Files Guide
  
- Data_extraction_from_gov_files.ipynb  -  Extracts data from the Department for Education CSV files (in [Data_original](Data_original)) and places the extracted data in the folder [Data_processed](Data_processed).
- Q1_visualisation_using_seaborn.ipynb  -  Uses the saved data on gender, ethnicity and free school meals (FSM) to produce seaborn bar plots and regression plots which look at the effect of these factors on GCSE outcomes. The graphs produced are saved into the folder [Graphs](Graphs/).
- Q1_statistical_analysis - Uses the gender, ethnicity and FSM data to do a statistical analysis using Anova and Tukey methods. Also produces box plots of the data.  
- Q4_regional_analysis - Uses local authority data provided by the DofE to see if there is a geographical variation in GCSE outcomes. This is then compared to government data on employment and parental qualifications to see if there is a correlation.

## Processed Data Files
  
- cleaned_ethnicity_data.csv - Data on ethnicity, gender and FSM for GCSE outcomes since 2019. 
- cleaned_grade9_data.csv - Data on how many pupils gain a grade 9 per subject
- cleaned_regional_data.csv - GCSE outcomes data by local authority region
- cleaned_school_data.csv - Data on GCSE outcomes at different types of schools
- cleaned_subject_data.csv - Data on how many students chose various subject combinations at GCSE for 2023
- cleaned_subject_data_all_years.csv - Data on how many students chose to do each GCSE subject over the last 14 years  
- cleaned_time_data.csv - GCSE outcomes data for state and independent school since 2019
- employment_data_for_local_authorities.csv - Data on people who have never worked by region for 2021
- qualifications_data_for_local_authorities.csv - Data on people with no qualifications by region for 2021

## Graphs
  
These are in the folder [Graphs](Graphs/)

They are the graphs produced by the Jupyter notebook files described in the section Jupyter Files Guide.
The first two characters i.e. Q1 show which question/ file the graphs are associated with.

## Repository Structure

- Notebook code files in the root directory
- Presentation powerpoint and pdf in the root directory
- Original data CSV files from gov.uk in [Data_original](Data_original)
- Processed data CSV files in [Data_processed](Data_processed)
- Graphs that were produced by the notebook files in [Graphs](Graphs/)
- 

## Contributors
- Mohammed Nawaz - Researched Q1
- Elcin Imanci - Researched Q2
- Kashfi Khalid - Reasearched Q3
- Yuk Hang Hui - Researched Q4
- Adel Mahmud - Reasearched Q5
- Muse Amin - Researched Q6

