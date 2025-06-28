# VS Code Mastery Guide 💻

## Overview

This guide covers VS Code features and extensions used in the Interactive Coding Challenges, from basic navigation to advanced debugging.

## 🔧 Essential Features

### File Navigation

```bash
# Quick file open
Ctrl+P (Cmd+P on Mac)

# Go to line
Ctrl+G (Cmd+G on Mac)

# Find in files
Ctrl+Shift+F (Cmd+Shift+F on Mac)

# Command palette
Ctrl+Shift+P (Cmd+Shift+P on Mac)
```

### Source Control Panel

- **Open**: `Ctrl+Shift+G` (Cmd+Shift+G on Mac)
- **Stage Changes**: Click `+` next to files
- **Commit**: Enter message and press `Ctrl+Enter`
- **Branch Switching**: Click branch name in status bar
- **View Changes**: Click on modified files

### Integrated Terminal

```bash
# Open terminal
Ctrl+` (Cmd+` on Mac)

# New terminal
Ctrl+Shift+` (Cmd+Shift+` on Mac)

# Split terminal
Ctrl+Shift+5 (Cmd+Shift+5 on Mac)
```

## 🐛 Debugging Features

### Breakpoints

- **Set Breakpoint**: Click in gutter next to line number
- **Conditional Breakpoint**: Right-click breakpoint → Edit Breakpoint
- **Logpoint**: Right-click breakpoint → Add Logpoint

### Debug Panel

```json
// launch.json configuration
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Debug Current File",
      "type": "node",
      "request": "launch",
      "program": "${file}",
      "console": "integratedTerminal"
    }
  ]
}
```

### Watch Panel

- Add variables to watch during debugging
- Monitor expressions and values
- Track variable changes in real-time

## 👥 Live Share Extension

### Starting a Session

1. Install Live Share extension
2. Click "Live Share" button in status bar
3. Share the generated link with teammates
4. Team members join via link

### Collaboration Features

- **Real-time editing**: See teammates' cursors
- **Follow mode**: Follow a teammate's navigation
- **Chat**: Built-in chat for communication
- **Terminal sharing**: Shared terminal sessions
- **Port forwarding**: Share local servers

### Best Practices

- **Communication**: Use chat for coordination
- **Role clarity**: Each person has specific responsibilities
- **File organization**: Keep shared files organized
- **Backup**: Save work frequently

## 🔌 Essential Extensions

### Git Integration

- **GitLens**: Enhanced Git capabilities
- **Git History**: Visual Git history
- **Git Graph**: Branch visualization

### Language Support

- **Python**: Python language support
- **JavaScript**: JS/TS language support
- **Java**: Java development tools
- **C/C++**: C/C++ language support

### Productivity

- **Auto Rename Tag**: HTML tag renaming
- **Bracket Pair Colorizer**: Visual bracket matching
- **Indent Rainbow**: Visual indentation
- **Path Intellisense**: File path autocomplete

### Themes and Icons

- **Material Icon Theme**: File type icons
- **One Dark Pro**: Popular dark theme
- **Dracula**: Dark theme with good contrast

## ⌨️ Keyboard Shortcuts

### Navigation

```bash
# Quick open
Ctrl+P

# Go to symbol
Ctrl+T

# Go to line
Ctrl+G

# Find references
Shift+F12

# Go to definition
F12
```

### Editing

```bash
# Multi-cursor
Alt+Click

# Select all occurrences
Ctrl+Shift+L

# Move line up/down
Alt+Up/Down

# Duplicate line
Shift+Alt+Down

# Comment/uncomment
Ctrl+/
```

### File Management

```bash
# New file
Ctrl+N

# Save
Ctrl+S

# Save all
Ctrl+K S

# Close file
Ctrl+W

# Close all
Ctrl+K W
```

## 🔍 Search and Replace

### Find in Files

```bash
# Open search
Ctrl+Shift+F

# Use regex
Alt+R

# Match case
Alt+C

# Match whole word
Alt+W
```

### Replace

```bash
# Replace in current file
Ctrl+H

# Replace in files
Ctrl+Shift+H

# Replace all
Ctrl+Alt+Enter
```

## 📁 Workspace Management

### Multi-root Workspaces

```json
// workspace.code-workspace
{
  "folders": [
    {
      "name": "Frontend",
      "path": "./frontend"
    },
    {
      "name": "Backend",
      "path": "./backend"
    }
  ],
  "settings": {
    "files.exclude": {
      "**/node_modules": true
    }
  }
}
```

### Task Configuration

```json
// tasks.json
{
  "version": "2.0.0",
  "tasks": [
    {
      "label": "Run Tests",
      "type": "shell",
      "command": "npm test",
      "group": "test"
    }
  ]
}
```

## 🎯 Challenge-Specific Features

### For Live Share Relay Race

- **Live Share**: Real-time collaboration
- **Chat**: Non-verbal communication
- **Follow mode**: Coordinate handoffs
- **Terminal sharing**: Shared command execution

### For Debugger Duel Arena

- **Breakpoints**: Strategic debugging
- **Watch panel**: Variable monitoring
- **Call stack**: Function trace
- **Debug console**: Expression evaluation

### For Extension Expedition

- **Extensions panel**: Browse and install
- **Extension marketplace**: Discover new tools
- **Extension settings**: Configure behavior
- **Extension commands**: Access new features

## ⚙️ Settings and Configuration

### User Settings

```json
// settings.json
{
  "editor.fontSize": 14,
  "editor.tabSize": 2,
  "editor.insertSpaces": true,
  "editor.wordWrap": "on",
  "files.autoSave": "afterDelay",
  "terminal.integrated.fontSize": 12
}
```

### Workspace Settings

- Project-specific configurations
- Override user settings
- Share settings with team
- Environment-specific settings

## 🔧 Troubleshooting

### Common Issues

- **Extension conflicts**: Disable conflicting extensions
- **Performance issues**: Disable heavy extensions
- **Git integration**: Check Git installation
- **Terminal problems**: Reset terminal settings

### Reset Settings

```bash
# Reset user settings
# Delete settings.json file

# Reset workspace
# Delete .vscode folder

# Reinstall extensions
# Uninstall and reinstall problematic extensions
```

## 📚 Additional Resources

### Official Documentation

- [VS Code Documentation](https://code.visualstudio.com/docs)
- [Extension API](https://code.visualstudio.com/api)
- [Keyboard Shortcuts](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)

### Community Resources

- [VS Code Marketplace](https://marketplace.visualstudio.com/vscode)
- [VS Code Tips](https://github.com/Microsoft/vscode-tips-and-tricks)
- [Extension Recommendations](https://marketplace.visualstudio.com/search?target=VSCode&category=All%20categories&sortBy=Rating)

---

**Master VS Code and enhance your development workflow! 🚀**
