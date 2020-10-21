Check given photo with binwalk command.
```$binwalk steg_2.jpg```
You will see like this
```
DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             JPEG image data, JFIF standard 1.01
327455        0x4FF1F         Zip archive data, encrypted at least v2.0 to extract, compressed size: 3970, uncompressed size: 5484, name: flag.png
331569        0x50F31         End of Zip archive, footer length: 22
```
There is some interesting file which is "flag.png".</br>
We can extract it using 
```$binwalk -e steg_2.jpg```
There are two files in extracted folder.
Zip file is protected with password.
Let's bruteforce its password with fcrackzip
```$fcrackzip -u -D -p /usr/share/wordlists/rockyou.txt ./4FF1F.zip ```

```PASSWORD FOUND!!!!: pw == password```


Bingo!!!; we get password
In above command</br>
-u : Try to decompress the first file by calling unzip with the guessed password. This weeds out false positives when not enough files have been given.<br>
-D : Select dictionary mode. In this mode, fcrackzip will read passwords from a file, which must contain one password per line and should be alphabetically sorted.<br>
-p : Set initial (starting) password for brute-force searching to string, or use the file with the name string to supply passwords for dictionary searching.<br>

Unzip file ; password is password
we get flag.png .Open it , Flag is mcsc{*}
