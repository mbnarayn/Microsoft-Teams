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
    
**Get Detailed Teams Configuration Information** 

The Get-CsOnlineUser cmdlet returns information about users who have accounts homed on Skype for Business Online. The returned information includes standard Active Directory account information (such as the department the user works in, his or her address and phone number, etc.) as well as Teams and Skype for Business Server 2015 specific information: the Get-CsOnlineUser cmdlet returns information about such things as whether or not the user has been enabled for Enterprise Voice and which per-user policies (if any) have been assigned to the user.

It includes information around any custom policies that may have been assigned to the users. The policies field is blank if only the default global policies are assigned.

`Get-CsOnlineUser`

**Get Detailed Teams Configuration Information for a Specific User**

`Get-CsOnlineUser -Identity JoeBlogs@domain.co.uk`



## Microsoft Teams PowerShell Cmdlets

**Connecting via the Microsoft Teams PowerShell Module**

