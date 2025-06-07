# PowerShell Cheat Sheet

## Basic Commands

```powershell
"Hello World!" | Out-Default
```

- `Get-ChildItem`
- `Copy-Item`
- `Clear-Host`
- `Write-Output`
- `Get-Content`
- `Remove-Item`
- `Get-Process`
- `Set-Location`
- `Get-Location`
- `Sort-Object`
- `ForEach-Object`
- `Where-Object`
- `Stop-Process`
- `Get-Member`
- `Select-Object`

---

## System Information

```powershell
# OS Name
(Get-WmiObject Win32_OperatingSystem).Name

# OS Architecture
(Get-WmiObject Win32_OperatingSystem).OSArchitecture

# Machine Name
(Get-WmiObject Win32_OperatingSystem).CSName

# List all properties
Get-WmiObject Win32_OperatingSystem | Get-Member
```

---

## User & Group Management

```powershell
# User permissions
net user /domain <username>

# Group details
Get-ADGroup -Filter {Name -like "Engineers_FullTime"} -Properties managedBy

# List all permissions
gpresult /V

# Locked out users
Search-ADAccount -LockedOut

# Unlock user
Unlock-ADAccount -Identity <username>

# Get local administrators
Get-LocalGroupMember administrators

# Get AD user details
Get-ADUser -Filter 'Name -like "<Name>"' -Properties Name, Title, Department | Format-Table Name, Title, Department

# Count users in division
(Get-Aduser -filter {division -eq "Software & Technology" -and enabled -eq "true"}).count
```

---

## Package Management

```powershell
# Update NuGet packages
Update-Package -reinstall

# Update PowerShell modules
Update-Module
```

---

## Windows Features

```powershell
# List IIS features
Get-WindowsOptionalFeature -Online | Where FeatureName -like 'IIS-*'

# Disable IIS Directory Browsing
Disable-WindowsOptionalFeature -Online -FeatureName IIS-DirectoryBrowsing

# Enable IIS Hostable Web Core
Enable-WindowsOptionalFeature -Online -FeatureName IIS-HostAbleWebCore

# RSAT Capabilities
Get-WindowsCapability -Name RSAT* -Online | Select-Object -Property Name, State
Get-WindowsCapability -Name RSAT* -Online | Add-WindowsCapability –Online
```

---

## Headless Windows

```powershell
# Server configuration
sconfig
```

---

## Troubleshooting

### Disk

```powershell
Get-WmiObject -Class Win32_logicaldisk
```

---

## Hyper-V Management

```powershell
# Example: Create checkpoint
Get-VM -ComputerName <ComputerName> -Name <Name> | Checkpoint-VM -SnapshotName 20200930 | Get-VMCheckpoint -VMName <Name>

# Restart remote computer
Restart-Computer -ComputerName <ComputerName> -Authentication Default -Credential $cred -Force
```

---

## Cleanup Scripts

```batch
:: Clean Prefetch
cd "C:\Windows\Prefetch\"
del /s /q /F *.*
for /d %%i in (*) do rmdir /s /q "%%i"

:: Clean Temp
cd "C:\Windows\Temp\"
del /s /q /F *.*
for /d %%i in (*) do rmdir /s /q "%%i"

:: Clean SoftwareDistribution\Download
cd "C:\Windows\SoftwareDistribution\Download"
del /s /q /F *.*
for /d %%i in (*) do rmdir /s /q "%%i"
```
