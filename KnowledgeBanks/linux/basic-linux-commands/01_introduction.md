# Linux OS Fundamentals & Interfaces

## Linux Kernel vs Distributions

**Kernel**: Core system component. Manages hardware, memory, processes, device drivers. Small and focused.

**Distribution**: Complete OS built around Linux kernel. Includes kernel + software packages + desktop environment + package manager + tools.

Common distros:
- Ubuntu: Beginner-friendly, desktop-focused
- Fedora: Cutting-edge features, developer-oriented
- Debian: Stable, free software focus
- CentOS: Enterprise, server-focused

## Unified Filesystem

Single tree structure starting at `/` (root). No drive letters like Windows C:, D:.

Key directories:
- `/` - Root directory
- `/home` - User directories
- `/etc` - Configuration files
- `/usr` - User programs
- `/var` - Variable data (logs, temp files)
- `/bin` - Essential programs
- `/lib` - Shared libraries
- `/dev` - Device files
- `/proc` - Process information
- `/sys` - Kernel/hardware info

External storage mounts into this tree (usually `/mnt` or `/media`).

## CLI vs GUI

**CLI (Command Line Interface)**:
- Terminal/shell access
- Default shell: Bash
- Direct system control
- Automation and scripting
- Remote administration

**GUI (Graphical Interface)**:
- Desktop environments: GNOME, KDE, XFCE
- Windows, menus, icons
- Mouse-driven
- Terminal still accessible and commonly used

## Linux vs Windows Differences

**File Paths**:
- Linux: `/home/user/file.txt` (forward slashes)
- Windows: `C:\Users\user\file.txt` (backslashes)

**Case Sensitivity**:
- Linux: `File.txt` and `file.txt` are different
- Windows: Same file

**Software Installation**:
- Linux: Package managers (apt, dnf, yum)
- Windows: Download and run installers

**File Permissions**:
- Linux: Read/write/execute for owner/group/others
- Windows: Basic permissions

## Ubuntu Overview

- Based on Debian
- GNOME desktop default
- Package manager: APT
  - `apt install package`
  - `apt update`
  - `apt upgrade`
- Terminal: Ctrl+Alt+T
- Includes Firefox, LibreOffice
- 6-month release cycle

## Fedora Overview

- Community-driven
- GNOME desktop default
- Package manager: DNF
  - `dnf install package`
  - `dnf update`
  - `dnf search package`
- Latest software versions
- Developer tools included
- 6-month release cycle

## Text Editors

### Nano
Simple editor with on-screen shortcuts.

Open file: `nano filename.txt`

Controls:
- `Ctrl+X` - Exit
- `Ctrl+O` - Save
- `Ctrl+W` - Search
- `Ctrl+K` - Cut line
- `Ctrl+U` - Paste
- `Ctrl+G` - Help

### Vim
Modal editor. Command mode vs insert mode.

Open file: `vim filename.txt`

Modes:
- Command mode (default)
- Insert mode (press `i`)
- Return to command mode (press `Esc`)

Commands:
- `:w` - Save
- `:q` - Quit
- `:wq` - Save and quit
- `:q!` - Quit without saving

Navigation (command mode):
- `h,j,k,l` - Left, down, up, right
- `w` - Next word
- `b` - Previous word
- `0` - Start of line
- `$` - End of line