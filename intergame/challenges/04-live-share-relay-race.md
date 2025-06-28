# Challenge #4: Live Share Relay Race 🏃

## 📖 Scenario

The annual Inter-Galactic Coding Relay is here! Your team must pass a coding baton through VS Code Live Share, with each member contributing their part of the solution. But here's the twist - no verbal communication allowed! 🤐

## 🎯 Team Tasks

### 🏃 Runner 1

**Description**: Start the Live Share session and write the first function. Leave comments for the next runner about what needs to be done, then step away from the keyboard.

**Responsibilities**:

- Initialize the Live Share session
- Create the project structure
- Write the first function with clear documentation
- Leave detailed comments for Runner 2
- Cannot communicate verbally with teammates
- Must step away from keyboard when done

**Tools**: VS Code Live Share, Code editing, Comments

### 🏃 Runner 2

**Description**: Join the Live Share, read the comments, complete the second function, and leave instructions for Runner 3. No talking allowed!

**Responsibilities**:

- Join the Live Share session
- Read and understand Runner 1's comments
- Implement the second function
- Add comprehensive comments for Runner 3
- Cannot communicate verbally
- Must rely only on written comments

**Tools**: VS Code Live Share, Code editing, Reading comments

### 🏃 Runner 3

**Description**: Join the session, complete the final function, run all tests, and commit the solution. Celebrate silently when tests pass!

**Responsibilities**:

- Join the Live Share session
- Read previous runners' comments
- Complete the final function
- Run all tests to verify functionality
- Create the final commit
- Cannot communicate verbally
- Must ensure all tests pass

**Tools**: VS Code Live Share, Testing framework, Git commit

## 🛠️ Tools Involved

- **VS Code**: Live Share extension, editing, commenting
- **Git**: commit, push
- **Testing frameworks**: Unit testing, integration testing

## ✅ Success Criteria

Complete a working program with all tests passing, committed by Runner 3 with message 'RELAY_COMPLETE'.

## ⏱️ Time Limit

25 minutes

## 🎮 Difficulty Level

🟢 Easy

## 📋 Setup Instructions

1. Install VS Code Live Share extension
2. Create a new project directory
3. Set up a testing framework (Jest, Mocha, etc.)
4. Prepare a simple coding problem (e.g., calculator, string manipulation)
5. Ensure all team members have VS Code installed

## 🔍 Tips for Success

- **Runner 1**: Write clear, detailed comments explaining your approach
- **Runner 2**: Read carefully and ask questions through comments if needed
- **Runner 3**: Test thoroughly and document any issues found
- **Team**: Use comments effectively for non-verbal communication

## 🏆 Victory Conditions

- All three functions are implemented correctly
- All tests pass successfully
- Code is properly documented with comments
- Final commit is created with message 'RELAY_COMPLETE'
- Team completes the relay without verbal communication

## ⚠️ Failure Conditions

- Verbal communication is used
- Tests fail to pass
- Code is not properly documented
- Team cannot complete the relay in time
- Live Share session fails or disconnects

## 📚 Example Problem: Calculator Functions

```javascript
// Runner 1: Implement addition function
function add(a, b) {
  // TODO: Runner 2 - Implement subtraction function
  // TODO: Runner 3 - Implement multiplication function and run tests
  return a + b;
}

// Runner 2: Implement subtraction function
function subtract(a, b) {
  // TODO: Runner 3 - Implement multiplication function and run tests
  return a - b;
}

// Runner 3: Implement multiplication function
function multiply(a, b) {
  return a * b;
}
```

---

**Ready to run the relay? Let the coding race begin! 🏃‍♂️💨**
