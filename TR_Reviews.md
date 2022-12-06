# PDCO RECEIVING AND REVIEWING PROCESS

This document details the steps for TBMA team members to process PDCO material received for Museum accession considerations. Members will refer to the Smartsheet questionnaires filled by curatorial staff members and the team share folder (links below) to prepare collections for pre-acquisition, accession, and DAMs ingestion.

## Pre-Acquisition
1. Receiving new entry on Time-Base Media questionnaire
   - BM/CC receive notifications when additions/changes are made to this sheet.
2. Verify questionnaire data (BM/CC)
   - Verify if files are in J drives (Questionnaire: J Drive folder location)
     - If files are received via Dropbox, confirm access and download copies to J-drive.
     - Make sure all files are playable.
     - Reach out to staff member who entered the data for any questions.
     - Create a folder in 04_TR-reviews with: CuratorName_CollectionName. 
         >Ex. TeddyReeves_SouthEuclidUnitedChurchofChrist
3. Work with Registrar to get TR number assigned (BM/CC)
   - Fill out *TEMPLATE_TBM_PDCO_TR-assignment-info.xltx* with needed Registrar data:
     - **Title:** title or name of the work (can be found in smartsheet). 
     - **Acquisition folders’ location:** location of the files indicated in the questionnaire (email the staff who filled out the questionnaire if this information is not available). 
     - **Total File Size:** in MB or GB (the template will sum up the total file size from the individual file size you entered). 
     - **Curator of Record:** Name of the curator (find in questionnaire). 
     - **Contact information for the acquisition constituent (donor and creator)** 
     - **Individual File information:** 
        - **Original File Name:** enter (copy and paste) individual file name, including extension, here.
        - **Size Mib or Gib, File Type, Codec, Container, Date of Creates, Date of File Last Modification:** find in MediaInfo.
        - **Donor, Creator:** find in questionnaire (sometimes the curators would not share the information, work with Drew). 
        - **Checksum:**
            - run nmaahcmm  (a .md5 checksum file will be generated in the same directory as your input):  
              ```
              makechecksum [file or package 1] [file or package 2] [file or package 3]
              ```
           
            OR 
            - run checksum in CLI:  
              (MAC) `md5deep -bre [file or package] >> [filepath]/checksums.txt`  
              (PC)  `md5sum [file path]/[file names] >> [filepath]/checksums.txt` 

    - Save as *CollectionName_TBM_PDCO_TR-assignment-info.xlsx*

4. Email the spreadsheet to Drew and cc the curator and staff who filled out questionnaire to request a TR number and create TMS shell record.  
5. Once received the TR number, Input the TR number in Smartsheet: 02_TBM_TRsTracking.  
6. Rename the folder to the assigned TR number. 
7. In Smartsheet 01_TBM_CollectionsQuestionnaire, move row to 02_TBM_TRsTracking (by clicking the checkbox in Move to TR Sheet column).  
8. In Smartsheet, assign Team member to conduct TR review (by selecting team member in TBM Archives & Conservation team column on 02_TBM_TRsTracking). 
9. Copy the media file to Z drive (add steps).  

