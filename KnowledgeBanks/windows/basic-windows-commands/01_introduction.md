# Windows OS Fundamentals & Interfaces

## Windows OS Versions

**Desktop Versions**:
- Windows 10: Support will end October 14, 2025
- Windows 11: Latest consumer version, TPM 2.0 required
- Windows 10/11 Pro: Business features, domain join, BitLocker
- Windows 10/11 Enterprise: Volume licensing, advanced management

**Server Versions**:
- Windows Server 2022: Stable enterprise server - support end October 13, 2026
- Windows Server 2025: Latest server version
- Windows Server Core: Command-line only, smaller footprint

**Legacy**:
- Windows 7: End of support 2020
- Windows 8/8.1: Discontinued
- Windows XP: End of support 2014

## Windows Registry

Centralized database storing system and application configuration.

**Structure**:
- `HKEY_LOCAL_MACHINE` (HKLM) - System-wide settings
- `HKEY_CURRENT_USER` (HKCU) - Current user settings
- `HKEY_CLASSES_ROOT` (HKCR) - File associations
- `HKEY_USERS` (HKU) - All user profiles
- `HKEY_CURRENT_CONFIG` (HKCC) - Hardware profiles

**Access**: Run `regedit.exe`

**Data Types**:
- REG_SZ: String value
- REG_DWORD: 32-bit number
- REG_BINARY: Binary data

## File System Layout

**Drive Letters**:
- `C:` - Primary system drive
- `D:`, `E:`, `F:` - Additional drives/partitions
- Network drives can use any available letter

**Key Directories**:
- `C:\Windows` - Operating system files
- `C:\Program Files` - 64-bit applications
- `C:\Program Files (x86)` - 32-bit applications on 64-bit systems
- `C:\Users` - User profiles and data
- `C:\Users\%USERNAME%` - Current user's profile
- `C:\Users\%USERNAME%\Desktop` - Desktop files
- `C:\Users\%USERNAME%\Documents` - User documents
- `C:\Users\%USERNAME%\Downloads` - Downloaded files
- `C:\Users\Public` - Shared files for all users
- `C:\ProgramData` - Application data (hidden)
- `C:\Temp` or `C:\Windows\Temp` - Temporary files

## Windows vs Linux Differences

**File Paths**:
- Windows: `C:\Users\user\file.txt` (backslashes)
- Linux: `/home/user/file.txt` (forward slashes)

**Case Sensitivity**:
- Windows: `File.txt` and `file.txt` are the same
- Linux: Different files

**Drive Structure**:
- Windows: Multiple drive letters (C:, D:, E:)
- Linux: Single unified tree from `/`

**File Permissions**:
- Windows: NTFS permissions, ACLs
- Linux: Simple read/write/execute for owner/group/others

**Software Installation**:
- Windows: .exe/.msi installers, Windows Store
- Linux: Package managers

**Hidden Files**:
- Windows: Hidden attribute, show with folder options
- Linux: Files starting with `.`

## GUI Interface

### Start Menu
- Windows key or click Start button
- Search for applications/files
- Recently used programs
- All apps list
- Power options (shutdown, restart, sleep)

### Control Panel vs Settings
**Control Panel** (legacy):
- `control` or `appwiz.cpl` from Run
- Programs and Features
- System and Security
- Network and Internet

**Settings** (modern):
- Windows key + I
- System settings
- Apps and features
- Update and Security
- Accounts

### File Explorer
- Windows key + E
- Navigate drives and folders
- Address bar shows current path
- Quick access to common folders
- Right-click context menus

## Command-Line Shells

### CMD (Command Prompt)
Legacy command interpreter.

**Open CMD**:
- `cmd` in Start Menu
- Windows key + R, type `cmd`
- Shift + right-click folder, "Open command window here"

**Basic Commands**:
- `dir` - List directory contents
- `cd` - Change directory
- `md` or `mkdir` - Make directory
- `rd` or `rmdir` - Remove directory
- `copy` - Copy files
- `del` - Delete files
- `type` - Display file contents

### PowerShell
Modern shell with object-oriented scripting.

**Open PowerShell**:
- `powershell` in Start Menu
- Windows key + X, select PowerShell
- Shift + right-click folder, "Open PowerShell window here"

**Basic Commands**:
- `Get-ChildItem` (alias: `ls`, `dir`) - List items
- `Set-Location` (alias: `cd`) - Change directory
- `New-Item` - Create files/directories
- `Copy-Item` - Copy files
- `Remove-Item` - Delete files
- `Get-Content` - Display file contents

## Lab Environment Setup

**Virtual Machine Options**:
- VMware Workstation/Player
- VirtualBox (free)
- Hyper-V (Windows Pro/Enterprise)

**ISO Download**:
- Microsoft Evaluation Center
- Windows Media Creation Tool
- Volume Licensing Service Center (enterprise)

**Basic VM Specs**:
- 4GB RAM minimum (8GB recommended)
- 60GB disk space
- Enable virtualization in BIOS

## Basic Navigation

### File Explorer Navigation
- Address bar: `C:\Users\%USERNAME%`
- Breadcrumb navigation
- Up arrow to parent directory
- Forward/back buttons

### Command-Line Navigation

**Change Directory**:
```cmd
cd C:\Users
cd Documents
cd ..
cd \
```

**List Contents**:
```cmd
dir
dir /a (show hidden files)
dir *.txt (show only .txt files)
```

**Switch Drives**:
```cmd
C:
D:
E:
```

**Full Path Navigation**:
```cmd
cd /d D:\Projects
cd /d "C:\Program Files"
```

**PowerShell Navigation**:
```powershell
Set-Location C:\Users
Get-ChildItem
Set-Location -Path "D:\Projects"
```

## Drive Switching Examples

**CMD**:
```cmd
C:\Users\john> D:
D:\> dir
D:\> C:
C:\Users\john>
```

**PowerShell**:
```powershell
PS C:\Users\john> Set-Location D:\
PS D:\> Get-ChildItem
PS D:\> Set-Location C:\
PS C:\>
```

**File Explorer**:
- Click drive letters in left panel
- Type drive letter in address bar: `D:`
- Use This PC to see all drives