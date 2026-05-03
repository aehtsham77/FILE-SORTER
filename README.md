<div align="center">

<img src="https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/GUI-Tkinter-FF6F00?style=for-the-badge&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Version-3.0.0-3498db?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey?style=for-the-badge"/>

<br/><br/>

```
 ███████╗██╗██╗     ███████╗    ███████╗ ██████╗ ██████╗ ████████╗███████╗██████╗
 ██╔════╝██║██║     ██╔════╝    ██╔════╝██╔═══██╗██╔══██╗╚══██╔══╝██╔════╝██╔══██╗
 █████╗  ██║██║     █████╗      ███████╗██║   ██║██████╔╝   ██║   █████╗  ██████╔╝
 ██╔══╝  ██║██║     ██╔══╝      ╚════██║██║   ██║██╔══██╗   ██║   ██╔══╝  ██╔══██╗
 ██║     ██║███████╗███████╗    ███████║╚██████╔╝██║  ██║   ██║   ███████╗██║  ██║
 ╚═╝     ╚═╝╚══════╝╚══════╝    ╚══════╝ ╚═════╝ ╚═╝  ╚═╝   ╚═╝   ╚══════╝╚═╝  ╚═╝
```

### **Professional Desktop File Organizer — Built with Python & Tkinter**

*Sort by type · Sort by date · Sort by size · Scan duplicates · Undo anything*

<br/>

</div>

---

## 📌 Overview

**File Sorter Pro** is a full-featured desktop application that automatically organizes the files in any directory. Instead of manually dragging files into folders, you point File Sorter Pro at a directory and it handles everything — sorting into clean category folders, filtering by date or size, finding duplicates, and even letting you reverse the entire operation with one click.

Built entirely with the Python standard library — **no pip installs required**.

---

## ✨ Features

### 🗂️ Four Sort Modes
| Mode | What it creates |
|------|----------------|
| **By File Type** | `Images/` `Documents/` `Videos/` `Audio/` `Programs/` `Compressed/` `Code/` `Fonts/` `Other/` |
| **By Date Modified** | `Today/` `Last 7 Days/` `Last 30 Days/` `Last 6 Months/` `Last Year/` `Older Than 1 Year/` |
| **By File Size** | `Tiny (< 1 MB)/` `Small (1–50 MB)/` `Medium (50–500 MB)/` `Large (500 MB–1 GB)/` `Huge (> 1 GB)/` |
| **By Extension** | One folder per extension — `PDF/` `MP4/` `PY/` etc. |

### 🔍 Smart Filters
- **Date filter** — preset ranges (Today / Last 7 Days / Last 30 Days / Last 6 Months / Last Year / Older) **or** a custom `YYYY-MM-DD` from/to range
- **Size filter** — custom Min MB / Max MB values, stackable with any sort mode

### 🛡️ Duplicate Management
- Built-in **Duplicate Scanner** tab — detects files sharing the same name + size
- Select and delete duplicates directly from the UI
- Five **collision strategies** when a filename already exists at the destination:

  | Strategy | Behaviour |
  |----------|-----------|
  | Keep Both (rename) | Adds `_1`, `_2` … suffix — **default** |
  | Keep Newer | Overwrites only if source is more recent |
  | Keep Older | Overwrites only if source is older |
  | Keep Larger | Overwrites only if source is bigger |
  | Skip | Leaves the file untouched |

### 🔄 Safety & Control
- **Dry Run** — full preview of every move with zero files touched
- **Undo Last Sort** — reverses every file move from the previous run
- **Stop button** — halt mid-sort at any time
- **Recursive mode** — optionally descend into sub-folders
- **Skip hidden files** — ignores dot-files by default

### 📊 Live Statistics
- Real-time progress bar and activity log
- Statistics tab with **four chart views**: Categories · File Extensions · Size Ranges · Date Buckets
- Summary panel: total files, processed, skipped, errors, total size moved, success rate

### 🎨 UI & Themes
- Four built-in colour themes: **Professional · Corporate · Dark Pro · Elegant**
- **Explorer tab** — browsable folder tree with file sizes and modified dates
- **Menu bar** with keyboard-accessible actions

---

## 🚀 Getting Started

### Prerequisites

- Python **3.10 or higher**
- `tkinter` — ships with the standard CPython installer on Windows and macOS.  
  On Linux (Debian/Ubuntu) install it with:

  ```bash
  sudo apt install python3-tk
  ```

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/aehtsham77/file-sorter-pro.git
cd file-sorter-pro

# 2. (Optional) create a virtual environment
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate

