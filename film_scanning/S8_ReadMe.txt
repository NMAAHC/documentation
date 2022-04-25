Revised - 2022-04-19 - Blake

1-------------1-------------1-------------1-------------1-------------1-------------1-------------1-------------1-------------1-------------1

This project will provide the following output structure:

/Volumes/xScans/01_Scans/20220419_Bowser_Pearl
└── _S8_131
    ├── mov_2048x1536
    │   ├── 20220419_Bowser_Pearl_S8_131.mov
    │   └── 20220419_Bowser_Pearl_S8_131_overscan.mov
    ├── mp4_1920x1080
    │   └── 20220419_Bowser_Pearl_S8_131_overscan.mp4
    └── mp4_2048x1536
        ├── 20220419_Bowser_Pearl_S8_131.mp4
        └── 20220419_Bowser_Pearl_S8_131_overscan.mp4

4 directories, 5 files

This presumes a project named 'Bowser_Pearl' a reel named 'S8_131' and a selection of all the available pre-made outputs.

A project named 'Bowser_Pearl' means a ScanStation project file named 'Bowser_Pearl'

Example: Bowser_Pearl.cdir

To achieve this open the S8_2K_MOS_Color.cdir file and 'save as' a new file named 'Bowser_Pearl'

To achieve a reel named 'S8_131' go to 'Job Settings' and, at the top, change 'Reel Name' to 'S8_131'


2-------------2-------------2-------------2-------------2-------------2-------------2-------------2-------------2-------------2-------------2

The 'Job Settings' for this project have the following 'Output Path':

S:\01_Scans\%date%_%job%\%reel%\%format%_%resolution%\

Where:

++ S:\01_Scans\
this is the the '01_Scans' directory in the root level of the 'S:' drive mapped to this PC computer. 
The 'S:' drive is also known as the xScans drive and will appear mounted on Mac desktops as such.

++ %date%_%job%\
creates a directory in 'S:\01_Scans\' where '%date%' is replaced by the current date in YYYMMDD format
and '%job%' is replaced by the name of the job, e.g. 'Pearl_Bowser' 
(remember, the name of the job matches the name of the project which is defined by what the .cdir file is named)

++ %reel%\
creates a directory in 'S:\01_Scans\%date%_%job%\' where %reel% is replaced by the name of the reel in the 'Job Settings'

++ %format%_%resolution%\
creates a directory in 'S:\01_Scans\%date%_%job%\%reel%\' where '%format%' is replaced by
the three-letter data format abbreviation of the out put file (e.g. DPX, mov, mp4), 
and '%resolution%' is replaced by the image resolution (width x height) specified in the Output file properties (e.g. 2048x1536)


3-------------3-------------3-------------3-------------3-------------3-------------3-------------3-------------3-------------3-------------3

The resolution, codec and whether the Output file is over-scanned (including as much of the file from edge-to-edge as possible) are 
all indicated in the names of the various Output files that can be chosen in this project, e.g. 'MP4_1920x1080-OS' or 'MP4_2048x1536' (the OS indicates overscan)

Each Output has its own 'Output Path Format Prefix' defined in the setting of each Output. 'Output Path Format' is at the bottom of the settings and has a 
'Prefix' and a 'Suffix'. For this project, the 'Prefix' is filled out and the 'Suffix' is left blank.

The 'Output Path Format Prefix' defines how the Output file will be named. 

Each over-scanned Output has the same 'Prefix' setting, as does each non-over-scanned Output.

The non-over-scanned Output 'Prefix' setting is:

++ %date%_%job%_%reel%
following the same variable substitution logic as the 'Output Path' setting defined in section number 2 above, this will give us a file named 
YYYMMDD_Bowser_Pearl_S8_131.mov or YYYMMDD_Bowser_Pearl_S8_131.mp4, depending on the Output(s) chosen. If the film was scanned
on April 19, 2022 the resulting file name would be '20220419_Bowser_Pearl_S8_131.mov'

The over-scanned Output 'Prefix' setting is:

++ %date%_%job%_%reel%_overscan
following the same variable substitution logic as the 'Output Path' setting defined in section number 2 above, this will give us a file named 
YYYMMDD_Bowser_Pearl_S8_131_overscan.mov or YYYMMDD_Bowser_Pearl_S8_131_overscan.mp4, depending on the Output(s) chosen.

Since the word 'overscan' in the 'Prefix' setting is not a variable it will be written to the file name as is. 
This same method of using a constant instead of variable can also be applied to the 'Output Path' setting.

4-------------4-------------4-------------4-------------4-------------4-------------4-------------4-------------4-------------4-------------4

The aspect ratio of each Output is locked to 4x3, which is the native frame size for most R8, S8 and 16mm. The resolution 2048x1536 is also a 4x3 aspect ratio.

The only exception is the 1920x1080 overscan MP4 Output option. This will produce a 16x9 frame and the Output is locked to 16x9.

To see this for any of the Outputs go the Output settings and in the 'Image Area and Position' choose 'Custom'. 
In the window that comes up, choose lock to 4x3 (or 16x9) and 'Square Pixels'.
Then, position your dotted frame line over the area of the image/film that you want to capture. 

*** 
It is recommended to test you settings with a 100 frame clip and look at the resulting directories and filenames created. 
If something looks off you can adjust it in by reading back over these guidelines and adjusting where necessary. 
Test and retest with 100 frame clips and when everything looks as you want to you can start the full scan. 
***

Scan On!!!
-NMAAHC TBMA
