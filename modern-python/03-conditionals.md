# Chapter 3: Conditionals in the AI Era

> **Navigation:** [← Previous: Chapter 2](./02-variables-and-types.md) | [Home](./index.md) | [Next: Chapter 4 →](./04-loops.md)

## 📋 Chapter Overview

**What You'll Learn:**
- How to make decisions in your code with if/elif/else
- Comparison operators (==, !=, >, <, >=, <=)
- Boolean logic with and/or/not
- Nested conditionals
- Debugging conditional logic

**Prerequisites:**
- ✅ Chapter 1: Getting Started with Python (print(), basic debugging)
- ✅ Chapter 2: Variables and Data Types (storing values, data types)

**Time Required:** 90 minutes

**AI Tools Used:** Claude Code, ChatGPT, Gemini CLI, GitHub Copilot

---

## 🎯 Learning Objectives

By the end of this chapter, you will be able to:

1. **Write if/elif/else statements** to control program flow
2. **Use comparison operators** to evaluate conditions
3. **Combine conditions** with and/or/not for complex logic
4. **Debug conditional errors** like logic mistakes and syntax issues
5. **Collaborate with AI** to explore conditional patterns

---

## 📚 Lesson Content (90 minutes)

### 🧩 Phase 1: Manual Concept Discovery (30 minutes)

#### What are Conditionals?

Conditionals are **code that makes decisions**. Your program can behave differently based on conditions.

**Real-world example:**
```
IF age >= 18
    THEN you can vote
ELSE
    you must wait a few years
```

In Python, we use `if`, `elif` (else if), and `else` statements.

#### Your First Conditional: The if Statement

**Basic Syntax:**
```python
if condition:
    # Do this if condition is True
    code_here
```

**Important:** Notice the `:` (colon) and **indentation** (spaces before the code)

**Simple Example:**
```python
age = 20

if age >= 18:
    print("You can vote!")
```

**What happens:**
1. Python checks: Is `age >= 18`?
2. Since age is 20, the condition is `True`
3. The code inside the if block runs
4. Output: `You can vote!`

**Example with False condition:**
```python
age = 15

if age >= 18:
    print("You can vote!")

# No output! The condition was False, so the code didn't run
```

#### Comparison Operators

To make conditions, we use **comparison operators**:

| Operator | Meaning | Example | Result |
|----------|---------|---------|--------|
| `==` | equals | `5 == 5` | `True` |
| `!=` | not equals | `5 != 3` | `True` |
| `>` | greater than | `5 > 3` | `True` |
| `<` | less than | `5 < 3` | `False` |
| `>=` | greater or equal | `5 >= 5` | `True` |
| `<=` | less or equal | `5 <= 3` | `False` |

**Important:** Don't confuse `=` (assignment) with `==` (comparison)

```python
x = 5      # This ASSIGNS 5 to x
x == 5     # This CHECKS if x equals 5 (gives True/False)
```

**Examples:**
```python
score = 85

if score > 80:
    print("Great job!")       # Prints: Great job!

if score == 85:
    print("Perfect!")         # Prints: Perfect!

if score < 60:
    print("Try again")        # Doesn't print (condition is False)
```

#### The if/else Statement

What if you want to do something when the condition is False? Use `else`:

**Syntax:**
```python
if condition:
    # Do this if True
    code_here
else:
    # Do this if False
    code_here
```

**Example:**
```python
age = 15

if age >= 18:
    print("You can vote!")
else:
    print("You cannot vote yet.")

# Output: You cannot vote yet.
```

**Another example:**
```python
password = "secret123"
user_input = "wrong"

if user_input == password:
    print("Access granted!")
else:
    print("Access denied!")

# Output: Access denied!
```

#### The if/elif/else Statement

What if you have MORE than two options? Use `elif` (else if):

**Syntax:**
```python
if condition1:
    # Option 1
    code_here
elif condition2:
    # Option 2
    code_here
elif condition3:
    # Option 3
    code_here
else:
    # Default option
    code_here
```

**Important:** Python stops at the FIRST True condition. It doesn't check the rest.

**Example: Grade Calculator**
```python
score = 85

if score >= 90:
    print("Grade: A")
elif score >= 80:
    print("Grade: B")
elif score >= 70:
    print("Grade: C")
elif score >= 60:
    print("Grade: D")
else:
    print("Grade: F")

# Output: Grade: B
```

