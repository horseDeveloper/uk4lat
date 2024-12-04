# uk4lat
Ukrainian phonetic layout for latin keyboard

# How to use uk4lat
## Install using precompiled files
[📥 Download]

## Alternatively, build your own keyboard
### Tools needed:
* MSKLC: Microsoft Keyboard Layout Creator - [📥 Download](https://www.microsoft.com/en-us/download/details.aspx?id=102134)
### Optional tools:
* Orca (.msi editor) - [🔗 Orca](https://learn.microsoft.com/en-us/windows/win32/msi/orca-exe) is available in the [🔗 Windows SDK Components for Windows Installer Developers](https://learn.microsoft.com/en-us/windows/win32/msi/platform-sdk-components-for-windows-installer-developers)
* Resource Hacker [📥 Download](https://www.angusj.com/resourcehacker/)

### Steps
1) The quickest way is to load the stanard language keyboard and edit whatever you need.<br>
2) In MSKLC, `Project\Build DLL and setup package`
3) 🎉 Enjoy*

*Note: MSKLC doesn't work very well. If you don't want leftover data you need to do this:<br>

To edit the name displayed in the Windows language bar:
1) `MSKC\File\Save source file as`
2) Close MSKC
3) Open layout.klc with a text editor; edit.

To edit the version number:
1) After you have done `Project\Build DLL and setup package`
2) Use 'Resource Hacker' to see the content of each of the 3 .dll files in the 3 folders
3) Edit:
```
VALUE "FileVersion", "1, 0, 3, 40"
VALUE "ProductVersion", "1, 0, 3, 40"
```
5) Edit with [🔗 Orca](https://learn.microsoft.com/en-us/windows/win32/msi/orca-exe) the .msi files. Each file has 5x instances of the File version to edit.

🎉 Enjoy!
