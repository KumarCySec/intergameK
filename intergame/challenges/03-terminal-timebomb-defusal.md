# Challenge #3: Terminal Timebomb Defusal 💣

## 📖 Scenario

A digital bomb has been planted in your system! It's set to go off in 10 minutes, and the only way to defuse it is by solving a series of terminal puzzles. One wrong command and BOOM! 💥

## 🎯 Team Tasks

### 💣 Bomb Expert

**Description**: You have the bomb defusal manual but cannot touch the computer. Give precise instructions to defuse each stage using grep, find, and sed commands.

**Responsibilities**:

- Read and interpret the bomb defusal manual
- Provide precise terminal commands to the Operator
- Guide the defusal process step by step
- Cannot touch the keyboard or see the screen
- Must give exact command syntax

**Tools**: Bomb defusal manual, Command reference guide

### ⌨️ Terminal Operator

**Description**: Execute terminal commands exactly as instructed. One mistake resets the timer! You cannot see the defusal manual.

**Responsibilities**:

- Execute commands exactly as instructed by Bomb Expert
- Report results and output back to the Expert
- Handle any errors or unexpected output
- Cannot see the defusal manual or make decisions
- Must follow instructions precisely

**Tools**: Linux Terminal, grep, find, sed, file manipulation

### ⏰ Time Keeper

**Description**: Monitor the countdown and system processes using htop/top. Alert the team when certain processes appear. You can only use monitoring tools.

**Responsibilities**:

- Monitor the countdown timer
- Watch system processes using htop/top
- Alert team about suspicious processes
- Track defusal progress
- Cannot execute defusal commands

**Tools**: htop, top, ps, process monitoring

## 🛠️ Tools Involved

- **Linux Terminal**: grep, find, sed, htop, ps, kill
- **VS Code**: file viewing
- **System Monitoring**: process management

## ✅ Success Criteria

Successfully defuse all bomb stages and create a 'DEFUSED.txt' file with the final disarm code.

## ⏱️ Time Limit

10 minutes

## 🎮 Difficulty Level

🔴 Hard

## 📋 Setup Instructions

1. Set up a virtual bomb with multiple stages
2. Create hidden files and processes to be discovered
3. Prepare the defusal manual with specific commands
4. Set up monitoring tools for the Time Keeper

## 🔍 Tips for Success

- **Bomb Expert**: Be precise with command syntax and parameters
- **Terminal Operator**: Execute commands exactly as given
- **Time Keeper**: Stay alert and communicate process changes
- **Team**: Work quickly but carefully - mistakes reset the timer!

## 🏆 Victory Conditions

- All bomb stages are successfully defused
- DEFUSED.txt file is created with correct disarm code
- System is secured and no threats remain
- Team completes the mission before time runs out

## ⚠️ Failure Conditions

- Timer reaches zero
- Wrong command is executed (resets timer)
- Critical system files are accidentally modified
- Team cannot communicate effectively

---

**The countdown begins... Can you defuse the bomb in time? ⏰💣**
