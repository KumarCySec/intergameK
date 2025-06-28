# Linux Terminal Mastery Guide 🐧

## Overview

This guide covers essential Linux terminal commands and tools used in the Interactive Coding Challenges, from basic navigation to advanced process management.

## 🔧 Basic Navigation

### File System Navigation

```bash
# List files and directories
ls
ls -la          # Show all files with details
ls -lh          # Human-readable file sizes
ls -t           # Sort by modification time

# Change directory
cd /path/to/directory
cd ..           # Go up one level
cd ~            # Go to home directory
cd -            # Go to previous directory

# Show current directory
pwd

# Create directories
mkdir directory_name
mkdir -p parent/child    # Create parent directories if needed
```

### File Operations

```bash
# Copy files
cp source destination
cp -r source_dir dest_dir    # Copy directories recursively

# Move/rename files
mv old_name new_name
mv file.txt /path/to/destination/

# Remove files
rm filename
rm -r directory              # Remove directory recursively
rm -f filename               # Force remove without confirmation

# Create files
touch filename               # Create empty file
echo "content" > filename    # Create file with content
cat > filename               # Interactive file creation
```

## 🔍 Search and Find

### Grep (Global Regular Expression Print)

```bash
# Basic search
grep "pattern" filename
grep -i "pattern" filename   # Case insensitive
grep -n "pattern" filename   # Show line numbers
grep -v "pattern" filename   # Invert match (show lines without pattern)

# Search in multiple files
grep -r "pattern" directory  # Recursive search
grep -l "pattern" *          # Show only filenames with matches

# Advanced patterns
grep "^start" filename       # Lines starting with "start"
grep "end$" filename         # Lines ending with "end"
grep "word1\|word2" filename # Multiple patterns
```

### Find Command

```bash
# Find files by name
find . -name "filename"
find . -iname "filename"     # Case insensitive

# Find files by type
find . -type f               # Files only
find . -type d               # Directories only

# Find files by size
find . -size +100M           # Files larger than 100MB
find . -size -1M             # Files smaller than 1MB

# Find files by modification time
find . -mtime -7             # Modified in last 7 days
find . -mtime +30            # Modified more than 30 days ago

# Execute commands on found files
find . -name "*.txt" -exec rm {} \;    # Remove all .txt files
find . -name "*.log" -exec grep "error" {} \;  # Search in log files
```

### Sed (Stream Editor)

```bash
# Replace text
sed 's/old/new/g' filename
sed 's/old/new/' filename    # Replace first occurrence per line

# Print specific lines
sed -n '5p' filename         # Print line 5
sed -n '10,20p' filename     # Print lines 10-20

# Delete lines
sed '5d' filename            # Delete line 5
sed '/pattern/d' filename    # Delete lines matching pattern

# In-place editing
sed -i 's/old/new/g' filename
```

## 📊 Process Management

### Process Monitoring

```bash
# List processes
ps aux                        # All processes with details
ps -ef                        # Alternative format
ps aux | grep process_name    # Find specific process

# Real-time process monitoring
top                           # Interactive process viewer
htop                          # Enhanced top (if installed)
top -p PID                    # Monitor specific process

# Process information
ps -p PID -o pid,ppid,cmd    # Show process tree
lsof -p PID                   # Show open files for process
```

### Process Control

```bash
# Kill processes
kill PID                      # Send SIGTERM (graceful shutdown)
kill -9 PID                   # Send SIGKILL (force kill)
killall process_name          # Kill all processes with name

# Background and foreground
command &                     # Run command in background
bg                           # Resume background job
fg                           # Bring job to foreground
jobs                         # List background jobs

# Suspend and resume
Ctrl+Z                       # Suspend current process
kill -STOP PID               # Suspend process
kill -CONT PID               # Resume suspended process
```

## 🔧 System Information

### System Status

```bash
# System information
uname -a                      # Kernel and system info
cat /etc/os-release           # OS version information
lscpu                         # CPU information
free -h                       # Memory usage (human readable)
df -h                         # Disk usage (human readable)

# System load
uptime                        # System load and uptime
w                            # Who is logged in and what they're doing
who                          # List logged in users
```

### Network Commands

```bash
# Network connectivity
ping hostname                 # Test connectivity
ping -c 4 hostname           # Ping 4 times
traceroute hostname          # Show network path

# Network information
ifconfig                      # Network interface configuration
ip addr                       # Modern network interface info
netstat -tuln                # Show listening ports
ss -tuln                     # Modern socket statistics

# Download files
wget URL                      # Download file
curl URL                      # Download or test URL
```

## 📝 Text Processing

### File Viewing

