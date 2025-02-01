# uk4lat
Ukrainian phonetic layout for latin keyboard

# How to install uk4lat
![Purple line](assets/imgs-for-docs/svg--900x05--c--ff5975.svg)
## Install using precompiled files. 
**Keep this files as they are required to remove/update the layout.** See the update section [below](#how-to-update-uk4lat) <br>
[📥 Download]

## Alternatively, build your own keyboard
### Tools needed:
* MSKLC: Microsoft Keyboard Layout Creator - [📥 Download](https://www.microsoft.com/en-us/download/details.aspx?id=102134)
* MSKLC unofficial documentation: https://msklc-guide.github.io/
### Optional tools:
* Orca (.msi editor) - [🔗 Orca](https://learn.microsoft.com/en-us/windows/win32/msi/orca-exe) is available in the [🔗 Windows SDK Components for Windows Installer Developers](https://learn.microsoft.com/en-us/windows/win32/msi/platform-sdk-components-for-windows-installer-developers)
* Resource Hacker [📥 Download](https://www.angusj.com/resourcehacker/) or similar software

### Steps
1) The quickest way is to load the standard language keyboard in MSKLC and edit whatever you need.<br>
2) Optional edits (see below)
3) In MSKLC, `Project\Build DLL and setup package`
4) Optional edits (see below)
5) Install with `setup.exe`
6) 🎉 Enjoy!

*Note: MSKLC doesn't work very well. If you don't want leftover data you need to do this:<br>

**2-)** To edit the name displayed in the Windows language bar: <br>
2.1) `MSKLC\File\Save source file as` <br>
2.2) Close MSKC <br>
2.3) Open layout.klc with a text editor; edit. <br>
2.4) 🎉 Enjoy!

**4-)** MSKLC defaults to 1,0,3,40. To edit the version number: <br>
4.1) After you have done `Project\Build DLL and setup package` <br>
4.2) Use 'Resource Hacker' to see the content of each of the 3 .dll files in the 3 folders <br>
4.3) Edit:
```
FILEVERSION 1,0,3,40
PRODUCTVERSION 1,0,3,40
[...]
VALUE "FileVersion", "1, 0, 3, 40"
VALUE "InternalName", "uk4lat2 (3.40)"
VALUE "ProductVersion", "1, 0, 3, 40"
```
4.4) Edit with [🔗 Orca](https://learn.microsoft.com/en-us/windows/win32/msi/orca-exe) the .msi files. Each file has 5x instances of the File version to edit.
4.5) 🎉 Enjoy!

# How to update uk4lat
![Purple line](assets/imgs-for-docs/svg--900x05--c--ff5975.svg) <br>
as an example, from `1.0.1.3` to `1.0.1.4`

1) Use `setup.exe` from `1.0.1.3` to remove the layout.
2) Use `setup.exe` from `1.0.1.4` to install the updated layout.
3) Reboot/Logout 
4) 🎉 Enjoy!

Note: It's possible to remove the files in the system folder and the registry entry if you lose the files.

## OS-specific 
### Windows 10
If you go into `Settings\Language Settings\Ukrainian` you can choose to remove the keyboard layout. <br>
This only hides it from the layouts in the start bar. It does not remove it from Windows.
