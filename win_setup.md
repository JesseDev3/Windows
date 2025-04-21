# Installing PowerShell on Windows

---

# Detect Architecture
X64 , X86 or Arm64

# Check if PowerShell is installed
```cmd
where powershell
```
# Choice of 
- WinGet (Recommended choice for Windows Clients)
- MSI (Windows Servers and enterprise deployment scenarios)
- Zip (Use this method for Windows Nano Server, Windows IoT, and Arm-based systems)
- .NET (.NET developers that install and use other global tools)
# WinGet
```bash
winget search Microsoft.PowerShell
winget install --id Microsoft.PowerShell --source winget
Env:ProgramFiles\PowerShell\<version>\pwsh.ex
```
# MSI
## From detected Architecture
## ** Silently install PowerShell with all the install options enabled **
- X64
```bash
https://github.com/PowerShell/PowerShell/releases/download/v7.5.0/PowerShell-7.5.0-win-x64.zip
```
- X86
```bash
https://github.com/PowerShell/PowerShell/releases/download/v7.5.0/PowerShell-7.5.0-win-x86.msi
```
- Arm64
```bash
https://github.com/PowerShell/PowerShell/releases/download/v7.5.0/PowerShell-7.5.0-win-arm64.msi
```
- Echo filename and continue
```bash
msiexec.exe /package PowerShell-7.5.0-win-x64.msi /quiet ADD_EXPLORER_CONTEXT_MENU_OPENPOWERSHELL=1 ADD_FILE_CONTEXT_MENU_RUNPOWERSHELL=1 ENABLE_PSREMOTING=1 REGISTER_MANIFEST=1 USE_MU=1 ENABLE_MU=1 ADD_PATH=1
```

---

# Install [Terraform](https://developer.hashicorp.com/terraform/install)
```bash
https://releases.hashicorp.com/terraform/1.11.4/terraform_1.11.4_windows_386.zip
https://releases.hashicorp.com/terraform/1.11.4/terraform_1.11.4_windows_amd64.zip
```

---

# Install Google Cloud [CLI](https://cloud.google.com/sdk/docs/install#windows)
- Win 8.1> & Win Svr 2012>
```bash
(New-Object Net.WebClient).DownloadFile("https://dl.google.com/dl/cloudsdk/channels/rapid/GoogleCloudSDKInstaller.exe", "$env:Temp\GoogleCloudSDKInstaller.exe")

& $env:Temp\GoogleCloudSDKInstaller.exe
```
- Launch installer

# Tools
python




