# Chapter 1: Getting Started with Python in the AI Era

> **Navigation:** Home | [Next: Chapter 2 →](./02-variables-and-types.md)

## 📋 Chapter Overview

**What You'll Learn:**
- How to set up Python on your computer
- Running your first Python programs
- Understanding how Python code executes
- Using AI tools to explore Python concepts

**Prerequisites:**
- None! This is your starting point.

**Time Required:** 90 minutes

**AI Tools Used:** Claude Code, ChatGPT/Gemini (optional)

---

## 🎯 Learning Objectives

By the end of this chapter, you will be able to:

1. Install and verify Python on your system
2. Write and run your first Python program manually
3. Understand how Python interprets and executes code
4. Use AI tools to explore and explain Python basics
5. Debug simple syntax errors independently

---

## 📚 Lesson Content (90 minutes)

### 🧩 Phase 1: Manual Concept Discovery (25 minutes)

#### What is Python?

Python is a programming language—a way to give instructions to a computer. Unlike languages like C++ or Java that require lots of complex syntax, Python is designed to be readable and beginner-friendly. When you write Python code, you're writing instructions that the computer will execute line by line.

**Why Python?**
- Clear, readable syntax (looks almost like English)
- Versatile (web, data science, AI, automation, games)
- Huge community and libraries
- Widely used in industry
- Perfect for learning programming fundamentals

#### Installing Python

**Step 1: Download Python**