**Why B?** Because 85 >= 80 is True, so Python stops and doesn't check >= 70, >= 60, etc.

#### Activity 1: Create a Simple Conditional (10 minutes)

Create a file called `simple_conditional.py` with code that:

1. Creates a variable `temperature` with a number (any temperature)
2. Uses if/elif/else to print a message:
   - If temperature > 30: print "It's hot!"
   - Elif temperature > 15: print "It's mild"
   - Elif temperature > 0: print "It's cold"
   - Else: print "It's freezing!"

**Example output:**
```
It's hot!
```

**Test your code** with different temperatures (31, 20, 5, -5) to verify it works correctly.

---

### 🤖 Phase 2: AI Exploration & Comparison (25 minutes)

Now let's see different ways to work with conditionals.

#### Exploration Activity: Boolean Logic (and/or/not)

**Using Claude Code or ChatGPT:**

Ask the AI:
```
"Show me 5 different ways to combine conditions in Python using 'and', 'or', and 'not'.
Include real-world examples like age verification or access control."
```

**What you'll see:**

Example with `and` (both must be True):
```python
age = 20
has_license = True

if age >= 18 and has_license:
    print("You can drive!")  # Prints if BOTH conditions are True
```

Example with `or` (at least one must be True):
```python
is_weekend = True
is_holiday = False

if is_weekend or is_holiday:
    print("No work today!")  # Prints if AT LEAST ONE is True
```

Example with `not` (reverses True/False):
```python
is_raining = False

if not is_raining:
    print("Let's go outside!")  # Prints if NOT raining
```

**Truth Tables:**

`and` operator:
```
True  and True  = True
True  and False = False
False and True  = False
False and False = False
```

`or` operator:
```
True  or True  = True
True  or False = True
False or True  = True
False or False = False
```

`not` operator:
```
not True  = False
not False = True
```

#### Your Task:
1. Ask the AI for these examples
2. Run each one
3. Predict the output before running
4. Note down when you'd use `and` vs `or` vs `not`

#### Exploration Activity: Nested Conditionals

**Using Gemini CLI or Claude Code:**

Ask:
```
"Show me examples of nested if statements in Python (if inside if).
When would you use nested conditionals instead of 'and'?"
```

**You'll see:**

Nested (if inside if):
```python
age = 20

if age >= 18:
    if has_license:
        print("You can drive!")
```

Combined with `and`:
```python
age = 20

if age >= 18 and has_license:
    print("You can drive!")
```

**Discussion:**
- When is each style clearer?
- Which is easier to read?
- When would nested be better?

#### Comparison Discussion

After exploring with AI, discuss:

1. **Readability**: Which style do you prefer?
   - Nested conditionals (clear structure)
   - Combined with `and`/`or` (concise)

2. **When to use what?**
   - `and` when both conditions must be true
   - `or` when at least one must be true
   - `not` when you want to reverse a condition

3. **Common patterns**: What patterns did the AI show?

---

### 🧠 Phase 3: Reverse Engineering & Debugging (20 minutes)

Now you'll debug conditional logic to cement your understanding.

#### Bug Example 1: Using = Instead of ==

**Buggy Code from AI:**
```python
age = 18

if age = 18:  # ❌ Wrong - using = (assignment)
    print("You are 18!")
```

**Error Message:**
```
SyntaxError: invalid syntax
```

**Why it fails:**
- `=` is for assigning values
- `==` is for comparing values
- Python thinks you're trying to assign in a condition (not allowed)

**Fixed Code:**
```python
age = 18

if age == 18:  # ✅ Correct - using ==
    print("You are 18!")
```

**Memory trick:** "Do I want to CHECK equality (==) or ASSIGN a value (=)?"

#### Bug Example 2: Indentation Error

**Buggy Code:**
```python
score = 85

if score > 80:
print("Good job!")  # ❌ Wrong - missing indentation
```

**Error Message:**
```
IndentationError: expected an indented block
```

**Why it fails:**
- Code inside the `if` block MUST be indented
- Python uses indentation to know what belongs to the if

**Fixed Code:**
```python
score = 85

if score > 80:
    print("Good job!")  # ✅ Correct - indented with 4 spaces
```

