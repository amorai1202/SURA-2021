This GREGORY_DATA_DISCOVERY_Readme.txt file was generated on 20200219 by Kathleen Gregory

-------------------
GENERAL INFORMATION
-------------------

Title of Data Set: Data discovery and reuse practices of researchers and research support professionals

Author Information:
Kathleen Gregory, Data Archiving and Networked Services, Royal Netherlands Academy of Arts and Sciences
kathleen.gregory@dans.knaw.nl / kathleengregory122@gmail.com


Principal Investigator: Kathleen Gregory
Associate or Co-investigator:Paul Groth, Andrea Scharnhorst, Sally Wyatt

Brief description:
This data set consists of data collected from an online survey questionnaire designed to examine the data discovery and data reuse practices of individuals involved in research, across disciplinary domains, who seek and use data they do not create themselves.

Date of data collection: 4 week period between 201809-201810

Geographic location of data collection: Global. Respondents from 105 countries. 

Funding sources that supported the collection of the data: This work is part of the project Re-SEARCH: Contextual Search for Research Data and was funded by the Netherlands Organization for Scientific Research (NWO). [Grant 652.001.002] 


--------------------------
SHARING/ACCESS INFORMATION
-------------------------- 

This data is available under a CC-BY license (https://creativecommons.org/licenses/by/4.0/). You may share or adapt the data but are required to give attribution. 

The data files are anonymised. 

Recommended citation for the data:
Gregory.(2020). Data discovery and reuse practices of researchers and research support professionals.[Data set]. DANS-EASY. DOI.

Citation for and links to publications that cite or use the data:
Gregory, K., Groth, P., Scharnhorst, A., & Wyatt, S. (2019). Lost or found? Discovering data needed for research. arXiv preprint arXiv:1909.00464.

 
--------------------
DATA & FILE OVERVIEW
--------------------

This data set consists of one text file, four csv files, and one pdf file, which must be used in conjunction with each other in order to understand the data. 

(1) GREGORY_DATA_DISCOVERY_Readme.txt	
This text file provides guidance to the dataset

(2) datadiscovery_researchers.csv 	
This csv file contains data for respondents identifying themselves as researchers, students, managers or other types of professionals. 

(3) datadiscovery_supportprof.csv	
This csv file contains data for respondents identifying themselves as librarians, archivists or research/data support providers. We term this group "research support professionals" in this data description and in related articles. 

(4) variable_labels_researchers.csv	
This csv file contains a description of the variable names in the datadiscovery_researchers.csv file

(5) variable_labels_supportprof.csv	
This csv file contains a description of the variable names in the datadiscovery_supportprof.csv

(6) datadiscovery_questionnaire.pdf	
This pdf file contains the questionnaire for both researchers and research support professionals. Variable names are listed in parentheses after the corresponding questions. 

--------------------------
METHODOLOGICAL INFORMATION
--------------------------

Description of original purpose of study: 
The questionnaire was designed to address the following research aims:
- To learn more about the people in academia seeking and reusing data
- To learn more about the data needs of respondents
- To learn more about how respondents discover and seek data for reuse
- To learn more about how respondents evaluate and make sense of data for reuse

Description of questionnaire design:
The questionnaire used a branching design consisting of a maximum of 28 primarily multiple choice items. Nine of the multiple choice questions allowed for multiple responses. There were three open response questions. The majority of multiple choice questions included the possibility for participants to write-in an "other" response. Research support professionals completed a slightly different version of the questionnaire. Both the qualitative and quantitative data are included in datadiscovery_researchers.csv and datadiscovery_supportprof.csv. files. 

Description of questionnaire administration:
The questionnaire was scripted and and administered using the Confirmit software. 

Description of sample recruitment and response:
Recruitment emails were sent to a random sample 150,000 authors who are indexed in Elsevier’s Scopus database and who have published in the past three years. The recruitment sample mirrored the distribution of published authors by country within Scopus. Two batches of recruitment emails were sent: one of 100,000 and the other of 50,000. One reminder email was sent. A member of the Elsevier Research and Academic Relations team created the sample and sent the recruitment letter.

We received 1637 complete responses during a four-week survey period. We posted messages to discussion lists in research data management and library science to further recruit support professionals. We received an additional 40 responses with this method. The total number of responses to the survey was 1677 complete responses. 

Brief description of sample:
- 1677 complete responses
- Respondents from 105 countries.
- 82% of respondents identify as researchers
- Many respondents in middle stages of careers (40% with 6-15 years of experience; 30% with 16-30 years of experience)

Description of limitations and biases:
- The data are descriptive of the behaviours of respondents. Work must be done to make the data generalisable to broader populations. Limited information is available about non-respondents. 
  
- Respondents are data-aware people, involved in research, with the ability to respond to a survey in English. 

- Disciplinary domains are not equally represented in Scopus.

- Self-reported responses could be overly positive,

- Responses could be influenced by wording and presentation of questions.

- Data represent only complete responses to survey.  


Methods for processing the data: 
All data cleaning and processing was done in R. 
 
The data were downloaded from the survey system by the employee from Elsevier and were sent to the primary investigator. The data were downloaded as csv files in two batches: the 1637 responses received before additional recruiting of research support professionals, and the 40 responses received after this second stage of recruitment. Seven respondents in the first batch identified as being research support professionals. These responses were extracted and added to the csv file from the second batch. This produced separate files for research support professionals and the remainder of respondents.

Variables representing questions asked only to research support professionals were removed from datadiscovery_researchers.csv. Variables representing questions asked only to researchers were removed from datadiscovery_supportprof.csv.

Variables were renamed using mnemonic names to facilitate understanding and future analysis. Variable names for questions asked to both research support professionals and researchers have the same name in both data files. 

Variables were re-ordered to match the order of the questions presented in the questionnaire. Demographic variables, including role, were grouped together at the end of the data files. 

Missing values/zeroes/NAs
- Multiple choice responses not selected by respondents were recorded as a 0. 
- If a respondent was not asked a question, the response is coded as "Not asked." 
- If a respondent wrote "NA" or a similar phrase in the open response questions, this was left unchanged. 
- If a respondent did not complete an optional open response question, this is recorded as a space, which appears as an empty cell. In the analysis program R, this empty space is represented as " ".


Quality-assurance procedures performed on survey questionnaire and the data:
- Questionnaire was piloted in two phases. Modifications were made to the order and wording of the questions after the pilots.
- Checks for NA's and missing values were performed for both data files. 
- Factor-level summaries were performed for all multiple choice questions. 
- Summary checks of total responses for all variables were performed routinely during data cleaning. Summary checks for re-named and re-ordered variables were also performed. 


Related publications with methodological details:
Article reporting on initial quantitative data analysis:Gregory, K., Groth, P., Scharnhorst, A., & Wyatt, S. (2019). Lost or found? Discovering data needed for research. arXiv preprint arXiv:1909.00464.


--------------------------
DATA-SPECIFIC INFORMATION 
--------------------------

(1) datadiscovery_researchers.csv 

Number of variables: 165

Number of cases/rows: 1630

Naming scheme of variables: Variables names begin with a mnemonic code representing the research aim which they are related to. The same variable names are used for identical variables in both data files. The primary codes are:

need_ : data needs
use_ : purposes for which data are used
find_ : data search and discovery practices
strategy_ : data discovery strategies. Related to find_
source_ : sources used to discover data. Related to find_
eval_ : data evaluation and sense-making 
accss_ : data access
disc_ : discipline chosen by respondent
dem_  : demographic

The csv file variable_labels_researchers.csv provides descriptions of all variable names. 


(2) datadiscovery_supportprof.csv

Number of variables: 167

Number of cases/rows: 47

Naming scheme of variables: Variables names begin with a mnemonic code representing the research aim which they are related to. The same variable names are used for identical variables in both data files. The primary codes are:

need_ : data needs
use_ : purposes for which data are used
find_ : data search and discovery practices
strategy_ : data discovery strategies. Related to find_
source_ : sources used to discover data. Related to find_
eval_ : data evaluation and sense-making 
accss_ : data access
disc_ : discipline chosen by respondent
dem_  : demographic

The csv file variable_labels_supportprof.csv provides descriptions of all variable names. 
   
