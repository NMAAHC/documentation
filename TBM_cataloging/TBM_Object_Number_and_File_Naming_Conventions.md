># NMAAHC Object Number and File Naming Conventions
># Time-Based Media  

## **Motion Picture Film**

### This section describes how motion picture films and their assocaited components and/or accessories numbered. 
#### It also desceribes how digital preservation files and derivatives are named.  

<br/>
The most general formulation for numbering films on one reel is:

>**2018.37.2.1a**  
>*[accessionYear].[collectionNumber].[workNumber].[instantiationNumber][componentElement]*  

<br/>  
The most general formulation for numbering films on multiple reels is:

>**2018.37.2.1a**  
>**2018.37.2.1b**  
>*[accessionYear].[collectionNumber].[workNumber].[instantiationNumber][componentElement]*

<br/>


*where:*


>***Accession Year*** = the year in which the collection is accessioned

>***Collection Number*** = the order in which the collection was accessioned in that accession year 

>***Work Number*** = the work (or object) number in the accessioned collection. 
>> ##### Note that works (or objects) can only share work numbers when they are within the same collection.

>***Instantiation Number*** = a number for the instantiation of a work (or object)

>***Component Element*** = starting with letter **a**, letter all films first then number all cans, reels and ephemera as components or accessories to their associated component element.

>> ##### For films to be projected, i.e., 35mm showprint collections, a reel number may be added to the physical film head/tail leader and the film can for projection booth clarity: reel number = R1 for reel 1, R2 for reel 2, R3 for reel 3, etc.  
<br/>  

- - -  
```
Mixed archival collections containing time-based works, such as the Pearl Bowser collection, have a Series Number inserted between the Collection Number and Work Number. This number is used to indicate the type of media carrier.

>1. motion picure film: - all gauges and bases
>2. video: tape-based video formats, both cassette and open-reel   
>3. audio: tape-based audio formats, both cassetes and open-reel
>4. optical discs: all optical disc formats - DVD, CD, Laserdisc, etc.
>5. digital carriers: all digital carriers - harddrives, thumbdrives, computer disks, etc.
>>> ###### the content of the digital carrier, e.g. digital photos, digital video, digital audio, software, word processing documents, etc., does not impact the numbering
>6. photographs: silver based, other analog processes and printed digital images
>7. paper items: all loose leaf paper items, flyers, posters, etc.
>8. bound paper items: books and magazines
>9. objects: furniture, trophies, clothing, all other objects
``` 
- - -  
<br/>

The character `a` must be used to designate the first physical carrier for the essence or signal (videotape, audiotape or film), and that the subsequent characters be used for any remaining phsyical carriers in the instantiation. Any containers, cans, cases or other ephemera related to the physical carrier will likley be accessory components in TMS.
>> ##### acessory components in TMS are differentiated from "part of an object" components.  
<br/> 

For example, where the work is a feature film in a can on one reel/core with Work Number 2018.37.2, the film itself will have the Instantiation Number `1` with Component Element `a`, e.g. object number `2018.37.2.1a`, while the can holding the film will have the same Instantiation Number and Component Element with the Accessory Suffix `acc1` appened with an underscore, e.g. object number `2018.37.2.1a_acc1` and the reel/core holding the film will have the Suffix Element `acc2`, e.g. object number `2018.37.2.1a_acc2`. Any additional ephemera in the film can, such as lab printing records or other pieces of filmlab paper, will have the Suffix Element `_acc3` and so on.  

When a accessory is associated with more than one Component Element, that accessory will have both Component Element letters in its object number. For instance, if a film can with the Accessory Suffix acc_1 contains two reels/cores of film with object numbers `2018.37.2.1a` & `2018.37.2.1b`, the object number for the film can will be `2018.37.2.1ab_acc1`. Don't make two object numbers for the can, e.g. creating both `2018.37.2.1a` and `2018.37.2.1b` for the singular can is incorrect. 

>> ##### when deciding what numerical order to creat the accessories to an object, give number `1` to the accessory carrying the most metadata about the object. For films this is most often the can/case and, as such, the can/case if given Accessory Suffix number `1` while reels/core and other ephemera are given later numbers. Don't skip numbers when assigning Accessory Suffix. 
<br/>
Given the variety of media objects across the Museum's time-basd collections of film, video, audio and digital objects, this process of naming and numbering is difficult to formulate for every possible situation and this documentaiton is a living document. The following scenarios provide guidance for naming and numbering works on film and their associated digital derivatives.  

---

<br/>

>### **Circumstance A**:

*One motion picture film sound film on a metal projection reel contained in a metal canister.*

**For film:**  
>*accessionYear(2012).collectionNumber(79).workNumber(169).instantiationNumber(1)componentElement(a)*  

**For metal canister:**
>*accessionYear(2012).collectionNumber(79).workNumber(169).instantiationNumber(1)componentElement(a)_acc1*  