**Indentation guide:**
- Use 4 spaces (or 1 tab)
- Be consistent! Mix of spaces and tabs causes errors

#### Bug Example 3: Logic Error (Wrong Operator)

**Buggy Code:**
```python
age = 15

if age < 18:
    print("You can vote!")  # ❌ Wrong logic - should be >=
```

**Error Message:**
```
(No error! But output is wrong)
```

**Why it's wrong:**
- Code runs without errors but gives wrong answer
- The condition checks the wrong thing
- Age 15 < 18 is True, so it prints "You can vote!" (WRONG!)

**Fixed Code:**
```python
age = 15

if age >= 18:
    print("You can vote!")  # ✅ Correct logic
```

**This is a LOGIC ERROR** (different from syntax error):
- Syntax error: Python can't understand the code
- Logic error: Python understands but code does wrong thing

#### Debugging Activity

Create a file called `debug_conditionals.py` and copy this buggy code:

```python
# Bug 1
temperature = 25
if temperature = 25
    print("Perfect temperature!")

# Bug 2
score = 75
if score > 70:
print("You passed!")

# Bug 3
has_money = True
if has_money:
    print("You are poor!")  # Logic is backwards!
```

**Your Task:**
1. Try to run the code (expect errors)
2. Fix the syntax errors first
3. Fix the logic error
4. Verify it runs correctly

**Discuss:**
- What was each error?
- Why did it happen?
- How did you fix it?

---

### 💡 Phase 4: Creative AI Collaboration (10 minutes)

Now you'll use AI to solve a problem that combines multiple conditional concepts.

#### Collaborative Challenge: User Login Verification

**Problem:** Create a login system that checks:
- Username is correct
- Password is correct
- Account is not locked

**Requirements:**
- Store correct username and password
- Store a boolean for account_locked
- Check all three conditions
- Print appropriate message for each case

**Example output:**
```
Username is correct
Password is correct
Account is not locked
Login successful!
```

#### Part A: Get AI Code (5 minutes)

**Prompt to AI (Claude Code or Gemini):**
```
"Write a Python login verification program.
Store these variables:
- correct_username = 'alice'
- correct_password = 'pass123'
- account_locked = False

Store user inputs:
- username = 'alice'
- password = 'pass123'

Check if all three conditions are met for successful login.
Give feedback on what's wrong if login fails."
```

**What you'll get:** AI will generate code with multiple if/elif/else statements

#### Part B: Modify and Understand (5 minutes)

**Your modifications:**
1. Change the stored username/password
2. Try different user inputs (correct, incorrect, locked account)
3. Test at least 3 different scenarios:
   - Correct credentials → success
   - Wrong password → failure
   - Locked account → failure
4. Explain to yourself how the conditionals work

#### Sample AI-Generated Code (for reference)

```python
correct_username = "alice"
correct_password = "pass123"
account_locked = False

username = "alice"
password = "pass123"

if account_locked:
    print("Account is locked. Contact support.")
elif username == correct_username and password == correct_password:
    print("Login successful!")
elif username != correct_username:
    print("Username is incorrect.")
else:
    print("Password is incorrect.")
```

**Key concepts in this code:**
- Multiple conditions with `and`
- Order matters in if/elif/else (check most important first)
- Different messages for different failures

---

### 🧱 Phase 5: Manual Reinforcement Challenge (15 minutes)

**IMPORTANT: NO AI ALLOWED FOR THIS SECTION**

Your challenge: Write a **grade and feedback system** from scratch.

**Requirements:**

Create a program that:

1. Stores a student's test score (0-100)

2. Uses if/elif/else to assign a grade:
   - 90-100: A
   - 80-89: B
   - 70-79: C
   - 60-69: D
   - Below 60: F

3. Provides personalized feedback:
   - A: "Excellent work!"
   - B: "Good job!"
   - C: "Passing, but you can improve."
   - D: "You need to study more."
   - F: "Please see your instructor."

4. Prints the score, grade, and feedback

**Expected Output (example):**
```
Score: 85
Grade: B
Feedback: Good job!
```

**Getting Started:**
```python
# Store the score
score = 85

# Determine grade using if/elif/else
if score >= 90:
    grade = "A"
    feedback = "Excellent work!"
# Continue with other grades...
```

