I checked steg3.jpg with exiftool.
$exiftool steg3.jpg 
ExifTool Version Number         : 12.06
File Name                       : steg3.jpg
Directory                       : .
File Size                       : 330 kB
File Modification Date/Time     : 2020:09:20 20:14:08+06:30
File Access Date/Time           : 2020:10:06 21:55:42+06:30
File Inode Change Date/Time     : 2020:10:08 01:26:12+06:30
File Permissions                : rwxrwxrwx
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : inches
X Resolution                    : 300
Y Resolution                    : 300
Comment                         : 'aHR0cDovL3N0ZWdoaWRlLnNvdXJjZWZvcmdlLm5ldA=='
Image Width                     : 1733
Image Height                    : 1733
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:4:4 (1 1)
Image Size                      : 1733x1733
Megapixels                      : 3.0
  Some base64 code is in comment.
echo "aHR0cDovL3N0ZWdoaWRlLnNvdXJjZWZvcmdlLm5ldA==" | base64 --decode
http://steghide.sourceforge.net
That is steghide tool. 
$steghide extract -sf steg3.jpg
I used passpharse " mcsc2018" that is given as hint in challenge.
I got a text file and read it.
Flag is "c3RlZ29fMjAwX2ExbW9zdF8zYTV5"
Bingo!!!
