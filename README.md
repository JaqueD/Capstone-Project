# Capstone-Project
CIND820 Capstone Project - A Study of Significant Volcanic Eruptions

In this repository  is included the following files and respective names:
- Abstract, 'Project Abstract - Jaqueline Oliveira Dias'
- Literature Review, 'A Study of Significant Volcanic Eruptions by Jaqueline Dias'
- Two initial datasets, 'volcano.csv' and 'eruptions.csv'
- Initial Results in HTML and Jupyter Notebook formats, 'Volcano Eruptions - Capstone Project Initial Results' and 'Volcano Eruptions - Capstone Project Initial Results.ipynb'
- Merged dataset imported as Excel file, 'volcanoeruptions (1).xlsx'

At the Initial Results I have analyzed both datasets used in this project and merged them. Next, I delete duplicates and rename remainig features. Given the long period of the dataframe I filter entries from 1020 to the newest records from 2020, another filter is added in this phase to make sure all the eruptions being analyzed have been confirmed.
At this point I know my dataset has some na's that I'll treat further on. I analyze the correlation between the variables and then I continue cleaning the data. I export the dataset to Excel where all records with missing VEI are treated as follows:
- for VEI missing, I will be using the last eruption VEI record per volcano to replace it;
- when last record is not available I will use the subsequent eruption;
- in cases where volcano had a unique eruption or multiple eruptions with no historical VEI recorded, those entries will be dropped.
The next na's to be treated are in the variables start_day, start_month, end_day, end_month and end_year. For the sake of this study, the granularity chosen was year and month, therefore the day variables are dropped. I created the following criteria to treat missing month and year entries:
- average duration of each eruption for each volcano which has complete date data (start month/year and end month/year);
- average start month for each eruption for each volcano;
- fill in start month where missing and apply average duration;
Once this phase is finalized the dataset is clean and I analyze the distribution of the numerical variables.
At this point I start to treat the categorial variables to transform them into numerical variables using One Hot Encoding. This variables will be used in the next stage of this study when models will be applied in the dataset to create predictions.
Lastly, there is the exploratory analyses applied to the significant volcanic eruptions. I consider eruptions of VEI 5 and above significant given their damage to society and the environment.
