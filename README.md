# Elicited Linguistic Data Wrangler (eLDW)
**Author:** [Richard Griscom](https://rgris.com/) (Leiden University Centre for Linguistics)

eLDW is a basic script which enables researchers to quickly process elicited linguistic data from a single speaker. When used as part of the [Digital Notebook Method](https://github.com/rgriscom/Digital-Notebook-Method), eLDW allows for the rapid creation of archivable time-aligned text annotations. Some of its notable features include:
* Integration of text data and timecode data from different data sources
* Multiple input and output formats accepted, including .csv, .TextGrid, .eaf, and .flextext
* Batch processing

## Google Colab Notebook
eLDW is available as a [Google Colab Notebook](https://colab.research.google.com/drive/1k_mI4tPUCHVNq_m9_J62fcUVjcuHY7Qb?usp=sharing), which can be used without downloading or installing any software. You must have [a Google account](https://www.google.com/intl/en/account/about/) and be logged into the account in order to use the Colab Notebook. 


## How to use eLDW
There are three primary steps to using the eLDW notebook:

1.  Choose the options in the first form and press the first play button. [Step 1 Option Descriptions](https://github.com/rgriscom/Elicited-Linguistic-Data-Wrangler/blob/main/Documentation/Step_1_Option_Descriptions.md)


2. Fill out the information in the generated form and press the second play button. [Step 2 Option Descriptions](https://github.com/rgriscom/Elicited-Linguistic-Data-Wrangler/blob/main/Documentation/Step_2_Option_Descriptions.md)
  
3. Press the "Browse" button to upload your files.
  
  
  
  
  
  
  
      
     
  

2.
3.
## Requirements
### Text Data Input
* .csv - Each row in the data should correspond to a single utterance, optionally with the first row serving as column names which can then be used as tier names for the output data. If paired with timecode data, each row of the text data should correspond to each pair of start and end times.
* .TextGrid - All non-empty segments are used as input text and all empty segments will be disregarded. 
* .eaf - All annotations are used for input text.
* .flextext - Currently only the non-parsed text of .flextext files can be used as input text.

### Timecode Data Input
* .csv - Each row in the data should include one column with a start time in ms and another column with an end time in ms
* .TextGrid - The timecode data for all non-empty segments are used as input timecode.
* .eaf - Only .eaf files which include annotations with identical timecode are currently supported.
* .flextext - Currently only the non-parsed text of .flextext files can be used as input text.

### FLEx Output Requirements





