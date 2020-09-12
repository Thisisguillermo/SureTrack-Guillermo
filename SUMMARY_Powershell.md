# Powershell

## Windows OpenSSH

https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse

```
# Install the OpenSSH Client
Add-WindowsCapability -Online -Name OpenSSH.Client~~~~0.0.1.0

# Install the OpenSSH Server
Add-WindowsCapability -Online -Name OpenSSH.Server~~~~0.0.1.0

# Both of these should return the following output:

Path          :
Online        : True
RestartNeeded : False
```

## Run Elevated Powershell prompt from command-line

https://serverfault.com/questions/464018/run-elevated-powershell-prompt-from-command-line

`powershell`

`Start-Process PowerShell -Verb RunAs`

## Windows update Powershell

https://www.itechtics.com/run-windows-update-cmd/
https://www.techrepublic.com/article/how-to-use-powershell-to-manage-microsoft-updates-on-windows/

`install-module pswindowsupdate`

`Add-WUServiceManager -MicrosoftUpdate`


