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

1. 
