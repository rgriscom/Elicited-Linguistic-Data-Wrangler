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

1.  Choose the options in the first form and press the first play button.

  **Operating_System** 
  
 Possible values: Linux, MacOS, Windows
  
 This option is used to create the correct filepaths for the user operating system.
      
  **Text_Data_Source** 
  
Possible values: .csv, .TextGrid, .eaf, .flextext, None
  
This option selects the file format of the text data source and affects the options presented in step 2. If "None" is selected, files will be created with timecode data only. 
      
  **Timecode_Data_Source** 
  
Possible values: .csv, .TextGrid, .eaf, .flextext, None
 
This option selects the file format of the text data source and affects the options presented in step 2. If "None" is selected, files will be created with timecode data only. 
    
  **Add_REFID_Tier** 
  
Possible values: Checked, unchecked

When the box is checked, this option adds a tier or column to the data that consists of a unique reference ID for each annotation or segment. The reference ID includes the filename and the annotation number in the format [filename] _ [annotation number]. For example, the 87th annotation of the file 20200127_RGb would be labeled 20200127_RGb_86. These reference IDs are useful for citing data in publications, as they enable researchers to cite individual annotations within a file.


2. Fill out the information in the generated form and press the second play button. 
  
  **Column_slider** 
  
  Possible values: 1 - 10
  
  Conditions: Text_Data_Source is .csv, .TextGrid, or .eaf
  
  This option is used to indicate the number of tiers or columns which the user would like to extract from the Text_Data_Source. Changing the value changes the number of options presented below the slider in the generated form. 
  
  **Column [number] Name**
  
  Possible values: any
  
  Conditions: Text_Data_Source is .csv, .TextGrid, or .eaf. Number of columns selected with Column_slider.
  
  This field specifies the name of the numbered column or tier of text. The name entered here should be exactly the same as the one used in the Text_Data_Source in order to secure successful data extraction.
  
  **Column [number] Type**
  
  Possible values: Transcription, Translation, Notes
  
  Conditions: Text_Data_Source is .csv, .TextGrid, or .eaf. Number of columns selected with Column_slider.
  
  This field specifies the type of the numbered column or tier of text, which is required for producing .flextext output files. The transcription option produces text that is interpreted by FLEx as target linguistic data, the translation option produces text that is interpreted by FLEx as a free translation of the target linguistic data. Both of these options also produce text in the other output formats. The notes option does not produce any text in the .flextext output because FLEx does not support annotation-level notes, but it does produce text in the other output formats.
  
  **Column [number] ISO 639**
  
  Possible values: any ISO 639 code.
  
  Conditions: Text_Data_Source is .csv, .TextGrid, or .eaf. Number of columns selected with Column_slider.
  
  This field specifies the language of the number column or tier of text, which is required for producing .flextext and .eaf output files. The language should be entered as [ISO 639 code](https://iso639-3.sil.org/code_tables/639/data).
  
  
  **CSV Delimiter**
  
  Possible values: Comma, Tab, Semi-colon
  
  Conditions: Text_Data_Source or Timecode_Data_Source is .csv
  
  This dropdown menu selects the delimiter of the .csv used as input data.
  
  
  
  
  
  
  
      
     
  

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





