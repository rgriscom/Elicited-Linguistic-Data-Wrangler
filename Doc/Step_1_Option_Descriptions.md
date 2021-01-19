# Step 1 Option Descriptions  
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

