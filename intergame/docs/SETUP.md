# Setup Guide 🚀

## Overview

This guide will help you set up the Interactive Coding Challenges environment for your team.

## 📋 Prerequisites

### Required Software

- **Git**: Version control system
- **VS Code**: Code editor with extensions
- **Linux Terminal**: Command line interface
- **Web Browser**: To view the presentation

### Recommended Extensions for VS Code

- **Live Share**: Real-time collaboration
- **GitLens**: Enhanced Git capabilities
- **Git History**: Visual Git history
- **Material Icon Theme**: File type icons
- **Auto Rename Tag**: HTML tag renaming
- **Bracket Pair Colorizer**: Visual bracket matching

## 🛠️ Installation Steps

### 1. Clone the Repository

```bash
git clone <repository-url>
cd interactive-coding-challenges
```

### 2. Install VS Code Extensions

```bash
# Install Live Share extension
code --install-extension ms-vsliveshare.vsliveshare

# Install GitLens
code --install-extension eamodio.gitlens

# Install Material Icon Theme
code --install-extension pkief.material-icon-theme
```

### 3. Configure Git (if not already done)

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### 4. Set Up Team Workspace

```bash
# Create a shared workspace directory
mkdir team-workspace
cd team-workspace

# Initialize a Git repository for challenges
git init
```

## 🎮 Running the Presentation

### Method 1: Direct Browser Opening

```bash
# Navigate to the repository
cd interactive-coding-challenges

# Open presentation in browser
open presentation.html  # macOS
xdg-open presentation.html  # Linux
start presentation.html  # Windows
```

### Method 2: Local Server (Recommended)

```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx http-server -p 8000

# Using PHP
php -S localhost:8000
```

Then open `http://localhost:8000/presentation.html` in your browser.

## 👥 Team Setup

### 1. Role Assignment

Each challenge requires exactly 3 team members with specific roles:

- **Navigator/Commander**: Strategic planning and coordination
- **Operator/Executor**: Hands-on implementation
- **Recorder/Analyst**: Documentation and analysis

### 2. Communication Setup

- **Voice/Video Call**: For real-time communication
- **Screen Sharing**: For coordination and guidance
- **Chat Application**: For text-based communication

### 3. Workspace Organization

```bash
# Create challenge-specific directories
mkdir challenge-01-dungeon-escape
mkdir challenge-02-code-heist
mkdir challenge-03-timebomb-defusal
# ... continue for all challenges
```

## 🔧 Challenge-Specific Setup

### For Repository Dungeon Escape (Challenge #1)

```bash
# Create a test repository with multiple branches
mkdir dungeon-repo
cd dungeon-repo
git init

# Create initial commit
echo "Welcome to the dungeon!" > README.md
git add README.md
git commit -m "Initial dungeon setup"

# Create puzzle branches
git checkout -b puzzle-1
echo "Puzzle piece 1: The key is hidden in the shadows" > puzzle1.txt
git add puzzle1.txt
git commit -m "Added first puzzle piece"

git checkout -b puzzle-2
echo "Puzzle piece 2: Ancient wisdom lies in the depths" > puzzle2.txt
git add puzzle2.txt
git commit -m "Added second puzzle piece"

git checkout -b puzzle-3
echo "Puzzle piece 3: Only together can you escape" > puzzle3.txt
git add puzzle3.txt
git commit -m "Added third puzzle piece"

# Return to main branch
git checkout main
```

### For The Great Code Heist (Challenge #2)

```bash
# Create a repository with a known bug
mkdir heist-repo
cd heist-repo
git init

# Create working code
echo "function calculate(a, b) { return a + b; }" > calculator.js
git add calculator.js
git commit -m "Add working calculator"

# Introduce bug in a later commit
echo "function calculate(a, b) { return a - b; }" > calculator.js
git add calculator.js
git commit -m "Update calculator logic"

# Create test file
echo "console.log(calculate(5, 3)); // Should be 8" > test.js
git add test.js
git commit -m "Add test case"
```

### For Terminal Timebomb Defusal (Challenge #3)

```bash
# Create bomb simulation files
mkdir bomb-simulation
cd bomb-simulation

# Create bomb stages
echo "Stage 1: Find the hidden file named 'detonator'" > stage1.txt
echo "Stage 2: Search for process 'countdown'" > stage2.txt
echo "Stage 3: Remove file 'explosive.txt'" > stage3.txt

# Create hidden files
echo "BOOM!" > detonator
echo "Ticking..." > explosive.txt

# Create defusal manual
cat > defusal-manual.txt << EOF
BOMB DEFUSAL MANUAL
==================

Stage 1: Find detonator file
Command: find . -name "detonator"

Stage 2: Check for countdown process
Command: ps aux | grep countdown

Stage 3: Remove explosive file
Command: rm explosive.txt

Final: Create DEFUSED.txt
Command: echo "BOMB DEFUSED" > DEFUSED.txt
EOF
```

## 📊 Monitoring and Tools

### System Monitoring Setup

```bash
# Install htop if not available
sudo apt-get install htop  # Ubuntu/Debian
brew install htop          # macOS
```

### Process Management

```bash
# Create test processes for challenges
while true; do echo "Test process"; sleep 5; done &
while true; do echo "Countdown process"; sleep 3; done &
```

## 🎯 Challenge Execution

### Before Each Challenge

1. **Review the scenario** with your team
2. **Assign roles** clearly
3. **Set up the environment** as specified
4. **Start the timer** when ready
5. **Begin the challenge**

### During the Challenge

1. **Stay in character** for your assigned role
2. **Communicate clearly** with teammates
3. **Follow the constraints** of your role
4. **Document progress** as required
5. **Monitor the timer**

### After Each Challenge

1. **Review the results** against success criteria
2. **Discuss what worked** and what didn't
3. **Share lessons learned**
4. **Prepare for the next challenge**

## 🔧 Troubleshooting

### Common Issues

#### Git Issues

```bash
# Reset repository if needed
git reset --hard HEAD
git clean -fd

# Fix merge conflicts
git status
git add resolved-file.txt
git commit -m "Resolve merge conflict"
```

#### VS Code Issues

```bash
# Reset VS Code settings
rm -rf ~/.vscode/settings.json

# Reinstall extensions
code --uninstall-extension extension-id
code --install-extension extension-id
```

#### Terminal Issues

```bash
# Check terminal permissions
ls -la /dev/tty*

# Reset terminal
reset

# Clear terminal history
history -c
```

### Performance Optimization

```bash
# Monitor system resources
htop
df -h
free -h

# Clean up if needed
sudo apt-get autoremove  # Ubuntu/Debian
brew cleanup             # macOS
```

## 📚 Additional Resources

### Documentation

- [Git Documentation](https://git-scm.com/doc)
- [VS Code Documentation](https://code.visualstudio.com/docs)
- [Linux Command Reference](https://www.gnu.org/software/bash/manual/)

### Community Support

- [GitHub Issues](https://github.com/your-repo/issues)
- [Stack Overflow](https://stackoverflow.com/)
- [VS Code Community](https://code.visualstudio.com/community)

---

**Ready to begin your coding adventure? Let's get started! 🚀**
