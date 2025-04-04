?? Intro to bindiffing ??


# Patch diffing

Patch Tuesday
* Is an unofficial term used to refer to when several large companies regularly release software patches for their software products. 
* Occurs on the second Tuesday of each month.


Microsoft on patch Tuesday usually releases security updates.
More about [Microsoft's patching schedule can be found here](https://learn.microsoft.com/en-us/windows/deployment/update/release-cycle#types-of-update-releases).
* 2nd Tuesday of each month - Security patching

Apple usually releases software updates on the second week of each month; not necessarily on Tuesdays.
* More about [Apple security updates can be found here](https://support.apple.com/en-us/100100).





Software Diffing
* 1-days
* researchers, perhaps to discover whether their suggested fixes were applied
* compare and categorise malware; this could help with attribution







# Diaphora
[diaphora.re](https://github.com/joxeankoret/diaphora)


# Bindiff
[bindiff](https://zynamics.com/bindiff.html)
[releases](https://github.com/google/bindiff/releases/tag/v8)



# Winbindex
Amazing resource. Winbindex is essentially a catalogue of Windows binaries, 
[winbindex](https://winbindex.m417z.com/)
[winbindex github](https://github.com/m417z/winbindex)



An index of Windows files which appear in update packages.
It allows viewing info about the files, and downloading some of them from Microsoft servers. -> exe / dll / sys files
At the time of writing the servers are at `microsoft[.]com` and `windows[.]net`


(((
perhaps more for winbindex
https://www.winhelponline.com/blog/download-missing-system-files-dll-exe-sys-from-microsoft-site/
https://www.ghacks.net/2020/07/23/download-individual-microsoft-windows-files-exe-dll-sys-from-microsoft-with-winbindex/
)))



https://learn.microsoft.com/en-us/windows/deployment/update/forward-reverse-differentials





Installing bindiff in Binary ninja
My tool of choice is
Binary Ninja

IDA


examples
