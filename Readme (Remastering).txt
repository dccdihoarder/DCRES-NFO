=== Read only if you're having trouble ==

The start of second session is very close to the end of the disc. Because of the reader's
calibration, some consoles may have trouble recognizing this disc. It can be "fixed" remastering
the disc. Here I teach you how to do it. Remember: if you console is recognizing your disc well,
you don't have to worry about that

You must be confortable using Echelon's selfboot method to make it right. Tools needed (not
included in the pack): cdrecord, mkisofs, binhack, ipins.

1) I'll assume the toolkit of Echelon's method is in "c:\selfboot". Copy the "audio.raw" from this
pack to there.
2) Record the audio track as told in Echelon's tutorial. You can use "cdrecord -dev=a,b,c -multi
-audio audio.raw -speed=x" where a,b,c is the number corresponding to your recorder (use "cdrecord
-scanbus" to find out) and x is the recording speed.
3) Create the directory "c:\selfboot\data" and copy the files of the game (extracted from your
already copied disc) to there. Copy "ip.bin" and "mars.txt") from this pack to "c:\selfboot". 
4) Use "cdrecord -dev=a,b,c -msinfo" and it will show you a number. I'll refeer it now on as
"0,11702". If you got a number different of 11702, use YOUR NUMBER, not 11702.
5) Now move "1ST_READ.BIN" of the "c:\selfboot\data" directory to "c:\selfboot".
6) Execute "binhack.exe" and it will ask for data. Type "1st_read.bin" for first question,
"ip.bin" for second, and "11702" (your -msinfo number without the 0,) for third.
7) Move "1ST_READ.BIN" back to the "c:\selfboot\data" directory.
8) Use "mkisofs.exe -C 0,11702 -sort mars.txt -l -o data.iso data", replacing the 11702 if you
need. It will create the file data.iso.
9) Execute "ipins.exe", then type "ip.bin" for first line and "data.iso" for the second one.
10) Burn the final session using "cdrecord -dev=a,b,c -xa1 data.iso -speed=x", replacing a,b,c and
x of course.
11) It's ready to play.

I think only a few people (if any) will need to remaster this disc, however, if a considerable
number of people has problem with this, I can remaster the disc and put it to download too, just
let me know.

=== End of trouble section ===