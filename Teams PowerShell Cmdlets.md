# Managing Microsoft Teams via PowerShell

The PowerShell Cmdlets for managing Microsoft Teams service are split between two powershell modules:

### Microsoft Teams PowerShell Module

The Teams PowerShell module contains all the cmdlets you need to create and manage teams.The Teams PowerShell module can be installed by running the PowerShellGet command below.

`Install-Module -Name MicrosoftTeams`

### Skype for Business PowerShell Module

The Skype for Business PowerShell module contains the cmdlets to manage policies, configurations, and other Teams tools. The Skype for Business Online module needs to be manually downloaded to your computer and installed from here https://www.microsoft.com/en-us/download/details.aspx?id=39366. A restart of your computer may also be needed.

## Skype for Business PowerShell Cmdlets

**Connecting via the Skype for Business PowerShell Module**

Import-Module SkypeOnlineConnector
$userCredential = Get-Credential
$sfbSession = New-CsOnlineSession -Credential $userCredential
Import-PSSession $sfbSession

**Connecting via the Microsoft Teams PowerShell Module**

## Microsoft Teams PowerShell Cmdlets