Go to [python.org](https://www.python.org) and click the "Downloads" button. Download the latest version (Python 3.12 or newer).

**Step 2: Run the Installer**

1. Double-click the installer
2. **IMPORTANT:** Check the box that says "Add Python to PATH"
3. Click "Install Now"

**Step 3: Verify Installation**

Open your terminal (Command Prompt on Windows, Terminal on Mac/Linux) and type:

```bash
python --version
```

You should see something like `Python 3.12.0`. If you see an error, Python wasn't added to PATH—reinstall and make sure to check that box.

#### Your First Program (Manual)

Let's write your first Python program without any fancy tools—just a text editor and the terminal.

**Step 1: Create a File**

Open any text editor (Notepad, Visual Studio Code, etc.) and create a new file. Type this:

```python
print("Hello, World!")
```

Save it as `hello.py` in a folder you'll remember (like your Documents folder).

**Step 2: Run It**

Open your terminal, navigate to the folder where you saved `hello.py`, and type:

```bash
python hello.py
```

You should see:
```
Hello, World!
```

**Congratulations!** You just wrote and ran your first Python program.

#### What Just Happened?

Let's break down what occurred:

1. You wrote a **Python instruction**: `print("Hello, World!")`
2. Python **interpreted** your code (read it line by line)
3. Python **executed** the instruction (ran it)
4. The computer **displayed** the output: `Hello, World!`

This is how Python always works:
```
Your Code → Python Reads It → Python Executes It → You See Results
```

#### Manual Practice Activity

Now you try. Create a new Python file called `about_me.py` with these instructions:

```python
print("My name is [your name]")
print("I am [your age] years old")
print("I am learning Python!")
```

Replace `[your name]` and `[your age]` with your actual information. Run it with `python about_me.py`. You should see three lines of output.

#### Discussion Questions

1. **What happens if you forget the parentheses** in `print` and write `print "Hello"`?
2. **What's the difference** between `print("Hello")` and `print('Hello')`?
3. **Why do you think** Python requires quotes around text in `print()`?

Take a moment to think about these before moving on.

---

### 🤖 Phase 2: AI Exploration & Comparison (20 minutes)

Now let's see how AI tools can help you understand Python. This phase is about expanding your perspective—seeing how AI approaches the same problems.

#### Using Claude Code (or ChatGPT/Gemini)

You now know how to run basic Python. Let's explore what else `print()` can do.

**Prompt to use:**

If using Claude Code in your terminal:
```bash
claude code "Show me 5 different ways to use print() in Python with examples.
Explain what each one does."
```

If using ChatGPT or Gemini:
```
Show me 5 different ways to use print() in Python with examples.
Explain what each one does.
```

**Expected output might include:**

```python
# Way 1: Simple text
print("Hello, World!")

# Way 2: Multiple items (separated by commas)
print("Name:", "Alice", "Age:", 25)

# Way 3: Using variables (you'll learn this soon)
message = "Welcome"
print(message)

# Way 4: Multiple lines
print("Line 1")
print("Line 2")

# Way 5: Printing numbers
print(42)
print(3 + 5)
```

#### Comparison Questions

After seeing these examples, think about:

1. **Which method is clearest** for printing your name and age?
2. **What happens** when you print a number vs. text in quotes?
3. **How is printing a calculation** (like `3 + 5`) different from printing text?

#### Try It Yourself

Copy one of the AI-generated examples into a new file called `ai_exploration.py` and run it. Did it work as you expected?

---

### 🧠 Phase 3: Reverse Engineering & Debugging (20 minutes)

Now let's practice finding and fixing errors. This is a critical skill in programming.

#### Common Python Errors

Here's some code with intentional bugs. Your job is to **identify what's wrong** and **fix it**.

**Bug Example 1:**
```python
print(Hello, World!")
```

**What's wrong?** The opening quote is missing. The code should be:
```python
print("Hello, World!")
```

**Why does this matter?** Python needs to know where your text starts and ends. Without the opening quote, Python gets confused.

---

**Bug Example 2:**
```python
Print("My name is Alex")
```

**What's wrong?** `Print` is capitalized, but Python requires lowercase `print`. Python is case-sensitive.

**The fix:**
```python
print("My name is Alex")
```

---

**Bug Example 3:**
```python
print("Welcome to Python)
```

**What's wrong?** The closing quote is missing. You have an opening double-quote but no closing one.

**The fix:**
```python
print("Welcome to Python")
```

---

#### Your Debugging Challenge

Here's a program with 3 bugs. Can you find and fix them all?

```python
print(What is Python?)
print("Python is awesome"
print('This line is correct')
```

**Hint:** Look for mismatched quotes and missing punctuation.

**Answer (don't peek!):**
```python
print("What is Python?")
print("Python is awesome")
print('This line is correct')
```

---

### 💡 Phase 4: Creative AI Collaboration (15 minutes)

Now let's use AI as a partner to solve a slightly more complex problem.

#### The Challenge

You want to write a program that introduces a person. Here's what you want it to do:
- Print a greeting
- Print their name
- Print their age
- Print what they're learning

**Here's your prompt to AI:**

"Write a Python program that introduces a person. The program should print their name, age, and what they're learning. Use the print() function. Here's an example output:

```
Hello! My name is Jordan
I am 16 years old
I am learning Python
```"

**AI might give you something like:**

```python
print("Hello! My name is Jordan")
print("I am 16 years old")
print("I am learning Python")
```

**Now, here's the manual part (YOU do this):**

1. **Copy this code** into a new file
2. **Change the values** to be about YOU instead of Jordan
3. **Run it** and verify it works
4. **Add one more line** that says what you had for lunch (try using the same `print()` pattern)

This is the real skill: Taking AI-generated code and adapting it to your needs. AI gives you a template; you make it your own.

---

### 🧱 Phase 5: Manual Reinforcement Challenge (10 minutes)

**⚠️ NO AI ALLOWED in this phase. You must code from scratch.**

Write a Python program that does the following:

1. Prints your favorite color
2. Prints your favorite food
3. Prints "I am excited to learn Python!"

Rules:
- You must write this WITHOUT copying from previous examples
- You must type `print()` for each line
- You must include quotes around text
- You must end the program and run it successfully

**Example output (your output will be different):**
```
Blue
Pizza
I am excited to learn Python!
```

**Success criteria:**
- Program runs without errors ✓
- Three lines of output appear ✓
- Output matches what you intended ✓

---

## 🧪 Homework / Practice Tasks

### Task 1: AI Interaction - Explore Python's History
Use Claude Code, ChatGPT, or Gemini to ask:

"What is the history of Python? Why is it called Python? What companies use Python?"

Read the response and write 2-3 sentences summarizing what you learned. Save this as `homework_history.txt`.

### Task 2: Manual Coding - Build Your Profile
Create a Python file called `my_profile.py` that prints:
- Your name (at least 2 print statements)
- Your age
- Three things you like (each on its own line)
- Something you want to learn

**Requirements:**
- Must have at least 6 `print()` statements
- No copy-pasting from examples
- Must run without errors

### Task 3: Reflection Journal
Write answers to these questions in a file called `reflection.txt`:

1. What was the easiest part of this chapter?
2. What was the hardest part?
3. How did using AI help you understand Python better?
4. What part of Python are you most excited to learn next?

Write at least 2-3 sentences for each question.

---

## 🧭 Assessment (10 points)

Submit your work from Phase 5 (the manual challenge) and Homework Task 2. You'll be assessed on:

| Criterion | Points | What Counts |
|-----------|--------|------------|
| **Manual Coding Correctness** | 3 | Program runs without errors, produces correct output |
| **Code Quality** | 2 | Proper syntax, correct quotes, clean formatting |
| **Completeness** | 2 | All required print statements included |
| **AI Exploration** | 2 | Homework Task 1 completed with thoughtful reflection |
| **Reflection** | 1 | Homework Task 3 shows metacognitive thinking |

**Total: 10 points**

---

## 🔑 Key Takeaways

- **Python is a programming language** that computers interpret and execute line by line
- **`print()` displays output** to your screen
- **Quotes are essential** for text in Python (use `"` or `'`)
- **Python is case-sensitive** (`print` ≠ `Print`)
- **Syntax errors are normal**—they're how you learn what Python expects
- **AI can help you explore** different approaches, but manual practice builds real understanding
- **Testing your code by running it** is the fastest way to learn what works
- **Small, focused programs** are the best way to start learning

---

## 📖 Quick Reference

**Basic Python Syntax:**
```python
# Printing text
print("Hello, World!")

# Printing multiple items
print("Name:", "Alice", "Age:", 25)

# Printing numbers
print(42)

# Printing the result of math
print(3 + 5)
```

**Common Mistakes to Avoid:**
```python
# ❌ Missing opening quote
print(Hello, World!")

# ✅ Correct
print("Hello, World!")

# ❌ Wrong capitalization
Print("Hello")

# ✅ Correct
print("Hello")

# ❌ Mismatched quotes
print("Hello')

# ✅ Correct
print("Hello")
```

**Running Your Program:**
```bash
# First, navigate to the folder with your file
# Then type:
python filename.py

# Example:
python hello.py
```

---

## 🚀 What's Next?

In **Chapter 2: Variables and Data Types**, you'll learn:
- How to store information in variables
- Different types of data (text, numbers, true/false)
- How to use variables in your programs
- Working with numbers and math in Python

You'll move from just printing text to creating programs that store and manipulate information!

---

> **Navigation:** Home | [Next: Chapter 2 →](./02-variables-and-types.md)

*Part of the Modern Python with AIDD curriculum*
