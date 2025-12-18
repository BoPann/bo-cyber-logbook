
windows registry
It's like the brain of the computer. It stores information such as congiguration settigns and options for the OS. All the registry data are stored in **Registry Editor**. 

components 
- **Hives:** The root folders of the Registry.
    
- **Keys:** Like folders in a file system; they can contain subkeys or values.
    
- **Values:** Like individual files; they contain the actual data (settings).



| **Hive Name**           | **Abbreviation** | **What it Stores**                                                                 |
| ----------------------- | ---------------- | ---------------------------------------------------------------------------------- |
| **HKEY_CLASSES_ROOT**   | **HKCR**         | File associations (which app opens a `.pdf`?) and OLE data.                        |
| **HKEY_CURRENT_USER**   | **HKCU**         | Settings for the **currently logged-in user** (wallpaper, desktop icons).          |
| **HKEY_LOCAL_MACHINE**  | **HKLM**         | Settings for the **entire computer** (drivers, boot settings, installed software). |
| **HKEY_USERS**          | **HKU**          | Profiles for all users who have ever logged into the machine.                      |
| **HKEY_CURRENT_CONFIG** | **HKCC**         | Information about the hardware profile currently in use.                           |
