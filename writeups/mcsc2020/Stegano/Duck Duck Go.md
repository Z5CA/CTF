First I checked .jpg file with binwalk .There is nothing.</br>
 In challge's description it said 
 "A duck flying a plane?!?! There must be a hidden meaning".</br>
 So I thought this word "hidden".</br>
 </br>
 I could guess  "steghide" tool that is  able to hide data in various kinds of image- and audio-files.
 `$steghide extract -sf duck4-s.jpg
 
 extract, --extract      extract data
 -sf, --stegofile        select stego file
 
 It showed "Enter Passpharse:"
 I didn't enter passpharse but it worked.
 We got a zip file with password protected.
 I used fcrackzip which is mentioned in steg2.md.
 That was just wasted time. We need to find password.
 I checked meta data of  duck4-s.jpg with exiftool.
 $exiftool duck4-s.jpg
 ExifTool Version Number         : 12.06
File Name                       : duck4-s.jpg
Directory                       : .
File Size                       : 44 kB
File Modification Date/Time     : 2020:09:19 00:34:13+06:30
File Access Date/Time           : 2020:10:06 21:55:43+06:30
File Inode Change Date/Time     : 2020:10:08 01:26:13+06:30
File Permissions                : rwxrwxrwx
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : None
X Resolution                    : 96
Y Resolution                    : 96
XMP Toolkit                     : Image::ExifTool 10.80
Subject                         : flappybird
Image Width                     : 367
Image Height                    : 279
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 367x279
Megapixels                      : 0.102
`
Haha ,We can see in Subject "flappybird".
So I used it to unzip flag.zip.
Gotcha!!! cat flag.txt
Is it a plane... is it a bird... it's cyber duck</br>
Flag is ACSC2019{Is it a plane... is it a bird... it's cyber duck}
 
