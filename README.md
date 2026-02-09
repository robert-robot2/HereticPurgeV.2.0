# HereticPurge v2.0

A professional Windows Forms utility for cleaning `bin` and `obj` folders from .NET projects.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![.NET](https://img.shields.io/badge/.NET-10.0-purple.svg)
![Platform](https://img.shields.io/badge/platform-Windows-lightgrey.svg)

## 🎯 Features

### 📁 Project Path Management
- **Visual path list** with validation status indicators (✓ Valid / ✗ Invalid)
- **Browse for folders** with integrated folder picker dialog
- **Drag-and-drop** folders directly from Windows Explorer
- **Add, remove, and clear** paths with one click
- **Multi-select support** for bulk operations
- **Right-click context menu** with quick actions:
  - Open in Explorer
  - Copy path to clipboard
  - Remove from list
- **Double-click** any path to open it in Windows Explorer

### 🗑️ Smart Purging
- **Selective purge filters** - choose to delete:
  - `bin` folders only
  - `obj` folders only
  - Both `bin` and `obj` folders
- **Real-time progress dialog** with live console-style logging
- **Color-coded output** for easy reading:
  - Cyan: Project headers
  - Yellow: Folders found
  - Green: Successful deletions
  - Red: Errors
- **Detailed statistics**:
  - Total folders deleted
  - Space freed (B/KB/MB/GB auto-formatting)
  - Error count
- **Confirmation dialog** before destructive operations
- **Async operation** - UI remains responsive during purge

### 🔍 Project Discovery
- **Search for Projects** - recursively scan any folder for `.csproj` files
- Automatically adds all found project directories
- Shows summary of projects found, added, and skipped
- Perfect for workspace cleanup or batch adding projects

### 📊 Preview & Analysis
- **Preview Purge Statistics** - see what will be deleted WITHOUT deleting
- Calculates total folder count and size before purging
- Respects your selected filter options (bin/obj)
- No commitment - just information

### 💾 Data Persistence
- **Auto-save** project paths to JSON configuration
- **Auto-load** paths on application startup
- Config location: `%AppData%\HereticPurge\config.json`
- Smart filtering removes invalid paths on load
- Manual save option available in File menu

### ⌨️ Keyboard Shortcuts
| Shortcut | Action |
|----------|--------|
| **Enter** | Add path from text box |
| **Delete** | Remove selected path(s) |
| **F5** | Refresh path validation |
| **Ctrl+S** | Save paths manually |

### 🎨 User Interface
- **Modern, clean design** with professional color scheme
- **Tooltips on all controls** for helpful hints
- **Status bar** with real-time feedback on all actions
- **Menu bar** with organized File, Tools, and Help menus
- **Resizable window** with enforced minimum size
- **Validation indicators** - instantly see which paths exist

### 🛠️ Advanced Features
- **Path validation** - auto-detects missing or invalid folders
- **Refresh validation** - re-check all paths with one click
- **Remove invalid** - bulk remove all missing paths
- **Multi-path clipboard** - copy one or many paths at once
- **Error resilience** - continues purging even if individual folders fail
- **Comprehensive logging** - see exactly what happened

## 🚀 Getting Started

### Prerequisites
- Windows OS
- .NET 10.0 Runtime (or SDK for building from source)

### Installation
1. Download the latest release
2. Extract and run `HereticPurge.exe`
3. No installation required - portable application

### Usage
1. **Add project paths** using one of these methods:
   - Type or paste path and click "Add Path"
   - Click "Browse..." to select a folder
   - Drag folders from Windows Explorer
   - Use "Search for Projects..." to auto-discover
2. **Choose what to purge** - check `bin` and/or `obj` boxes
3. **(Optional) Preview** - Tools → Preview Purge Statistics
4. **Click "PURGE"** - confirm and watch it work!
5. **Done!** - Your paths are saved for next time

## 📋 Use Cases

- **Clean development workspace** - remove all build artifacts from multiple projects
- **Free up disk space** - bin/obj folders can consume gigabytes
- **Pre-commit cleanup** - ensure no build artifacts in version control
- **CI/CD preparation** - clean slate before builds
- **Project migration** - clean old projects before archiving

## 🔧 Technical Details

### Built With
- **.NET 10.0** - Modern .NET framework
- **Windows Forms** - Native Windows UI
- **System.Text.Json** - Configuration persistence
- **Async/Await** - Responsive UI during operations

### Architecture
- Clean separation of concerns (UI vs business logic)
- Thread-safe UI updates with proper Invoke patterns
- Comprehensive error handling and logging
- File size calculation with overflow protection

## 📝 Configuration

Configuration is automatically stored at:
```
%AppData%\HereticPurge\config.json
```

You can:
- View config location: Help → About
- Open config folder: File → Open Config Folder
- Manually edit JSON if needed

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

## 📄 License

This project is licensed under the MIT License.

## 🙏 Acknowledgments

- Built to solve real developer pain points
- Evolved from simple console app to full-featured GUI
- Community-driven feature development

---

**Made with ❤️ for developers who hate disk clutter**
