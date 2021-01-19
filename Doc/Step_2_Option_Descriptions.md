# Step 2 Option Descriptions
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
  
  
  **First row of CSV is column titles**
  
  Possible values: Checked, unchecked
  
  Conditions: Text_Data_Source is .csv
  
  If checked, this option causes the script to process the first row of the .csv file as the column names for the text data.
  
  
  **Expand duration of time segments**
  
  Possible values: Checked, unchecked
  
  Conditions: Any input data is selected for Timecode_Data_Source
  
  If checked, this option presents a slider which can be used to specify the number of milliseconds to subtract from start times and add to end times. This feature is designed specifically for use with timecode data that has been automatically segmented, e.g. by Praat's Annotate to TextGrid (silences) feature, and which might include start and end times which cut off some of the speech. 
  
 **Amount**
  
  Possible values: 0 - 100
  
  Conditions: The "Expand duration of time segments" option has been checked
  
  This slider specifies the number of milliseconds which are subtracted from start times and added to end times. If the expanded durations result in the overlap of two segments in a given file, then the expansion is abandoned and original timecode data are used. 
  
   **Sounding interval**
  
  Possible values: any
  
  Conditions: Text_Data_Source is .TextGrid
  
  This field specifies a string which is used by the script to distinguish between segments in a .TextGrid file which contain sound and those that do not. This feature is intended to be used together with the Praat Annotate to TextGrid (silences) feature, which produces "sounding" segments containing a particular string. If segments which do not contain a sound do not contain text, then this field can be left blank, and the script will include any non-empty segments as text data.
  
  **CSV Time Format:**
  
  Possible values: Seconds, Milliseconds 
  
  Conditions: Timecode_Data_source is .csv
  
  This dropdown menu specifies the type of timecode data included in the .csv file.  
  
  
  
  