**For metal projection reel:**
>*accessionYear(2012).collectionNumber(79).workNumber(169).instantiationNumber(1)componentElement(a)_acc2*  

**For DPX package:**
>*accessionYear(2012)_collectionNumber(79)_workNumber(169)_instantiationNumber(1)componentElement(a)_DPX.mkv*  

**For digital audio file accompanying DPX package:**
>*accessionYear(2012)_collectionNumber(79)_workNumber(169)_instantiationNumber(1)_AUD.wav*  

**For digital file access file derived from DPX package:** 
>*accessionYear(2012)_collectionNumber(79)_workNumber(169)_instantiationNumber(1)componentElement(a)_DER_01.mp4

| Component | Object # |
| --- | --- |
| Film | 2012.79.169.1a |
| Metal canister | 2012.79.169.1a_acc1 |
| Metal projection reel	| 2012.79.169.1a_acc2 |
| Lab paper in can | 2012.79.169.1a._acc3 |
| DPX Package (ffv1/mkv) |	2012_79_169_1a.mkv |
| Audio file accompanying DPX package | 2012_79_169_1a_AUD.wav |
| Access copy derived from DPX Package | 2012_79_169_1a_DER_01.mov |
|  |  |

>> ##### Filenames for digital files will by necessity transform all periods within the object number into underscores, due to the fact that using periods in filenames can result in problems when trying to automate or batch digital preservation processes.

---
<br/>

>### **Circumstance B**:

*Two reels of sound 16mm film comprising one 'work', held on plastic cores inside a single 35mm metal canister.*

**For film (reel 1):**
>*accessionYear(2015).collectionNumber(167).workNumber(5).instantiationNumber(1)componentElement(a).reelNumber(R1)*

**For film (reel 2):**
>*accessionYear(2015).collectionNumber(167).workNumber(5).instantiationNumber(1)componentElement(b).reelNumber(R2)*

**For plastic core (reel 1):**
>*accessionYear(2015).collectionNumber(167).workNumber(5).instantiationNumber(1)componentElement(c).reelNumber(R1)*

**For plastic core (reel 2):***
>*accessionYear(2015).collectionNumber(167).workNumber(5).instantiationNumber(1)componentElement(d).reelNumber(R2)*

For metal canister: 
>accessionYear(2015).collectionNumber(167).workNumber(5).instantiationNumber(1)componentElement(abe)_acc1

For DPX package:
>accessionYear(2015)_collectionNumber(167)_workNumber(5)_instantiationNumber(1)

For digital audio file accompanying DPX package (reel 1):
>accessionYear(2015)_collectionNumber(167)_workNumber(5)_instantiationNumber(1)_R1_AUD.mov

For digital audio file accompanying DPX package (reel 2):
>accessionYear(2015)_collectionNumber(167)_workNumber(5)_instantiationNumber(1)_R2_AUD.mov

For digital file ProRes derived from DPX package (reel 1&2): 
>accessionYear(2015)_collectionNumber(167)_workNumber(5)_instantiationNumber(1)_R1R2_DER_01.mov*

For digital file v210 derived from DPX package (reel 1):
>accessionYear(2015)_collectionNumber(167)_workNumber(5)_instantiationNumber(1)_R1_DER_02.mov

For digital file v210 derived from DPX package (reel 2):
>accessionYear(2015)_collectionNumber(167)_workNumber(5)_instantiationNumber(1)_R2_DER_02.mov

Virtual Object Number (1st alternate ID in DAMS)	2015.167.5
Film (reel 1)					2015.167.5.1a
Film (reel 2)					2015.167.5.1b
Plastic core (reel 1)				2015.167.5.1a_acc1
Plastic core (reel 2)				2015.167.5.1b_acc1
Metal canister					2015.167.5.1ab_acc1
DPX Package					2015.167.5.1ab
Audio file accompanying DPX package reel 1		2015_167_5_1a_AUD.wav
Audio file accompanying DPX package reel 2		2015_167_5_1b_AUD.wav
ProRes Derived from DPX Package reel 1&2		2015_167_5_1ab_DER_01.mov*
v210 Derived from DPX Package reel 1		2015_167_5_1_R1_DER_02.mov
v210 Derived from DPX Package reel 2		2015_167_5_1_R2_DER_02.mov

This naming schema extends for any number of reels that compose a single ‘work’ with the films being assigned consecutive letters first and then the cannisters being assigned acc number, then and paper ephemera or lab notes contained in the cannister and finally  the reels/cores  of  the films.

*NMAAHC policy is to combine DER_01 files from multiple reel films. This is in order to make streaming the video to public via the Smithsonian Media Asset Delivery System (MADS) a more efficient process and ease the process of uploading to DAMS. DER_02, which is not ingested into DAMS, will remain as separate video files for each reel. 

 