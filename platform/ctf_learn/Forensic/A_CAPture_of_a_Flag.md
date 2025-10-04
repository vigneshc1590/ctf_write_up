
# **A CAPture of a flag**


**Difficulty:** medium

## **TOOLS**
- file
- wireshark
  
## DESCRIPTION 

This isn't what I had in mind, when I asked someone to capture a flag... can you help? You should check out WireShark. [File](https://mega.nz/#!3WhAWKwR!1T9cw2srN2CeOQWeuCm0ZVXgwk-E2v-TrPsZ4HUQ_f4)

>***NOTE: I use wsl(Windows Sub system for linux)it's support most of the tools that's run in linux***

# SOLUTION

- Download the file from the given [File](https://mega.nz/#!3WhAWKwR!1T9cw2srN2CeOQWeuCm0ZVXgwk-E2v-TrPsZ4HUQ_f4)
- Analysis the what type of file is this using `file` and you will get `pcapng capture file - version 1.0`
- You should open the file in `wireshark` and you will get a lot of `TCP,HTTP` and other request and responses
- Use fileter `http`
- Go through those request/response and looking out for flag
- Look all the request you will notice one GET request for `msg` among those request
- **Boom you will get a flag**
- `HINT=base64` 
- **CTFlearn{example_flag_here}**

# lasy approach
- looking for base 64 pattern form the downloaded [File](https://mega.nz/#!3WhAWKwR!1T9cw2srN2CeOQWeuCm0ZVXgwk-E2v-TrPsZ4HUQ_f4)
- using `Strings -n 10` or grep for `msg`
- you will get a [data](https://www.base64encode.org/) to find a flag

### *POINT FOR BEGINNERS*
- Before start analysing the file you will need know to what type of `file` is this
- Get a Familiarize with wireshark it's a swiss Army Knife.

>DON'T JUST RELY ON TOOLS SOMETIMES WE NEED TO MAKE A DIFFERENT APPROACH. AND LESS FAMILIAR IN SOME BASIC/FUNDAMENTAL TOOLS IS ALSO SLOW DOWN YOUR HACKING 

##                                                            HAPPY HACKING

