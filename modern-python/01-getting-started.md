# Chapter 1: Getting Started with Python in the AI Era

> **Navigation:** Home | [Next: Chapter 2 →](./02-variables-and-types.md)

## 📋 Chapter Overview

**What You'll Learn:**
- How to install Python and verify it works
- Running your first Python program
- Understanding the Python REPL (interactive shell)
- Writing and executing Python scripts
- Basic output with `print()`
- How to use AI tools effectively for learning Python

**Prerequisites:**
- None! This is the starting point

**Time Required:** 90 minutes

**AI Tools Used:** Gemini CLI, Claude Code, GitHub Copilot (optional)

---

## 🎯 Learning Objectives

By the end of this chapter, you will be able to:

1. **Install Python** and verify the installation works on your system
2. **Understand the difference** between interactive Python (REPL) and script mode
3. **Write and execute** your first Python script using `print()`
4. **Collaborate with AI tools** by crafting effective prompts for programming help
5. **Debug simple errors** by reading Python error messages and identifying common beginner mistakes

---

## 📚 Lesson Content (90 minutes)

### 🧩 Phase 1: Manual Concept Discovery (30 minutes)

#### What is Python?

Python is a programming language—a set of instructions you write to tell a computer what to do. Think of it like writing a recipe:
- **Recipe**: "Heat water, add pasta, drain when done"
- **Python**: "Open a file, read the data, print the results"

Python is popular because:
- **Easy to read**: Code looks like English
- **Beginner-friendly**: Less complicated syntax than other languages
- **Powerful**: Used for web apps, data science, AI, automation
- **Large community**: Lots of tutorials and libraries available

#### Getting Started: Installation

**Windows:**
1. Go to https://www.python.org/downloads/
2. Click the big yellow "Download Python" button
3. Run the installer
4. **IMPORTANT**: Check "Add Python to PATH" during installation
5. Click "Install Now"

**Mac:**
```bash
# If you have Homebrew installed:
brew install python3
```

**Linux (Ubuntu/Debian):**
```bash
sudo apt-get update
sudo apt-get install python3
```

#### Verify Your Installation

Open a terminal or command prompt and type:
```bash
python --version
```

Or on Mac/Linux:
```bash
python3 --version
```

You should see something like: `Python 3.11.0`

If you see an error, Python isn't installed correctly. Go back and repeat the installation steps.

#### Your First Python Program

The simplest Python program ever:

```python
print("Hello, World!")
```

That's it! This program outputs the text "Hello, World!" to the screen.

**Understanding `print()`:**
- `print` is a built-in Python function (a pre-written tool)
- The parentheses `()` tell Python: "I'm using this function"
- The text in quotes `"Hello, World!"` is what gets printed
- The exclamation mark is just a character—Python doesn't care what's inside the quotes

#### Activity 1: Run Your First Program (10 minutes)

**Method A: Interactive REPL (Read-Eval-Print Loop)**

The REPL is Python's interactive mode—it reads what you type, evaluates it, prints the result, then waits for more input.

1. Open Terminal/Command Prompt
2. Type: `python` (or `python3` on Mac/Linux)
3. You should see:
   ```
   Python 3.11.0 (main, Oct 24 2023, 12:00:00)
   [GCC 12.2.0] on linux
   Type "help", "copyright", "credits" or "license" for more information.
   >>>
   ```

4. Type this and press Enter:
   ```python
   print("Hello, World!")
   ```

5. Python outputs: `Hello, World!`

6. Type `exit()` to leave the REPL

**Method B: Script File**

1. Open a text editor (Notepad, VS Code, or any plain text editor)
2. Type:
   ```python
   print("Hello, World!")
   ```

3. Save the file as `hello.py` (the `.py` extension means "Python file")

4. Open Terminal/Command Prompt and navigate to where you saved the file

5. Run it:
   ```bash
   python hello.py
   ```
   (or `python3 hello.py` on Mac/Linux)

6. You should see: `Hello, World!`

**Discussion Question:** Why would you use the REPL for quick testing but a script file for longer programs? (Hint: Think about saving your work and running it multiple times.)

#### Activity 2: Experiment with `print()` (10 minutes)

Try these in the REPL (type `python` first):

```python
# Print a number
print(42)

# Print multiple things separated by commas
print("Hello", "Python")

# Print with line breaks (don't worry about the details yet)
print("Line 1\nLine 2")

# Print special characters
print("@#$%^&*()")
```

