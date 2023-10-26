# capston project
This is the individual repository for CITS5503 capstone project 

# uploaded file
## 1. Labeled Data (Table Extraction).csv
  Dataset manually created by human(answer) and extracted by model
  This is used to evaluate table extraction

## 2. Test Data (text extraction).zip
  Dataset manually created by human(answer) and extracted by model
  This is used to evaluate text extraction

## 3. cv_paddleocr_test.ipynb
  Test text extraction against the table extraction model (OpenCV with morphological transformation)

  To Run Script:

  Ensure you have updated IMAGE_PATH to be the path to the repository
  Ensure input image is the extracted Table in Cropped Images Folders.

  Output:

  Extracted text from the input image in a data frame

## 4. table_text_extraction_evaluation.ipynb
  Table and text extract scripts
  Including data generation for evaluating tables and text extracts

  ### Table Detection
  To Run Script:

  Ensure you have updated DATA_PATH to be the path to the repository
  Ensure you have run Web_Scraping_Python.ipynb and table_transformer.ipynb. This will generate the WAMEX DATA in a file called WAMEX_DATA_EXTRACTED
  
  Output:

  The Table Detection Model scans each .jpg file and will extract tables in a Cropped Images Subfolder. These Subfolders are named by the Afile_DocNum_PageNum so for tables contained on Afile '111' Document 1 and Page 1 these will be contained within '111_1_1 Cropped Images'.
  Within these folders are the extracted table images and they are named by 111_1_1_table_0 for Afile_DocNum_PageNum_table_num.
  After detection and the images are extracted all .jpg files are placed in a folder called jpg_extracted for neatness.
  
  ### Table Extraction
  To Run Script:

  Ensure you have run Table Detection and A File Folders contain the extracted Tables in Cropped Images Folders.

  Output:

  The Table Extraction Model will run over each of the tables contained within the Cropped Images files.
  It will perform Table extraction and save these tables to csv in the A file folder.
  Tables are extracted to csv and are named as Afile_Doc_Page_table_Num. For example 111_1_1_table_0.csv for Afile '111' Document 1 and Page 1 Table 1
