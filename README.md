# Elicited Linguistic Data Wrangler (eLDW)
**Author:** [Richard Griscom](https://rgris.com/) (Leiden University Centre for Linguistics)

eLDW is a basic script which enables researchers to quickly process elicited linguistic data from a single speaker. When used as part of the [Digital Notebook Method](https://github.com/rgriscom/Digital-Notebook-Method), eLDW allows for the rapid creation of archivable time-aligned text annotations. Some of its notable features include:
* Integration of text data and timecode data from different data sources
* Multiple input and output formats accepted, including .csv, .TextGrid, .eaf, and .flextext
* Batch processing

## Google Colab Notebook
eLDW is available as a [Google Colab Notebook](https://colab.research.google.com/drive/1k_mI4tPUCHVNq_m9_J62fcUVjcuHY7Qb?usp=sharing), which can be used without downloading or installing any software. You must have [a Google account](https://www.google.com/intl/en/account/about/) and be logged into the account in order to use the Colab Notebook. 


## How to use eLDW
Open the notebook and follow the three primary steps outline in the instructions:

1.  Choose the options in the first form and press the first play button. [Step 1 Option Descriptions](https://github.com/rgriscom/Elicited-Linguistic-Data-Wrangler/blob/main/Documentation/Step_1_Option_Descriptions.md)


2. Fill out the information in the generated form and press the second play button. [Step 2 Option Descriptions](https://github.com/rgriscom/Elicited-Linguistic-Data-Wrangler/blob/main/Documentation/Step_2_Option_Descriptions.md)
  
3. Press the "Browse" button to upload your files.

When the process is complete you will be able to download all of the output files in a zipped folder. Download this file to your computer and extract the contents. 
  
  
## Requirements
The eLDW is suitable only for recordings of a single speaker.

### Text Data Input
* .csv - ([Tidy data format](https://www.jstatsoft.org/article/view/v059i10)) Each row in the data should correspond to a single utterance, optionally with the first row serving as column names which can then be used as tier names for the output data. If the first row does not include column names, then columns must be specified in the generated form of Step 2. If paired with timecode data, each row of the text data should correspond to each pair of start and end times.
* .TextGrid - For each tier specified in Step 2, all non-empty segments are used as input text and all empty segments will be disregarded. 
* .eaf - For each tier specified in Step 2, all annotations are used for input text.
* .flextext - Currently only the non-parsed text of .flextext files can be used as input text.

### Timecode Data Input
* .csv - Each row in the data should include one column with a start time in ms and another column with an end time in ms
* .TextGrid - The timecode data for all non-empty segments are used as input timecode.
* .eaf - Only .eaf files which include annotations with identical timecode are currently supported.
* .flextext - Currently only the non-parsed text of .flextext files can be used as input text.

## Output

* .csv - The output .csv file includes the following data, sparated by commas: REF_ID (if selected in Step 1), start time, end time, Tier 1, Tier 2, Tier 3, etc.
* .TextGrid - The output .TextGrid includes the REF_ID tier as the first tier (if selected in Step 1), followed by the text data tiers.
* .eaf - The output .eaf includes the REF_ID tier as the parent tier (if selected in Step 1), with all of the text data as child tiers.
* .flextext - The output .flextext includes the tier selected as Transcription as linguistic data during Step 1, and any tiers selected as Translation are included as free translations of the linguistic data. The REF_ID is included as a free translation with the language code "zxx".








