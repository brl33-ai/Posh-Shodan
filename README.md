Posh-Shodan (for MacOS)
===========

PowerShell Module to interact with the Shodan REST API https://developer.shodan.io/ provided with the proper API key. 

# Install
To install the module including all source code you can just run in a PowerShell v3 or higher session the following command:
<pre>
iex (New-Object Net.WebClient).DownloadString("https://gist.githubusercontent.com/mahatah/e72cd157ecfbb5c23d36e1140ff38c20/raw/71f6d2ba428e9e4c72db68a039ddd10a1086b202/PoshShodanInstallMacOS.ps1")
</pre>

The installation process should look like:
<pre>
PS C:\> iex (New-Object Net.WebClient).DownloadString("https://gist.githubusercontent.com/mahatah/e72cd157ecfbb5c23d36e1140ff38c20/raw/71f6d2ba428e9e4c72db68a039ddd10a1086b202/PoshShodanInstallMacOS.ps1")
Downloading latest version of Posh-Shodan (for MacOS) from https://github.com/mahatah/Posh-Shodan/archive/master.zip
File saved to /tmp/Posh-Shodan.zip
Relocating folder to PowerShell Modules location
Module has been installed

CommandType     Name                                               ModuleName
-----------     ----                                               ----------
Function        Get-ShodanAPIInfo                                  Posh-Shodan
Function        Get-ShodanDNSResolve                               Posh-Shodan
Function        Get-ShodanDNSReverse                               Posh-Shodan
Function        Get-ShodanHostServices                             Posh-Shodan
Function        Get-ShodanMyIP                                     Posh-Shodan
Function        Get-ShodanServices                                 Posh-Shodan
Function        Measure-ShodanExploit                              Posh-Shodan
Function        Measure-ShodanHost                                 Posh-Shodan
Function        Read-ShodanAPIKey                                  Posh-Shodan
Function        Search-ShodanExploit                               Posh-Shodan
Function        Search-ShodanHost                                  Posh-Shodan
Function        Set-ShodanAPIKey                                   Posh-Shodan

</pre>

After install set your API key and use a Master Password to encrypt it on disk:
<pre>
PS C:\> Set-ShodanAPIKey -APIKey 238784665352425277288393 -MasterPassword (Read-Host -AsSecureString)
</pre>
The key is now saved in a secure manner on disk and set as the key for use for all other commands.
For loading a stored key after opening a new session just issue the command to read the key with you master password:
<pre>
Read-ShodanAPIKey -MasterPassword (Read-Host -AsSecureString)
</pre>
