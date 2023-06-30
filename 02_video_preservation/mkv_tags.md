># NMAAHC Matroska container tag values
># **Draft 2023-06-29**

<details>
<summary>
Definition and Scope    
</summary>
<p>

### These draft guidelines pertain to matroska container files created/dervied from born-digital or analog sources, both video and film. These guidelines build upon and should be used in conjunction with the general cataloging rules enumerated in the NMAAHC Cataloging Standards and Guidelines.

<br/>

| tag                       | value                                   | DAMS field                | Comments                                                          | 
| ------------------------- | ------                                  | ------------              | --------                                                          |
| title                     | Twilight City                           | mkv_title                 | title as determined by technician at time of transfer             |
| coding_history            | O=VHS, C=Color, S=Analog, VS= NTSC, F=24, A=4:3, R=640×480, T=Sony SVO-5800,  O=FFV1mkv, C=Color, V=Composite, S=Analog Stereo, F=24, A=4:3, W=10-bit, R=640×480, M=YUV422p10, T=Blackmagic UltraStudio 4K Mini SN123456, ffmpeg vrecord; in-house, O=FFV1mkv, W=10-bit, R640x480, MYUV422p10 N=Emily Nabasny  | mkv_coding_history        | Coding history for tape digitization. Should we use the cumbersome FADGI lingo? |
| camera_make_model         | Canon C300                              | mkv_camera_make_model     | this data should be able to be populate in the tag with already existing metatdata in the file |
| camera_card_script        | nmaahcmm-v0.0.7/camera_cards            | mkv_script_version        | include an attachment with detail operation of camera_cards script (e.g. how many original files and concatenated using ffmpeg,.etc) |
| content_description       | In the 1980s a young journalist...      | mkv_content_description   | short content description created by technician at time of transfer |
| identifier                | 2012.79.1.16.1a                         | mkv_identifier            | unit identifier |
| alternate_identifier      | TR2019-63                               | mkv_alternate_indentifier | for your secret agent ID |
| original_projection_speed | 18fps                                   | mkv_fps                   | we do also put this in the DPX header... but does anyone anywhere ever look at those? |
| originating format        | U-matic                                 | mkv_originating_format    | needs controlled vocab... PBCore... how to enforce? |
| creator                   | Smithsonian NMAAHC                      | mkv_creator               | Entity responsible for creation of digital file |
|||||      