**Success Criteria:**
- All grades (A-F) work correctly ✓
- Feedback matches each grade ✓
- Output is formatted clearly ✓
- You understand every line ✓
- NO copy-paste from AI ✓

**Tips:**
- Write one if/elif block for each grade
- Store both grade and feedback in variables
- Test with scores like 95, 85, 75, 65, 55 to verify all grades work

**Time Limit:** 15 minutes

**When Done:**
- Test your code with at least 5 different scores
- Verify each grade and feedback are correct
- Feel confident in your conditional logic

---

## 🧪 Homework / Practice Tasks

### Part 1: AI Exploration (15 minutes)

**Task:** Explore conditional patterns and best practices.

**Prompts to use:**
1. "Show me common conditional patterns in Python (guard clauses, early returns)."
2. "When should I use nested if statements vs 'and'/'or' operators?"
3. "What are common conditional errors beginners make?"

**What to do:**
- Copy examples the AI shows
- Run them to understand the output
- Note down best practices
- Save insights in `conditional_patterns.txt`

**Expected output should include:**
- Guard clauses (returning early)
- Readability tips
- When to use nested vs combined conditions

### Part 2: Manual Coding Practice (30 minutes)

**Task:** Create a weather advice program.

**File name:** `weather_advisor.py`

**Requirements:**

Create variables for:
- `temperature` (integer, in Fahrenheit)
- `is_raining` (boolean)
- `is_windy` (boolean)

Use conditionals to print advice:
- If temperature >= 85 and not raining: "Wear light clothes and sunscreen"
- If temperature >= 85 and raining: "Bring an umbrella and wear light clothes"
- If temperature between 60-84 and not raining: "Nice weather, enjoy outside!"
- If temperature between 60-84 and raining: "Bring an umbrella"
- If temperature < 60 and is_windy: "Wear a jacket and hat"
- If temperature < 60 and not windy: "Wear a light jacket"
- If is_windy (any temp): Add "Watch out for strong winds!"

**Testing scenarios:**
Test with at least 4 different combinations:
```python
# Scenario 1: Hot and dry
temperature = 90
is_raining = False
is_windy = False

# Scenario 2: Cool and rainy
temperature = 55
is_raining = True
is_windy = False

# Scenario 3: Moderate and windy
temperature = 70
is_raining = False
is_windy = True

# Scenario 4: Cold and rainy
temperature = 35
is_raining = True
is_windy = True
```

**Rules:**
- No copy-paste from AI
- Use if/elif/else with and/or conditions
- Output should be clear and helpful
- Test all 4 scenarios

**Example output for Scenario 1:**
```
Nice weather, enjoy outside!
```

### Part 3: Reflection Journal (15 minutes)

**File name:** `reflection.txt`

**Answer these questions (3-5 sentences each):**

1. **What was hardest about conditionals?**
   - Was it the syntax? Logic? Operators?
   - What helped you understand it?

2. **Comparison operators (==, >, <, etc.)**
   - Can you explain the difference between = and ==?
   - Why is this distinction important?

3. **When to use and/or/not**
   - Think of a real-world example for each
   - When would nested if be better than and/or?

4. **Logic errors vs syntax errors**
   - What's the difference?
   - Why is debugging logic errors harder?

5. **What will you remember?**
   - What's one key insight about conditionals?
   - How will you use this in future programs?

---

## 🧭 Assessment (10 points)

Use this rubric to check your work:

| Criterion | Full Points | Partial (1/2) | Zero | Notes |
|-----------|-------------|---------------|------|-------|
| **Conditionals Work Correctly** (3 pts) | All if/elif/else branches execute correctly; all test cases pass | Some branches work; minor logic issues | Multiple failures; incorrect logic | Test: Does each condition work? |
| **Operator Understanding** (2 pts) | Correctly uses ==, !=, >, <, >=, <=; no confusion with = | Mostly correct; one operator confusion | Fundamental operator confusion | Check: Did you use = instead of ==? |
| **and/or/not Logic** (2 pts) | Complex conditions work; proper use of boolean operators | Simple and/or work; confusion on complex | Doesn't use and/or/not correctly | Can you explain your logic? |
| **AI Collaboration** (2 pts) | Effectively used AI; understood generated code; made meaningful changes | Used AI but surface-level understanding | Copied without understanding | Explain the logic to yourself |
| **Reflection Quality** (1 pt) | Thoughtful, specific insights about conditionals | Generic observations; little depth | Missing or too brief | Is this YOUR thinking? |

