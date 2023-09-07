≈:≈ camera_cards -h
camera_cards
 1. By default, this script will detect a camera card file/directory structure and transform the original camera card files into a usable AIP. The script will concatenate video files into a single file, move important metadata files into a new directory structure, and create a log of these changes."
  Current camera cards recognized:
      - AVCHD (e.g. Canon C100)
      - Canon XF (e.g. Canon C300)
      - P2 (Panasonic)
      - XAVC (Sony)
      - XDCAM EX (e.g. Canon XF100)
2. If you prefer to package files as-is to preserve your original camera directories, you can choose to compress your directory structure into a tarball. To select this option, use the '-t' flag.
If your camera card structure is not recognized, the script will prompt you to choose one or both of these strategies. If you want to create an AIP with concatenated video files and restructured metadata directories, it is recommended that you review the output to make sure the script was able to process your camera files properly.

Your input package is the top-level directory of your camera card, which should be mounted on your computer or provided as a directory.
Your output package will be named after the MEDIAID you supply and delivered to the AIP destination set in nmaahcmmconfig (AIP_DESTINATION).

The AIP_DESTINATION can be set via nmaahcconfig, or via the -o options, or the script with request it.

Dependencies: ffmpeg md5sum tree mediaconch exiftool ffprobe

Usage: camera_cards -m MEDIAID [ -o AIP_DESTINATION ] [-tca] /path/to/input/camera_card_directory [ /path/to/input/camera_card_directory_2... ]
  -m MEDIAID (type media id for final package, e.g. SC0001_20190101_SMITH_VHS_01)
  -f FORMAT (choose the output format (as a file extension) for the rewrapping process, such as 'mxf' or 'mkv'. The default is set to match the input card set. Experimental.)
  -o AIP_DESTINATION (the output directory for the package); if not supplied, script will look for it in nmaahcconfig
  -t tar camera files and folders into a tarball, compressed with gzip
  -a create packaged AIP; this is the default option, but you can use this flag to specify you want an AIP alongside a tarball (e.g. '-ta')
  -n Do not actually package anything, but just show information about the input and what would happen.
  -h display this help

