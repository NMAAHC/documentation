># NMAAHC RAWcooked Guidelines 

<details><summary>INTRODUCTION: General package structure for RAWcook-ing DPX film scans</summary>

>### This intro section describes general package structure for directories of DPX film scans and files designated to be attachements in the Matroska container created via RAWcooked. 
>#### Tags will be discussed later.  

<br/>

The most general directory structure for DPX films scans and attachments is:

<details><summary>Structure</summary>
<img src="images/DPX_directoryStructure.png">
</details>

<details><summary>Files</summary>

- the top directory is Object_ID_resolution
	- this should be constructed at the time of scanning
	- the Object ID is the NMAAHC Object ID number
	- the resolution is the is the pixel resolution of the DPX scans
- the .wav file will exist if the film being scanned has an audio track
	- PCM/24/48
- the .dpx files are all the frames of the film that were scanned
	- NMAAHC naming structure:
		- OBJECT_ID_7digit.dpx
		- start with 0000000.dpx
		- e.g. 2012_79_1_16_1a_0000000.dpx
- the .TIF files are photos of the physical object
- README.txt
	- notes
	- need to structure this
	- current "my name is Crystal and when I was making these DPX I was thinkng about the stars."
- .zip file is a SD .mp4 of the full film being scanned
	- this may not actually be an acceptable attachment
	- will discuss further with Jerome/Dave
	- should be made at time of scan
- still-01_JPC_AV-474_0000226.png
	- these are .dpx that were trasncoded into .png via Photoshop to be representative stills
	- make 3-4 per scan


</details>
<details><summary>Tags</summary>
</details>

</details>