Each time, notice what appears on the screen. **Experiment!** What happens if you:
- Remove the quotes around text?
- Use single quotes instead of double quotes?
- Leave out the parentheses?

**Key Discovery:** Python reads your code exactly as you write it. If you make a mistake, Python gives you an error message (don't be scared of errors—they're helpful!).

---

### 🤖 Phase 2: AI Exploration & Comparison (25 minutes)

Now that you understand the basics, let's see how AI tools can help you learn and write Python.

#### AI Tool #1: Claude Code

Claude Code is an AI assistant specifically designed for programming. Here's how to use it:

**Prompt 1: Ask for different ways to print**
```
Prompt: "Show me 5 different ways to use the print() function in Python to display information. Explain what each one does."
```

**Expected Output (Paraphrased):**
Claude might show you:
1. Basic text: `print("Hello")`
2. Multiple items: `print("Hello", "World")`
3. With special formatting: `print("Hello\nWorld")` (adds line break)
4. With variables: `print(name)` (we'll learn variables next chapter)
5. With numbers: `print(1 + 2)`

**Comparison Questions:**
- Which method would you use if you wanted to print a person's name and age on the same line?
- What do you think `\n` does? (Hint: check the output)
- Why would printing numbers be useful in a program?

#### AI Tool #2: GitHub Copilot

If you're using VS Code with Copilot, you can write comments and AI generates code:

```python
# Write a program that prints a welcome message
```

Copilot might suggest:
```python
print("Welcome to Python!")
```

Or even:
```python
name = input("What is your name? ")
print(f"Welcome, {name}!")
```

**Key Insight:** AI gives you code, but you need to understand it. The code with `name` and `input()` uses concepts we haven't covered yet. Would you use it? Should you? (More on this in future chapters!)

#### AI Tool #3: Gemini CLI (or ChatGPT)

Command line:
```bash
gemini "What is the difference between printing text and printing numbers in Python? Give an example of each."
```

**Expected Output:**
Gemini might explain:
- Text needs quotes: `print("Hello")`
- Numbers don't: `print(42)`
- But: `print("42")` (with quotes) is text, not a number

**Key Learning:** AI tools show you patterns and best practices. Notice how they explain the "why" behind code, not just the "what."

#### Comparison Activity (10 minutes)

Ask each tool (Claude Code, ChatGPT, or Gemini): **"Write a simple Python program that prints three different messages on separate lines."**

Compare the results:
- Are all the programs correct?
- Do they look different?
- Which explanation was clearest to you?
- Would you use any approach differently?

**Why This Matters:** Different AI tools have different "personalities." Getting good at prompting means finding which tools work best for YOU and how to ask questions clearly.

---

### 🧠 Phase 3: Reverse Engineering & Debugging (20 minutes)

Now let's practice reading and fixing code—a critical skill for programmers.

#### Buggy Code Example 1: Missing Parentheses

Here's code an AI might generate (with an intentional bug):

```python
print "Hello, Python!"
```

**What's wrong?** Try running it. Python gives an error:
```
SyntaxError: Missing parentheses in call to 'print'. Did you mean: print(...)?
```

**Why it's broken:** In Python 3, `print` is a function and MUST have parentheses, even if they're empty.

**The fix:**
```python
print("Hello, Python!")
```

**Debugging lesson:** Read the error message! Python literally told you what was wrong and even suggested a fix.

#### Buggy Code Example 2: Incorrect Quotes

```python
print('Hello, Python!")
```

Error:
```
SyntaxError: unterminated string literal
```

**Why it's broken:** You opened the string with a single quote `'` but closed with a double quote `"`. Python thinks the string never ended.

**The fix:**
```python
print("Hello, Python!")
# OR
print('Hello, Python!')
```

**Key rule:** Open and close quotes must match.

#### Buggy Code Example 3: Typo in Function Name

```python
print("Learning Python")
pritn("Almost there!")
```

Error:
```
NameError: name 'pritn' is not defined
```

**Why it's broken:** `pritn` is not a real Python function. You misspelled `print`.

**The fix:**
```python
print("Learning Python")
print("Almost there!")
```

**Debugging lesson:** When you see "not defined," check your spelling and capitalization. Python is case-sensitive: `print`, `Print`, and `PRINT` are three different things.

#### Debugging Activity (10 minutes)

Here's broken code. Identify the bugs and fix them:

```python
print(Hello, World!)
print 'Python is fun'
print("Almost there)
pritn("Done!")
```

**Answers (try to find them before looking):**
```python
print("Hello, World!")        # Added quotes, fixed parentheses
print('Python is fun')        # Added parentheses
print("Almost there")         # Fixed closing quote
print("Done!")                # Fixed spelling of print
```

**Debugging mindset:** Every error is a clue. Read the error message carefully—it usually tells you exactly what's wrong.

---

### 💡 Phase 4: Creative AI Collaboration (10 minutes)

Let's practice working WITH AI rather than just copying from it.

#### Task: Create a Personalized Welcome Program

Ask Claude Code or ChatGPT:

**Prompt:** "Write a Python program that prints my name and a welcoming message. Use the name 'Alice' as an example."

**Expected Output:**
```python
print("Welcome, Alice!")
print("I'm excited to learn Python with you!")
```

#### Now Make It Your Own

Take the AI-generated code and:
1. **Change the name** from "Alice" to your name
2. **Modify the message** to something you'd actually say
3. **Add another print() call** with additional information

**Example modification:**
```python
print("Welcome, Sarah!")
print("I'm excited to learn Python with you!")
print("Today I learned about the print() function.")
```

#### Collaboration Reflection:
- What was easy about using the AI?
- What would be harder without the AI?
- How did you modify the AI's code to make it yours?
- **When would you be afraid to trust AI code without understanding it?** (Hint: Always!)

---

### 🧱 Phase 5: Manual Reinforcement Challenge (15 minutes)

**NO AI ALLOWED FOR THIS SECTION**

Write a Python program from scratch (no copying) that:

1. Prints your name
2. Prints your favorite hobby
3. Prints a sentence combining both (e.g., "I am Sarah and I love painting")
4. Prints a blank line (using `print()` with no arguments)
5. Prints a fun fact about yourself

**Requirements:**
- Use only `print()` statements
- Each item must be on a separate line
- At least one output should be multiple words

**Example Output:**
```
Sarah
Painting
I am Sarah and I love painting

I have three cats!
```

**Your Challenge:**
Write this program in a file called `about_me.py` and make sure it runs without errors.

**Verification:**
When you run it, your information should appear exactly as you intended. No error messages!

**Success Criteria:**
- ✅ Program runs without errors
- ✅ All 5 pieces of information are printed
- ✅ Information is on separate lines
- ✅ You wrote it yourself (not copied from AI)

---

## 🧪 Homework / Practice Tasks

### Task 1: AI Exploration (Exploration Phase)

Use Claude Code, ChatGPT, or Gemini to explore these questions:

1. **"What are the most common beginner mistakes when learning Python? Give examples."**
   - Take notes on at least 3 mistakes
   - For each mistake, understand WHY it's wrong

2. **"What are some real-world uses of Python? Show me one example of each."**
   - Identify a Python use case that interests you
   - Save this for future motivation!

### Task 2: Manual Coding Practice (30 minutes)

Create a file called `practice.py` with a program that prints:
- Your full name (on one line)
- Your age (on another line)
- Your favorite color (on another line)
- A sentence that combines all three pieces of info

Example output:
```
Sarah Chen
22
Blue
My name is Sarah Chen, I am 22 years old, and my favorite color is Blue.
```

Run the program and verify it works!

### Task 3: Reflection Journal

Answer these questions (write in a text file or your learning journal):

1. **What was the easiest part of this chapter?** Why was it easy?
2. **What was the hardest part?** What would help you understand it better?
3. **How did using AI tools help you learn?** Did they confuse you at any point?
4. **What error message did you find most confusing?** How would you explain it to someone else?
5. **If you had to teach someone else to print text in Python, what's the one thing they MUST understand?**

---

## 🧭 Assessment (10 points)

### Rubric for Chapter 1

| Criterion | Excellent (Full Points) | Good (Partial) | Needs Improvement |
|-----------|-------------------------|----------------|------------------|
| **Manual Code Correctness (3 points)** | `about_me.py` runs with zero errors; all 5 items print correctly on separate lines | Code runs but has minor issues (one missing item or formatting error) | Code doesn't run or has multiple errors |
| **Understanding print() (2 points)** | Explains that print() outputs text; understands quotes and parentheses are required | Identifies print() as "something that makes output" but unclear on syntax details | Confuses print() with other concepts |
| **Error Reading & Debugging (2 points)** | Correctly identifies and fixes all 3 bugs in Phase 3; explains WHY each was wrong | Fixes most bugs but explanation is vague | Guesses at fixes without understanding errors |
| **AI Collaboration (2 points)** | Effectively prompts AI; modifies AI output to make it personal; explains learned concepts | Uses AI but mostly copies output without understanding | Doesn't engage with AI tools or completely lost |
| **Reflection Quality (1 point)** | Thoughtful answers showing genuine learning; specific examples from the chapter | Answers are generic or superficial | No reflection or completely off-topic |

### Example of Excellent Work (10/10):
- `about_me.py` runs perfectly with all 5 required elements
- Student explains print() clearly: "You use print() with parentheses and quotes to show text on the screen"
- Student found all 3 bugs and explained: "The first one needed quotes because print needs a string"
- Student used Claude Code to explore; modified example code; explained one thing they learned
- Reflection includes specific moments: "I was confused about quotes until I tried different types myself"

### Example of Needs Improvement (3/10):
- `about_me.py` has syntax errors
- Student doesn't understand when quotes are needed
- Only fixed 1 out of 3 bugs
- Didn't interact with AI tools meaningfully
- Reflection answers are one sentence and don't show learning

---

## 🔑 Key Takeaways

- **Python is a programming language** that communicates instructions to a computer
- **print() outputs text** to the screen; syntax is crucial: `print("text")`
- **The REPL lets you test code instantly**; scripts let you save and reuse programs
- **Error messages are your friends**—they tell you exactly what's wrong
- **AI tools show patterns and alternatives**, but you must understand the code
- **Always debug by reading the error message** and finding what's different from correct syntax
- **Practice matters more than perfection** at this stage—expect mistakes!

---

## 📖 Quick Reference

### Basic print() Syntax:
```python
# Print text (must use quotes)
print("Hello, World!")

# Print a number (no quotes needed)
print(42)

# Print multiple items (separated by commas)
print("Hello", "World")

# Print nothing (blank line)
print()
```

### Common Patterns:
```python
# Start of a script (tells others what it does)
# This program prints a greeting

# Main content
print("Welcome to Python!")
print("Let's learn together!")
```

### Common Mistakes:
```python
# ❌ Wrong - missing quotes
print(Hello, World!)

# ✅ Correct
print("Hello, World!")

# ❌ Wrong - missing parentheses
print "Hello"

# ✅ Correct
print("Hello")

# ❌ Wrong - mismatched quotes
print('Hello")

# ✅ Correct
print("Hello")
# OR
print('Hello')
```

---

## 🚀 What's Next?

In **Chapter 2: Variables and Data Types**, you'll learn:
- How to store information in variables (like containers for data)
- Different types of data: text, numbers, true/false values
- How to use variables to make programs more flexible and powerful
- AI tools for exploring data types and conversions

You'll write programs that actually DO something with information, not just print static text!

---

## 📚 Teaching Notes for Instructors

### Pacing
- Phase 1: ~30 min (spend time on installation if needed)
- Phase 2: ~25 min (can be homework if time is tight)
- Phase 3: ~20 min (this is where errors become concrete)
- Phase 4: ~10 min (collaboration demonstration)
- Phase 5: ~15 min (watch students code live if possible)

### Common Issues
1. **Installation problems**: Some students' Python won't be in PATH. Have them use the full path: `/usr/bin/python3 hello.py`
2. **REPL confusion**: Some students close it accidentally. Show that `exit()` is intentional.
3. **Quote/parenthesis errors**: These are THE most common beginner mistakes. Drill them.
4. **AI prompt overwhelm**: Some students freeze when using AI. Start with very specific prompts: "Print hello world" not "help me learn python"

### Reinforcement
- Have students run each code example personally
- Let them break code intentionally to see errors
- Celebrate error messages: "Great error! What does it tell us?"
- Pair weaker students with AI-assisted coding to build confidence

### Extensions for Advanced Learners
- Ask them to create a Python file with 10 print() statements
- Have them research: "What was Python named after?" (Hint: not snakes!)
- Challenge: "Use print() to create ASCII art" (squares, triangles, etc.)

---

> **Navigation:** Home | [Next: Chapter 2 →](./02-variables-and-types.md)

---

*Part of the Modern Python with AIDD curriculum*
*Last updated: 2025*
