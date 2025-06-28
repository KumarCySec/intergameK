# Challenge #2: The Great Code Heist 🕵️

## 📖 Scenario

A notorious bug has infiltrated your codebase and is hiding somewhere in the commit history. Your elite team of digital detectives must track it down using forensic Git tools before it corrupts the entire system!

## 🎯 Team Tasks

### 🕵️ Detective Chief

**Description**: Use git blame and git log to identify which developer introduced the suspicious code. You coordinate the investigation but cannot touch the keyboard.

**Responsibilities**:

- Analyze code using git blame to find suspicious changes
- Review git log to identify problematic commits
- Coordinate the investigation strategy
- Direct team members on what to examine
- Cannot execute commands directly

**Tools**: Git blame, Git log analysis, Investigation coordination

### 🔍 Forensic Analyst

**Description**: Execute git bisect to narrow down the exact commit where the bug was introduced. Follow only verbal instructions from the Detective Chief.

**Responsibilities**:

- Execute git bisect commands as directed
- Test each commit to determine if bug is present
- Report results back to Detective Chief
- Cannot make independent decisions about which commits to test
- Follow precise instructions from the Chief

**Tools**: Git bisect, Testing framework, Terminal commands

### 📝 Evidence Recorder

**Description**: Document all findings in a case-report.md file and create a git tag marking the criminal commit. You can only work when the other two give you permission.

**Responsibilities**:

- Document all investigation findings
- Create detailed case report
- Tag the criminal commit when identified
- Organize evidence and timeline
- Wait for permission before documenting

**Tools**: Markdown editing, Git tagging, Documentation

## 🛠️ Tools Involved

- **Git**: blame, log, bisect, tag
- **VS Code**: editing, search
- **Linux Terminal**: file manipulation

## ✅ Success Criteria

Create a git tag 'CRIMINAL_COMMIT' on the offending commit and submit a detailed case report with evidence.

## ⏱️ Time Limit

20 minutes

## 🎮 Difficulty Level

🟡 Moderate

## 📋 Setup Instructions

1. Set up a repository with a known bug in the commit history
2. Prepare test cases to identify when the bug appears
3. Ensure git bisect is properly configured
4. Create template for case report

## 🔍 Tips for Success

- **Detective Chief**: Be systematic in your investigation approach
- **Forensic Analyst**: Test thoroughly at each bisect step
- **Evidence Recorder**: Keep detailed notes of all findings
- **Team**: Communicate clearly about test results and findings

## 🏆 Victory Conditions

- Bug is successfully identified in the commit history
- Git tag 'CRIMINAL_COMMIT' is created on the correct commit
- Complete case report is submitted with all evidence
- Investigation timeline is documented

---

**The hunt for the code criminal begins! 🔍**
