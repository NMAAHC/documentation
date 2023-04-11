# PDCO RECEIVING AND REVIEWING PROCESS

This document details the steps for TBMA team members to process PDCO material received for Museum accession considerations. Members will refer to the Smartsheet questionnaires filled by curatorial staff members and the team share folder (links below) to prepare collections for pre-acquisition, accession, and DAMs ingestion.

## Pre-Acquisition
1. Receiving new entry on Time-Base Media questionnaire
   - Team leader receive notifications when additions/changes are made to this sheet.
2. Verify questionnaire data
   - Verify if files are in J drives (Questionnaire: J Drive folder location)
     - If files are received via Dropbox, confirm access and download access copies to J-drive for curatorial team and download exact copies to the born-digital drive and/or NMAAHC Sharepoint site
     - Make sure files are as described in Smartsheet, e.g. if the Smartsheet says “4 audio files” make sure it is not 3 .jpeg files.
   - Reach out to staff member who entered the data for any questions.
   - Create a folder in 04_TR-reviews_inventories > 00_needing-TR-assigned with: **CuratorName_CollectionName**, e.g. _TeddyReeves_SouthEuclidUnitedChurchofChrist_
3. Work with Registrar to get TR number assigned
   - Fill out *TEMPLATE_TBM_PDCO_TR-assignment-info.xltx* with needed Registrar data (see Appendix A for detail).
   - Email the spreadsheet to Drew and cc the Curator and staff who filled out questionnaire to request a TR number and create TMS shell record
   - Once received the TR number, input the TR number in Smartsheet
   - Rename the folder to its TR number and move to 01_TR-needingReview
4.	In 01_TBM_CollectionsQuestionnaire (smartsheet), click the checkbox in Move to TR Sheet column to move row to 02_TBM_TRsTracking (smartsheet)
5.	Team leader will assign Team member to conduct TR review (by selecting team member in TBM Archives & Conservation team column on 02_TBM_TRsTracking)

## Files Review Process

Team member who is assigned to review the files in TR status will receive email notification that details the information of the collection to be review and file location. The object of the review process is to perform assessment of the file qualities, report any technical issues and generate the supplementary files (listed below) for the proposed accession media.
```
•	[filename]_YYYY-MM-DD_checksums.md5
•	[filename]_mediainfo_YYYY-MM-DD.txt
•	TR20xx-xx_YYYY-MM-DD_TBM_assessment.pdf
```

1.	Go to 04_TR-reviews_inventories > 01_TR-needingReview find the folder with the TR number of your assignment. There will be a comment in the Smartsheet pointing to the exact location.
2. Generate mediainfo:
   - NMAAHCmm: _**makemediainfo [file or package]**_
```
           ≈:≈ makemediainfo Nelson\ Malden_Edited_100322.mov Nelson\ Malden_Unedited.mov
```
      - CLI: _**mediainfo -f [file] >> [filename]_mediainfo_YYYYMMDD.txt**_
   
   a mediainfo file named **[file]_mediainfo_YYYMMDD.txt** (e.g. Nelson Malden_Edited_100322.mov_mediainfo_2022-12-09.txt) will be generated in the same directory as your input for each qualified file in the folder/package.

3.	Review mediainfo.txt file to fill out TBM_Pre-acquisitionAssessment.pdf
a.	Some of this info can be found in the TBM_PDCO_TR-assignment-info.xlsx

4.	Generate checksum: 
a.	nmaahcmm:  makechecksum [file or package 1] [file or package 2] [file or package 3]

≈:≈ makechecksum TR2022-97_NelsonMalden/Nelson\ Malden_Edited_100322.mov TR2022-97_NelsonMalden/Nelson\ Malden_Unedited.mov

i.	a .md5 checksum file (e.g. TR2021-51_2022-06-29_checksums.md5) will be generated in the same directory as your input.

b.	CLI:  
i.	(MAC) md5deep -bre [file or package] >> [filepath]/TR20xx-xx_YYYY-MM-DD_checksums.md5
ii.	(PC) md5sum [file path]/[file names] >> [filepath]/ TR20xx-xx_YYYY-MM-DD_checksums.md5

5.	A review completed TR folder would look like below:
6.	Attached the metadata files (mediainfo files, md5s) to the corresponding row in the Smartsheet:
7.	Move Folder to 04_TR-reviews_inventories > 02_reviewComplete

8.	Copy TR20xx-xx_TBM_Pre-acquisitionAssessment into the J-drive accession folder.

9.	Put written assessment into the official Justification Form. This should be located in the J-drive accession folder. If not, ask the curator of record where it is.
a.	Example note for no problems:
i.	“No immediate archival or conservation concerns.” <name> <date>
b.	If there is a problem or concern, describe accurately and concisely

## Accession

Collections in TR status will go before the collections committee and, if approved, will receive Accession numbers from the Registrar. These recent accession numbers will be emailed to staff by the Registrar at some point in the days following the collection committee meeting.

A good way to check on the recent accession numbers is to type the TR into TMS and see if a record with an accession number comes up. When doing this type of search make sure to check the “search alternate numbers” checkbox.  

1.	Confirm accession number in TMS
2.	Input accession number in Smartsheet in column
3.	Select Yes in Accession column in Smartsheet
4.	Use nmaahcmm rename script to rename media files to [Accession number]_1.ext.:

	≈:≈ rename 
	Please enter a Base File Name: TR2022-97
Plese drag in a list of files: Nelson Malden_Unedited.mov Nelson Malden_Edited_100322.mov 
		
(a SI_DAMS-MD_UPDATE_2021_VIDEOTemplate.csv with original file names will be generated in the script)
5.	Rerun checksum for the media files
6.	Create a folder with accession number in 01_accessioned
7.	Move the corresponding TR number folder to the accession number folder (in 01_accessioned)

## DAMs Ingest Process

These steps serve as a quick guide, for detail DAMs workflow, please refer to DigiTeam & DAMs Ingest workflow documentation.

1.	Log into your DAMs import folder (see Appendix B below for detail)
2.	Upload media file(s) and corresponding checksum file(s) to TEMP-XFER folder
3.	Create or update DAMs Video template (If single file: add original file name to DAMS metadata field for the file ingested. For multiple files, see step 5)
4.	Move files to be ingested to Master
5.	Move SI_DAMS-MD_UPDATE_2021_VIDEOTemplate.csv to MD_UPDATE folder
6.	Copy Ready.txt to both MASTER and MD_UPDATE Folder
7.	Received email notification for upload completion
8.	Move files to Checksum
9.	Copy Ready.txt to Checksum
10.	Received email notification for successful verification

## Final Steps

1.	Find records in DAMs, check if all fields are import correctly
2.	Add original file name to DAMS metadata field for each file ingested
3.	If the TBM is not artwork, make sure TBMA is not checked (or remove if you didn’t do so in the import template)
4.	In Smartsheet, check Ingest in DAMs in 02_TBM_TRsTracking
5.	Move row to Ingested


## Appendix A:

Registrar data in *TEMPLATE_TBM_PDCO_TR-assignment-info.xltx*

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

