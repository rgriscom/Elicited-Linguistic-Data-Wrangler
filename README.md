# Elicited Linguistic Data Wrangler (eLDW)
**Author:** Richard Griscom

**Contact:** rgriscom@gmail.com

eLDW is a basic script which enables researchers to quickly process elicited linguistic data from a single speaker. When used as part of the [Digital Notebook Method](https://github.com/rgriscom/Digital-Notebook-Method), eLDW allows for the rapid creation of archivable time-aligned text annotations. Some of its notable features include:
* Integration of text data and timecode data from different data sources
* Multiple input and output formats accepted, including .csv, .TextGrid, .eaf, and .flextext
* Batch processing

# How to use eLDW
## Google Colab Notebook
eLDW is available as a [Google Colab Notebook](https://colab.research.google.com/drive/1k_mI4tPUCHVNq_m9_J62fcUVjcuHY7Qb?usp=sharing), which can be used without downloading or installing any software. You must have [a Google account](https://www.google.com/intl/en/account/about/) and be logged into the account in order to use the Colab Notebook. 

## Requirements for Input Data
### Text Data


It assumes that you have a .wav audio recording, a tab-delimited .tsv file with two or more columns of text data (e.g. transcription and translation), and a .TextGrid file that includes segment timecode data (either manually created or automatically through "Annotate to Silences...").
* It combines the text data and timecode data and outputs in three formats: .EAF, .TextGrid, and .TXT.  

ISO 639 Language Codes: https://iso639-3.sil.org/code_tables/639/data