**Total: 10 points**

**How to Self-Grade:**
1. Test your code with multiple inputs
2. Be honest about understanding
3. If you scored less than 8/10, review that section before Chapter 4
4. Ask your instructor for feedback

---

## 🔑 Key Takeaways

- **Conditionals control program flow** with if/elif/else
- **Comparison operators** check conditions: ==, !=, >, <, >=, <=
- **= assigns, == compares** (most common mistake!)
- **and/or/not combine conditions**: and (both), or (at least one), not (reverse)
- **Indentation matters** in Python (inside if block must be indented)
- **Order matters** in if/elif/else (stops at first True)
- **Logic errors** run without crashing but give wrong output
- **When debugging**, check: operator used? Indentation? Order of conditions?

---

## 📖 Quick Reference

### Basic Conditionals
```python
# Simple if
if condition:
    print("condition was True")

# if/else
if condition:
    print("True")
else:
    print("False")

# if/elif/else
if condition1:
    print("First")
elif condition2:
    print("Second")
else:
    print("Neither")
```

### Comparison Operators
```python
x == 5    # equals
x != 5    # not equals
x > 5     # greater than
x < 5     # less than
x >= 5    # greater or equal
x <= 5    # less or equal
```

### Boolean Logic
```python
# and - both must be True
if age > 18 and has_license:
    print("Can drive")

# or - at least one must be True
if is_weekend or is_holiday:
    print("Day off")

# not - reverses True/False
if not is_raining:
    print("Go outside")
```

### Nested Conditionals
```python
if age > 18:
    if has_license:
        print("Can drive")
    else:
        print("Get a license")
```

### Common Patterns
```python
# Check multiple conditions
if condition1 and condition2 and condition3:
    print("All true")

# Check if in range
if 18 <= age <= 65:
    print("Working age")

# Guard clause (return early)
if not valid:
    print("Invalid input")
    return
```

### Common Mistakes
```python
# ❌ Wrong - using = instead of ==
if age = 18:
    print("18")

# ✅ Correct
if age == 18:
    print("18")

# ❌ Wrong - missing indentation
if score > 80:
print("Good!")

# ✅ Correct
if score > 80:
    print("Good!")

# ❌ Wrong - logic error
if age < 18:
    print("You can vote!")

# ✅ Correct
if age >= 18:
    print("You can vote!")
```

---

## 🚀 What's Next?

In **Chapter 4: Loops**, you'll learn:
- How to repeat code with `for` and `while` loops
- Using `range()` to control repetition
- Breaking out of loops with `break` and `continue`
- Combining loops with conditionals for powerful programs

**Preview:** Loops let you do the same thing many times:

```python
for i in range(5):
    print(f"Count: {i}")
```

This prints "Count: 0, 1, 2, 3, 4" automatically!

---

> **Navigation:** [← Previous: Chapter 2](./02-variables-and-types.md) | [Home](./index.md) | [Next: Chapter 4 →](./04-loops.md)

---

## 📖 Teaching Notes (For Instructors)

### Pacing Guide

- **Phase 1** (30 min): Live coding with class typing along
  - Emphasize the difference between `=` and `==` (biggest confusion point)
  - Have students practice each operator with examples
  - Do Activity 1 together if time allows
  - Show indentation visually (explain 4-space rule)

- **Phase 2** (25 min): Demonstrate boolean logic
  - Use truth tables on board/slides
  - Show real-world examples (age + license, weekend + holiday)
  - Demo nested vs. combined conditions
  - Discuss readability (which style is clearer?)

- **Phase 3** (20 min): Debugging practice
  - Do Bug Example 1 live; have students predict error
  - Explain difference between syntax errors and logic errors
  - Let students run buggy code to see real errors
  - Debugging activity should feel like detective work

- **Phase 4** (10 min): Quick AI collaboration
  - Show how AI generates multiple branches
  - Emphasize understanding over copying
  - This should feel like a natural extension

