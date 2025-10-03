
# **BINWALK**
**Difficulty:** Easy

## **TOOLS**
-  Strings
- binwalk or
- foremost
## DESCRIPTION 

Here is a file with another file hidden inside it. Can you extract it? [FILE]("https://mega.nz/#!qbpUTYiK!-deNdQJxsQS8bTSMxeUOtpEclCI-zpK7tbJiKV0tXYY")

>***NOTE: I use wsl(Windows Sub system for linux)it's support most of the tools that's run in linux***

# SOLUTION
Initial steps to find the file type by using `file` to see the image file from cli `eog` will help

- I just download the [.jpeg]("https://mega.nz/#!qbpUTYiK!-deNdQJxsQS8bTSMxeUOtpEclCI-zpK7tbJiKV0tXYY") file from this link, and i just run like basic commands/tools Run **strings** and i get nothing.
- And in generally Forensic challenges will hide the flag in the .jpeg/.wav/.mp4 file , i order to find that, we need some tools like `steghide,zsteg` from linux and online website like *photo forensic(website)* and exiftools for metadata , and binwalk for scanning hidden files and folder in the source
- According to this challenges you need to use binwalk but my `suggestion is "foremost" file craving` it's extract the hidden file and .zip and other file from the source.
- RUN `foremost <*.jpeg>` it will extract the file and folders in the seperate folder `output`
- check the `output` folder you will get two image files.
- **CTFlearn{example_flag_here}**

### *POINT FOR BEGINNERS*
- strings is a good first step, but for steganography/embedded files you usually need binwalk / foremost / zsteg [commands](https://linuxcommandlibrary.com).

- Always verify carved files with file and check their *[magic bytes](https://en.wikipedia.org/wiki/List_of_file_signatures)* before trusting contents.

- Keep your environment isolated (WSL/VM) when running unknown binaries or extracted files.


>DON'T JUST RELY ON TOOLS SOMETIMES WE NEED TO MAKE A DIFFERENT APPROACH. AND LESS FAMILIAR IN SOME BASIC/FUNDAMENTAL TOOLS IS ALSO SLOW DOWN YOUR HACKING 

##                                                            HAPPY HACKING
