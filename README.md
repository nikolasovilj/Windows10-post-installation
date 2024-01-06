# Windows 10 post installation procedures

Either run the ```script.ps1``` or use the code snippets from this README.md

***

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
