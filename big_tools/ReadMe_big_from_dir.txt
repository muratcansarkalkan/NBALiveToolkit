big_from_dir - create .big file from directory
version 29-10-2023

----------
Usage
----------
big_from_dir <out path> <in folder path> [options]

----------
Options
----------
All options are optional.
-align <size> - align size in bytes, default value - 4
-order <file names> - order of files, separated by comma (,)
-orderFile <file path> - path to a file with files order
-marker <marker string> - big file marker, default value - "L231"
-printInfo - output info to console while packing
-c - compress files (refpack compression)
-ce - compress files (refpack compression) with extended compression header (use this if you have files larger than 16 MB)
-cf - compress final big file (refpack compression)
-cfk - compress final big file (refpack compression) and also keep uncompressed file
-bh - generate .bh file
-f - replace backslashes (\) with forward slashes (/) in file names
-r - create .big file for each subfolder (output path must be a folder path)

----------
Examples
----------
big_from_dir art_01.big fm13\art_01 -c
big_from_dir "D:\Games\FIFA 08\data\cmn\be\motion.big" D:\motion\08\motion_new
big_from_dir "D:\audio\hdr_eng.big" "D:\fifa07_comm\hdr_eng" -align 128 -marker L234 -orderFile "order_audio_hdrdat.txt"
big_from_dir "D:\Games\FIFA14\Game\data\ui\artassets\eatrax\e1.big" "D:\eatrax\e1" -align 64 -order "0,3,sg1,2,sg2,1"

----------
Order file
----------

Order file is a text file with filenames.

  file1.fsh
  file2.fsh

So file1.fsh will be added first, and then file2.fsh will be added.
You can optionally set the order priority after filename.

  file1.fsh,2
  file2.fsh,1

So file2.fsh will be added first, and then file1.fsh will be added.
By default, the order priority is set to 1000000.
So if you want to place some file in the end of big file, use 1000001 as order priority.

  file3.fsh,1000001

So file3.fsh will be added last, and any other file will be added before file3.fsh.
You can also use wildcard symbol (*) in filenames.

  ch0*.*,1000001
  ch1*.*,1000001
  ch2*.*,1000001
  ch3*.*,1000001
  ch4*.*,1000001
  ch5*.*,1000001
  ch6*.*,1000001
  ch7*.*,1000001
  ch8*.*,1000001
  ch9*.*,1000001
  pn0*.*,1000002
  pn1*.*,1000002
  pn2*.*,1000002
  pn3*.*,1000002
  pn4*.*,1000002
  pn5*.*,1000002
  pn6*.*,1000002
  pn7*.*,1000002
  pn8*.*,1000002
  pn9*.*,1000002