- **Phase 5** (15 min): Work time
  - Circulate and check student understanding
  - Ask: "Why did you use >= instead of >?"
  - Verify each student can explain their logic

### Common Student Mistakes

1. **= vs == (MOST COMMON)**
   - They write `if age = 18:` instead of `if age == 18:`
   - Teach: "= puts something IN. == checks if they're the same"
   - Drill this extensively!

2. **Indentation Errors**
   - They forget to indent code inside if block
   - Show: "Indentation tells Python what belongs to the if"
   - Have them count spaces (4 spaces = 1 level)

3. **Logic Errors**
   - They understand syntax but write wrong condition
   - Example: `if age < 18: print("You can vote!")`
   - Teach: "Think about what you want to check, then write it"

4. **Order of if/elif/else**
   - They don't understand that first True match wins
   - Show: "Python stops checking once it finds a True"
   - Draw flowchart to visualize

5. **Complex Conditions**
   - They struggle with `and` vs `or`
   - Teach truth tables explicitly
   - Give many real-world examples

6. **Off-by-One in Ranges**
   - `18 <= age < 65` vs `18 < age <= 65`
   - Clarify: <= includes the number, < doesn't
   - Give practice with multiple ranges

### Troubleshooting Tips

| Issue | Solution |
|-------|----------|
| Students confused about = vs == | Drill repeatedly; make it a class joke/catchphrase |
| Indentation not clear | Show invisible characters in editor; count spaces |
| Boolean logic is abstract | Use truth tables AND real-world examples both |
| Students make logic errors | Have them "talk through" logic before coding |
| Some finish early | Challenge: "Make a more complex login system" |
| Some feel behind | Pair with student ahead; work through logic together |

### Extension Activities (For Advanced Learners)

1. **Number Guessing Game**
   - Generate random number
   - User guesses with feedback (too high/low/correct)
   - Use multiple conditionals

2. **Calculator with Validation**
   - Check if inputs are valid numbers
   - Check if denominator is not zero
   - Give appropriate error messages

3. **Age-Appropriate Content Recommendations**
   - Store movie rating (G, PG, PG-13, R)
   - Store viewer age
   - Use conditionals to recommend

4. **Income Tax Calculator**
   - Different tax rates for different income brackets
   - Nested conditionals or complex and/or logic

5. **Multi-Step Validation**
   - Username (length, characters)
   - Password (length, complexity)
   - Email format check (contains @)

### Assessment Tips

- **High Scores (8-10)**: Student understands conditionals, can debug logic errors, uses and/or/not correctly
- **Medium Scores (6-7)**: Works but some confusion on operators or logic
- **Low Scores (0-5)**: Fundamental concept misunderstanding; recommend 1-on-1 help before Chapter 4

### Key Teachable Moments

1. **After Phase 1**: "Every program you use makes decisions like this. You're building the foundation of real software."
2. **When = vs == clicks**: "That's a huge aha moment! This is one of the top bugs in programming."
3. **During Phase 3**: "Logic errors are harder than syntax errors because Python can't help you find them. YOU have to think like a detective."
4. **In Phase 4**: "Notice how AI combined conditions with 'and'? That's a pro pattern."
5. **In reflection**: "Understanding when to use and vs or is a superpower. It unlocks real programming."

### Customization Ideas

- **Use local examples**: Sports teams, local weather patterns, school grades
- **Make it interactive**: Have students vote on conditions ("Is this a valid password?")
- **Use real data**: Store actual login credentials (non-sensitive), actual temperature data
- **Create flowcharts**: Have students draw before coding
- **Pair activity**: Have partners write opposite conditions (one writes "if", other writes "else")
- **Debugging as game**: "Fix this code faster than your partner"

### Real-World Connection

- **Video games**: Conditionals check if player hit enemy, has health > 0, level complete
- **Banking apps**: Check if balance sufficient, password correct, account active
- **Navigation apps**: Check if route valid, traffic conditions, ETA accurate
- **E-commerce**: Check if user logged in, item in stock, payment successful
- **Social media**: Check if post violates rules, user blocked, comment offensive

Emphasize: "Every app makes millions of decisions per second using conditionals. You're learning what powers the digital world."

---

*Part of the Modern Python with AIDD curriculum*
*Last updated: 2025*
