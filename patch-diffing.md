# Intro to bindiffing ??



## Patch diffing


Software Diffing - why?
* 1-days
* researchers, perhaps to discover whether their suggested fixes were applied
* compare and categorise malware; this could help with attribution, however due to obfuscation it is more of a manual process



Patch Tuesday
* Is an unofficial term used to refer to when several large companies regularly release software patches for their software products. 
* Occurs on the second Tuesday of each month.


Microsoft on patch Tuesday usually releases security updates.
More about [Microsoft's patching schedule can be found here](https://learn.microsoft.com/en-us/windows/deployment/update/release-cycle#types-of-update-releases).
* 2nd Tuesday of each month - Security patching

Apple usually releases software updates on the second week of each month; not necessarily on Tuesdays.
* More about [Apple security updates can be found here](https://support.apple.com/en-us/100100).









## tools?


### Diaphora
[diaphora.re](https://github.com/joxeankoret/diaphora)
[releases](https://github.com/joxeankoret/diaphora/releases)


### Bindiff
[bindiff](https://zynamics.com/bindiff.html)
[releases](https://github.com/google/bindiff/releases/tag/v8)









## How is a Microsoft patch structured?
https://learn.microsoft.com/en-us/windows/deployment/update/forward-reverse-differentials


* Updates to executables are saved in Patch Storage Files (PSF) - another name for them is express download files
    * PSF files are hosted or cached on Windows Update or other update management or distribution servers
    * A device applying express updates uses network protocol to determine optimal differentials, then downloads only what is needed from the update distribution endpoints.
* Update package metadata, content manifests, and forward and reverse differentials are packaged into a cabinet file (.cab). This .cab file, and the applicability logic, will also be wrapped in Microsoft Standalone Update (.msu) format.

https://learn.microsoft.com/en-us/windows/deployment/update/images/psf4.png

f folder -> forward diffs
r folder -> reverse diffs
n folder -> null diffs (used for instance when a new file is introduced)



### Winbindex
[winbindex](https://winbindex.m417z.com/)
[winbindex github](https://github.com/m417z/winbindex)

Amazing resource. Winbindex is essentially a catalogue of Windows binaries, files which appear in update packages.
It allows viewing info about the files, and downloading some of them from Microsoft servers. -> exe / dll / sys files
At the time of writing the servers are at `microsoft[.]com` and `windows[.]net`



### apply patches manually?

There is an excellent walkthrough on how to unpack an msu and apply a delta patch here: [fortra - coresecurity](https://www.coresecurity.com/core-labs/articles/how-deal-microsoft-monthly-updates-reverse-engineering-binary-patches)




# Running bindiff in Binary ninja
Using bindiff / diaphora with IDA is straightforward, however my RE tool of choice lately has been Binary Ninja.

One needs to compile it for the specific python / Binja version

Once that's done, open a file in binja.


Run binexport against both files.



Run bindiff.


examples
