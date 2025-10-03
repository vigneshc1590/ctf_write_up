
# **seeing is believing Audio/spectogram forensic**

**ctf site: ctflearn.com**

**Difficulty: HARD** 

## **TOOLS**
- ffmpeg
- sonic visualizer or sox
- binwalk
- zbarimg
- eog

## DESCRIPTION 

`My colleague's an astronaut who's currently on a mission orbiting in space. Just a few hours ago, unfortunately, his communication device caught fire so he's unable to report back to base. I did, however, receive a strange file that I can't seem to open. I think it may shed some light on his situation. Can you help me save poor boy Johnny?` [File](https://mega.nz/#!LTRUTaZb!9Nh0NwDONJQiOThif3G62evP8H_W9eIJSu0PdBQWKyg)

>***NOTE: I use wsl(Windows Sub system for linux)it's support most of the tools that's run in linux***

# SOLUTION

- just download the file form provided [link](https://mega.nz/#!LTRUTaZb!9Nh0NwDONJQiOThif3G62evP8H_W9eIJSu0PdBQWKyg).
- unzip the `.zip` file.
- the extracted file containing `help.me in the folder seeingisbelieving` 
- At first running basic commands like `strings, hexdump, xxd`.
- But nothing will help with this challenge.
- running `file` on the help.me file you will notice the file type `HINT: googling about OGG and spectogram`

- `Let's think with basic , generally audio forensic/stegnography challenges hide their flag with in the .ogg, .wav, .mp3 with visual text image`

- in order to get that flag we need to think extract the hidden file/folder, but in this challenges you get some `MYSQL FILES` but it's a decoy data.

>NOTE: read about [QR-CODE](https://en.wikipedia.org/wiki/QR_code)

**APPROACH-1**
- change the .me to .ogg as per the result of `file` result.

- And run this `.ogg` file in the `sonic visualizer` add a layer with `spectogram` and you get `SEE` data and adjust.(learn how to use sonic visualizer)

- From that data you will get the flag CTF{YOU_WILL_FIND_THAT_FLAG}

**APPROACH-2**

THIS IS MY WAY TO GET THAT DATA WILL GIVE US FLAG
- make sure these tools will install on you maching ffmpeg,sox,zbarimg.

- Run ffmpeg or sox to extract the `data` that will bring us `flag` (ffmpeg -i help.me -lavfi "showspectrumpic=s=2000x2000:color=channel" huge_spectro.png),(sox output.wav -n spectrogram -x 1200 -y 1200 -z 100 -Z -20 -o hd_spectro.png)

- use that data[HINT:`c2NhbiB0aGUgUVItQ09ERQ==`] to get a `flag`

- **CTFlearn{example_flag_here}**

### *POINT FOR hackers*
- Always check the hidden .zip, .wav, .ogg, .zlib files from the source file that get form ctfs.
- Audio steganography often requires iterative image processing (different spectrogram parameters + contrast tweaks).

### *real world approach*
- EVIDENCE PRESERVATION: Created forensic image/artifact (.dd, .wav, .png, flashdrive,etc) apart from the original in order to corrupt the original file
- FILE SYSTEM ANALYSIS: Understood NTFS structure (fsstat,file)
- DIRECTORY/file MAPPING: Enumerated all hiddenn files 
- TARGETED EXTRACTION: Recovered specific evidence 
- DATA CORRELATION: Connected multiple data points
- REPORTING: Documented findings

>DON'T JUST RELY ON TOOLS SOMETIMES WE NEED TO MAKE A DIFFERENT APPROACH. AND LESS FAMILIAR IN SOME BASIC/FUNDAMENTAL TOOLS IS ALSO SLOW DOWN YOUR HACKING PROCESS.

##                                                            HAPPY HACKING
