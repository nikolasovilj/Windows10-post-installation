# Windows 10 post installation procedures

Either run the ```script.ps1``` or use the code snippets from this README.md

***
![image](https://github.com/nikolasovilj/Windows10-post-installation/assets/23420051/33575572-4f92-44da-aa6a-b4fd0843e78d)
![image](https://github.com/nikolasovilj/Windows10-post-installation/assets/23420051/75a01c42-7a01-4f52-9170-50be38fe488c)


TODO:
- [ ] cleanup/speedup procedures
- [ ] write the script once all of the code snippets are done

***

1. Rename the host

    ```powershell
    Rename-Computer -NewName "YourNewComputerName" -Restart
    ```

1. Alt + Tab behaviour - **DOUBLE TEST WITH RESTART**

    ```powershell
    Set-ItemProperty -Path "HKCU:\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Advanced" `
    -Name "MultiTaskingAltTabFilter" -Value 3
    ```

1. Clipboard history

    ```powershell
    Set-ItemProperty -Path "HKCU:\Software\Microsoft\Clipboard" `
    -Name "EnableClipboardHistory" -Value 1
    ```


1. Ransomware protection: Windows Security -> Virus & threat protection -> Manage Ransomware protection -> On  
	* `Set-MpPreference -EnableControlledFolderAccess Enabled`
	* `Add-MpPreference -ControlledFolderAccessProtectedFolders "Path\to\your\folder"`

1. Privacy activity (task view) -> Settings -> Privacy -> Activity history/tasks/

1. Update Windowsa
1. Instaliraj Winget
1. Instaliraj PowerShell 7 i sudo 
1. Instaliraj Terminal aplikaciju

1. Date time/format/keyboard layout
  1. Pod preferred languages instaliraj Croatian
  1. Promijeni Regional Format u Croatian
  1. Instaliraj srpski radi keyboard layouta

1. Upali clipboard history (Win + V)
1. Instaliraj Office

1. Microsoft Defender Application Guard (Turn Windows feature on or off)
  1. Podesi postavke - dozvoli copy paste

1. Sandbox (Turn Windows feature on or off)
1. Windows Security -> Device Security -> Core isolation -> Memory Integrity -> On
1. Podesi night light
1. Ugasi page file ()

1. eID Middleware

1. Firefox i Edge download folderi

1. Start - Settings - Personalization - Start - turn off "Show recently opened items in Jump Lists on Start or the Taskbar.

1. Discord -> Settings wheel next to profile -> Windows Settings -> Start Minimized -> On

#Firefox

browser.tabs.loadBookmarksInBackground (stavi u True)