# 3. Run — no extra dependencies needed
python file_sorter_v3.py
```

> **Windows users:** you can also double-click `file_sorter_v3.py` if Python is associated with `.py` files.

### Optional — build a standalone executable

```bash
pip install pyinstaller
pyinstaller --onefile --windowed file_sorter_v3.py
# Output: dist/file_sorter_v3.exe  (or dist/file_sorter_v3 on macOS/Linux)
```

---

## 🗺️ Usage Guide

### Basic workflow
1. Launch the app
2. **Browse** to the folder you want to organise
3. Switch to **Sort Options** and pick a sort mode + any filters
4. Return to **Main** and click **▶ Start Sorting**
5. Watch the live log — or switch to **Statistics** for charts

### Before you commit to a real folder
Enable **Dry Run** in Sort Options. Every planned move is logged without touching a single file.

### Made a mistake?
Click **↩ Undo Last Sort** on the Main tab to move every file back to its original location.

### Finding & removing duplicates
1. Select a directory
2. Open the **Duplicates** tab
3. Click **🔍 Scan for Duplicates**
4. Select the copies you want to remove and click **🗑 Delete Selected Dupes**

---

## 📁 Project Structure

```
file-sorter-pro/
├── file_sorter_v3.py      # Main application (single file, no dependencies)
├── README.md
├── LICENSE
└── docs/
    └── screenshots/       # UI screenshots for README
```

---

## 🗺️ Roadmap

- [ ] **Scheduled sorting** — run automatically at a set time or on a folder-watch trigger
- [ ] **Rule builder** — custom rules like "files containing 'invoice' → Finance/"
- [ ] **Cloud sync** — push sorted folders to Google Drive / OneDrive
- [ ] **CSV export** — export the activity log and statistics as a spreadsheet
- [ ] **Context menu integration** — right-click any folder in Windows Explorer to sort it
- [ ] **Dark mode auto-detect** — follow OS light/dark preference on launch
- [ ] **Localisation** — UI strings in Urdu, Arabic, Spanish, French

---

## ⚙️ How It Works

File Sorter Pro is intentionally **zero-dependency** — it relies only on modules that ship with CPython:

| Module | Used for |
|--------|----------|
| `os` / `shutil` | File scanning, moving, stat retrieval |
| `pathlib` | Cross-platform path handling |
| `tkinter` | Entire GUI — windows, tabs, widgets, canvas charts |
| `threading` | Keeps the UI responsive while sorting runs in the background |
| `collections.defaultdict` | Live stats aggregation |
| `datetime` | Date bucket calculations and log timestamps |

The sort engine works in three steps on every file:
1. **Filter** — checks date and size constraints; skips the file if it fails
2. **Bucket** — maps the file to a destination folder based on the chosen sort mode
3. **Move** — applies the selected collision strategy, moves the file, records the action in the undo log

---

## 📋 Changelog

### v3.0.0 — May 2025
- ✅ Added **By Date**, **By Size**, and **By Extension** sort modes
- ✅ Date filter with presets + custom from/to range
- ✅ Size filter with custom Min/Max MB values
- ✅ **Duplicate Scanner** tab with selective deletion
- ✅ Five collision/duplicate strategies (rename, keep newer/older/larger, skip)
- ✅ **Dry Run** preview mode — zero files touched
- ✅ **Undo Last Sort** — full reversal of any completed run
- ✅ Recursive mode and skip-hidden-files toggle
- ✅ Statistics charts for Categories, Extensions, Sizes, Dates
- ✅ Explorer tab now shows file sizes and modified dates
- ✅ Added **Code** and **Fonts** file categories

### v2.0.0
- ✅ Sort by file type into named category folders
- ✅ Files keep original names — no renaming
- ✅ Numeric suffix on name collision
- ✅ Live progress bar and activity log

### v1.0.0
- Initial release — sorted files into date-named folders

---

## ❓ FAQ

**Q: Will it delete any of my files?**
A: No. The app only *moves* files between folders within the directory you select. The only exception is the Duplicate Scanner tab, which deletes only files you manually select and confirm.

**Q: Can I run it on a network drive or external USB?**
A: Yes, as long as Python can reach the path. Just browse to the drive in the directory picker.

**Q: What happens if the sort is interrupted halfway?**
A: Files already moved stay moved. Click **↩ Undo Last Sort** to reverse everything processed before the interruption.

**Q: Does it work on files inside sub-folders?**
A: Only if you enable **Recursive mode** in Sort Options. By default it only touches files directly inside the chosen folder.

**Q: A file ended up in "Other" — why?**
A: Its extension isn't in any built-in category list. Open a GitHub Issue to request it be added, or add it yourself in the `FILE_CATEGORIES` dict at the top of the script.

**Q: Can I build a `.exe` to share with non-technical users?**
A: Yes — see the PyInstaller instructions in the Getting Started section above.

---

## 🤝 Contributing

Contributions, issues and feature requests are welcome!

```bash
# Fork → clone your fork → create a branch
git checkout -b feature/your-feature-name

# Make changes, then commit
git commit -m "feat: describe your change"

# Push and open a Pull Request
git push origin feature/your-feature-name
```

Please keep PRs focused — one feature or fix per PR. Open an issue first for large changes so we can discuss the approach.

---

## 📄 License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for details.

---

## 👤 Author

**M. Aehtsham Nasir**

<a href="https://github.com/aehtsham77"><img src="https://img.shields.io/badge/GitHub-aehtsham77-181717?style=flat-square&logo=github"/></a>
<a href="https://www.linkedin.com/in/muhammad-aehtsham-nasir"><img src="https://img.shields.io/badge/LinkedIn-Muhammad%20Aehtsham%20Nasir-0A66C2?style=flat-square&logo=linkedin"/></a>

---

<div align="center">

⭐ **If this project saved you time, please give it a star!** ⭐

*Built with ❤️ and Python*

</div>
