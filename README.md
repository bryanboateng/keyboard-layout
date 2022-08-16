# Keyboard Layout

## Windows

### Installation
1. Download and install Microsoft Keyboard Layout Creator (MSKLC)
1. Open "File > Load Source File..."
1. Choose the .klc file from this repository
1. Open "Project > Build DLL and Setup Package"
1. If asked whether you want to see the log, choose "yes". The warning should note that the key OEM_102 may not be present on all keyboards, which is acceptable
1. Open the directory containing the Windows Installer package that has just been created
1. Run the setup.exe that is inside the directory
1. Restart your device

### Uninstallation
1. Open Registry Editor
1. Navigate to "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layouts"
1. Delete the entry corresponding to the layout (usually the last entry of the list)
1. Delete "C:\Windows\system32\bryan.dll"
1. If you are on a 64-bit machine, also delete "C:\Windows\SysWOW64\bryan.dll"
1. Delete the directory containing the Windows Installer package that was created during the installation
1. Restart your device

### How this Layout was created in MSKLC
1. Open "File > Load Existing Keyboard"
1. Choose "US"
1. Open "Project > Properties"
1. Set Properties to the following
    - Name: bryan
    - Description: bryanboateng Custom Keyboard Layout
    - Copyright: (c) *&lt;current year&gt;* bryanboateng
    - Language: English (United States)
1. Click "Ok"
1. Right-click the key between "left shift" and "Z" (VK_OEM_102)
1. Choose "Properties for VK_OEM_102 in all shift states"
1. Set "&lt;Key&gt;" to U+00a8
1. Set "shift+&lt;Key&gt;" to U+00df
1. Enable "Dead Key View" at the top of the dialog
1. Enable "Dead Key?" at the "&lt;Key&gt;" row
1. Click the three dots next to "Dead Key?" to open the dead key dialog
1. Fill the table with the following values

| Base (code point) | Composite (code point) | Base | Composite |
|-------------------|------------------------|------|-----------|
| U+0061            | U+00e4                 | a    | ä         |
| U+0065            | U+00eb                 | e    | ë         |
| U+006f            | U+00f6                 | o    | ö         |
| U+0079            | U+00ff                 | y    | ÿ         |
| U+0075            | U+00fc                 | u    | ü         |
| U+0069            | U+00ef                 | i    | ï         |
| U+0041            | U+00c4                 | A    | Ä         |
| U+0045            | U+00cb                 | E    | Ë         |
| U+004f            | U+00d6                 | O    | Ö         |
| U+0059            | U+0178                 | Y    | ?         |
| U+0055            | U+00dc                 | U    | Ü         |
| U+0049            | U+00cf                 | I    | Ï         |
| U+0020            | U+00a8                 |      | ¨         |

14. Click "Ok"