```bash
# View file contents
cat filename                  # Display entire file
less filename                 # Interactive file viewer
more filename                 # Page through file
head -n 10 filename           # Show first 10 lines
tail -n 10 filename           # Show last 10 lines
tail -f filename              # Follow file in real-time
```

### Text Manipulation

```bash
# Sort files
sort filename                 # Sort lines alphabetically
sort -n filename              # Sort numerically
sort -r filename              # Sort in reverse order

# Unique lines
uniq filename                 # Remove consecutive duplicate lines
sort filename | uniq          # Remove all duplicates

# Word count
wc filename                   # Lines, words, characters
wc -l filename                # Line count only
wc -w filename                # Word count only
```

### File Comparison

```bash
# Compare files
diff file1 file2              # Show differences
diff -u file1 file2           # Unified diff format
cmp file1 file2               # Binary file comparison

# Compare directories
diff -r dir1 dir2             # Recursive directory comparison
rsync -avn dir1/ dir2/        # Show differences without copying
```

## 🛠️ Advanced Commands

### Compression and Archives

```bash
# Tar archives
tar -cvf archive.tar files/   # Create archive
tar -xvf archive.tar          # Extract archive
tar -czvf archive.tar.gz files/  # Create compressed archive
tar -xzvf archive.tar.gz      # Extract compressed archive

# Zip files
zip archive.zip files/        # Create zip archive
unzip archive.zip             # Extract zip archive

# Gzip compression
gzip filename                 # Compress file
gunzip filename.gz            # Decompress file
```

### Permissions and Ownership

```bash
# Change permissions
chmod 755 filename            # Set permissions (rwxr-xr-x)
chmod +x filename             # Make executable
chmod -w filename             # Remove write permission

# Change ownership
chown user:group filename     # Change owner and group
chgrp group filename          # Change group only

# View permissions
ls -la                        # Show permissions
stat filename                 # Detailed file information
```

### Environment and Variables

```bash
# Environment variables
echo $PATH                    # Show PATH variable
export VAR=value              # Set environment variable
env                           # Show all environment variables

# Shell variables
variable="value"              # Set shell variable
echo $variable                # Display variable value
unset variable                # Remove variable
```

## 🎯 Challenge-Specific Commands

### For Terminal Timebomb Defusal

```bash
# Process monitoring
ps aux | grep suspicious
kill -9 PID

# File searching
find / -name "bomb*" 2>/dev/null
grep -r "explosive" /path/to/search

# System monitoring
htop
top -p $(pgrep suspicious_process)
```

### For Process Monitoring Space Station

```bash
# System monitoring
htop
top -b -n 1                   # One-time snapshot
ps aux --sort=-%cpu           # Sort by CPU usage
ps aux --sort=-%mem           # Sort by memory usage

# Process management
killall process_name
pkill -f pattern
kill -STOP PID
kill -CONT PID
```

### For Grep Detective Agency

```bash
# Pattern searching
grep -r "clue" /path/to/search
grep -i "suspect" *.log
grep -n "evidence" file.txt
grep -A 5 -B 5 "key" file.txt  # Show 5 lines before and after

# Advanced searching
grep -E "pattern1|pattern2" file.txt  # Extended regex
grep -v "red_herring" file.txt        # Exclude patterns
```

## 📚 Useful Aliases and Functions

### Common Aliases

```bash
# Add to ~/.bashrc or ~/.zshrc
alias ll='ls -la'
alias la='ls -A'
alias l='ls -CF'
alias ..='cd ..'
alias ...='cd ../..'
alias grep='grep --color=auto'
alias h='history'
alias j='jobs -l'
```

### Custom Functions

```bash
# Extract function
extract() {
    if [ -f $1 ] ; then
        case $1 in
            *.tar.bz2)   tar xjf $1     ;;
            *.tar.gz)    tar xzf $1     ;;
            *.bz2)       bunzip2 $1     ;;
            *.rar)       unrar e $1     ;;
            *.gz)        gunzip $1      ;;
            *.tar)       tar xf $1      ;;
            *.tbz2)      tar xjf $1     ;;
            *.tgz)       tar xzf $1     ;;
            *.zip)       unzip $1       ;;
            *.Z)         uncompress $1  ;;
            *.7z)        7z x $1        ;;
            *)          echo "'$1' cannot be extracted via extract()" ;;
        esac
    else
        echo "'$1' is not a valid file"
    fi
}
```

## 🔧 Troubleshooting

### Common Issues

```bash
# Permission denied
sudo command                  # Run with elevated privileges
chmod +x filename             # Make file executable

# Command not found
which command                 # Find command location
whereis command               # Find command and documentation

# Disk space issues
df -h                         # Check disk usage
du -sh directory              # Check directory size
du -h | sort -hr | head -10   # Find largest directories
```

---

**Master these commands and become a terminal ninja! 🥷**
