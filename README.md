# 🕹️ PS3 CFW USB Creator — RetroTechModding.de

> **Custom Firmware USB Stick Creator for PlayStation 3**  
> Create a bootable PS3 CFW USB stick in just a few clicks — with all essential Homebrew tools included.

![Windows](https://img.shields.io/badge/Platform-Windows%2010%2F11-blue?logo=windows)
![.NET 8](https://img.shields.io/badge/.NET-8.0-purple?logo=dotnet)
![License](https://img.shields.io/badge/License-Freeware-green)
![Language](https://img.shields.io/badge/Languages-18-cyan)

---

## ✨ Features

- **4 CFW Variants** — PEX, PEX noBD, PEX noBT, PEX noBD+noBT
- **18 Languages** — DE, EN, FR, ES, IT, PT, NL, RU, PL, JA, KO, ZH-Hans, ZH-Hant, TR, SV, DA, NO, FI
- **Automatic FAT32 Formatting** (MBR) with safety confirmation
- **14 Pre-installed Homebrew PKGs** — webMAN MOD, multiMAN, IRISMAN, RetroArch, Apollo, and more
- **Safe Eject** of USB stick after creation
- **Admin Rights** automatically requested
- **Error Logging** for troubleshooting

---

## 📥 Download & Installation

### Requirements
- **Windows 10/11** (64-Bit)
- **.NET 8 Desktop Runtime** — [Download here](https://dotnet.microsoft.com/download/dotnet/8.0)
- **USB Stick** with at least 8 GB (FAT32 compatible)

### Installation
1. **Download ZIP/RAR**
2. **Extract** to any folder
3. **Double-click** `PS3CFWUSBAIOCreator.exe` (or the shortcut)
4. Done!

> ⚠️ **Important:** Extract the folder completely! Do not run directly from the ZIP.

---

## 🎮 Usage

### Step 1: Choose CFW Variant
| Variant | Description |
|---|---|
| **CFW PEX** | Standard — all features enabled |
| **CFW PEX noBD** | For PS3 without or with defective Blu-ray drive |
| **CFW PEX noBT** | For PS3 without or with defective Bluetooth module |
| **CFW PEX noBD+noBT** | For PS3 without or with defective BD drive AND Bluetooth |

### Step 2: Select USB Stick
- Plug in your USB stick
- Select the correct drive from the dropdown
- Press 🔄 to refresh the list if needed

### Step 3: Create USB Stick
- Click **CREATE USB STICK**
- Confirm the safety prompt
- Wait until the process is complete
- Optional: Safely eject the USB stick

> ⚠️ **WARNING:** All data on the USB stick will be permanently deleted!

---

## 📦 Included Homebrew Packages (PKGs)

| Package | Description | Developer |
|---|---|---|
| **webMAN MOD** | FTP/File Manager & Fan Control | @aldostools |
| **multiMAN** | Backup Manager | @deank |
| **IRISMAN** | ISO Manager | @aldostools |
| **RetroArch CE** | Multi-Emulator Frontend | psx-place.com |
| **Apollo PS3** | Save Game Tool | @bucanero |
| **Artemis PS3 GUI** | Cheat/Save Manager | @bucanero |
| **PKGi** (Part 1 & 2) | PKG Installer | @bucanero |
| **PlayStation Network DB** | PSN Database | @luanteles |
| **PS2CONFIG** | PS2 Emulator Configuration | — |
| **PSP Minis Launcher** | PSP Minis Launcher | — |
| **PSP Remasters Launcher** | PSP Remaster Launcher | — |
| **Cover Databases** | Cover Art for Games | — |

---

## 🌐 Supported Languages

| 🇩🇪 Deutsch | 🇬🇧 English | 🇫🇷 Français | 🇪🇸 Español | 🇮🇹 Italiano | 🇧🇷 Português |
|---|---|---|---|---|---|
| 🇳🇱 Nederlands | 🇷🇺 Русский | 🇵🇱 Polski | 🇯🇵 日本語 | 🇰🇷 한국어 | 🇨🇳 简体中文 |
| 🇹🇼 繁體中文 | 🇹🇷 Türkçe | 🇸🇪 Svenska | 🇩🇰 Dansk | 🇳🇴 Norsk | 🇫🇮 Suomi |

> 🤖 Translations (except DE/EN) were AI-assisted (Claude, Anthropic)

---

## 🔧 For Developers

### Build the Project
```bash
# Debug
dotnet build

# Release
dotnet build -c Release

# Single-File EXE (self-contained)
dotnet publish -c Release -r win-x64 --self-contained true -p:PublishSingleFile=true
```

### Project Structure
```
PS3CFWUSBAIO/
├── PS3CFWUSBAIOCreator.exe      # Shortcut to exe
└── Resources/
    ├── CFW_Varianten/           # CFW PUP files
    │   ├── CFW_PEX/
    │   ├── CFW_PEX_noBD/
    │   ├── CFW_PEX_noBT/
    │   └── CFW_PEX_noBD_noBT/
    ├── PKG_Files/               # Homebrew PKG files
    ├── Helpers/                 # C# Helper classes
    ├── Localization/            # Multi-language support
    ├── Models/                  # Data models
    ├── MainWindow.xaml          # UI (WPF/XAML)
    ├── MainWindow.xaml.cs       # UI logic
    └── PS3USBCreator.csproj     # Project file
```

### Tech Stack
- **WPF** (.NET 8, Windows Desktop)
- **C#** 12
- **System.Management** (WMI for USB detection)
- **diskpart** (FAT32 formatting)

---

## ❓ FAQ

**Q: Do I need .NET installed?**  
A: Yes, the [.NET 8 Desktop Runtime](https://dotnet.microsoft.com/download/dotnet/8.0) must be installed. Alternatively, a self-contained .exe can be built (see Developer section).

**Q: Why is my USB stick not detected?**  
A: Make sure the stick is plugged in and press 🔄. Only removable drives are shown.

**Q: Can I update the CFW files myself?**  
A: Yes! Simply replace the `PS3UPDAT.PUP` in the respective `CFW_Varianten/` subfolders.

**Q: The app won't start?**  
A: Right-click → "Run as Administrator". The app requires admin rights for USB formatting.

**Q: Will my data be deleted?**  
A: Yes — the USB stick will be completely formatted (FAT32, MBR). Back up all important data beforehand!

---

## 🙏 Credits & Acknowledgments

- **CFW PEX** — [EvilNat](https://twitter.com/xXEvilnatXx) (Custom Firmware)
- **webMAN MOD / IRISMAN** — [@aldostools](https://github.com/aldostools)
- **Apollo / Artemis / PKGi** — [@bucanero](https://github.com/bucanero)
- **multiMAN** — [@deank](https://twitter.com/deaborern)
- **RetroArch CE** — [psx-place.com](https://www.psx-place.com)
- **PSN Database** — [@luanteles](https://github.com/luanteles)
- **PS3 Homebrew Community** — For years of dedication and passion 💜

---

## 📄 License

This tool is **Freeware** and may be freely used and distributed.  
The included Homebrew packages are subject to the respective licenses of their developers.

---

## 🔗 Links

- 🌐 **Website:** [RetroTechModding.de](https://retrotechmodding.de)
- 🛒 **Shop:** [RetroTechModding.de Shop](https://retrotechmodding.de)
- 💬 **Support:** Via GitHub Issues or the website

---

<p align="center">
  <strong>Made with 💜 by RetroTechModding.de</strong><br>
  <em>Cyberpunk UI powered by Claude (Anthropic) 🤖</em>
</p>
