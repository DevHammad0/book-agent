# Chapter 2: Variables and Data Types in the AI Era

> **Navigation:** [← Previous: Chapter 1](./01-getting-started.md) | [Home](./index.md) | [Next: Chapter 3 →](./03-conditionals.md)

## 📋 Chapter Overview

**What You'll Learn:**
- How to store and use data with variables
- Different data types (strings, integers, floats, booleans)
- Type conversion and checking
- Naming variables effectively
- Working with multiple variables

**Prerequisites:**
- ✅ Chapter 1: Getting Started with Python (print(), running scripts, basic debugging)

**Time Required:** 90 minutes

**AI Tools Used:** Claude Code, ChatGPT, Gemini CLI, GitHub Copilot

---

## 🎯 Learning Objectives

By the end of this chapter, you will be able to:

1. **Create and use variables** to store different types of data
2. **Understand Python's main data types** and when to use each one
3. **Convert between data types** when needed
4. **Debug type-related errors** like incorrect conversions or type mismatches
5. **Collaborate with AI** to explore data type patterns and solve problems

---

## 📚 Lesson Content (90 minutes)

### 🧩 Phase 1: Manual Concept Discovery (30 minutes)

#### What is a Variable?

A variable is a **named container that holds a value**. Think of it like a labeled box:
- The **label** is the variable name (e.g., `name`)
- The **contents** are the value (e.g., `"Alice"`)
- When you need that value, you use the label

Variables let you:
- Store data for later use
- Make code readable (meaningful names instead of numbers)
- Change values without rewriting code

#### Creating Your First Variable

**Basic Syntax:**
```python
variable_name = value
```

The **`=` sign means "store this value in this variable"** (not "equals" like in math).

**Example 1: Storing a name**
```python
name = "Alice"
print(name)  # Output: Alice
```

**What happens:**
1. Python creates a variable called `name`
2. Stores the text `"Alice"` in it
3. `print(name)` retrieves and displays the value

**Example 2: Storing a number**
```python
age = 25
print(age)  # Output: 25
```

**Example 3: Using variables in print()**
```python
name = "Bob"
age = 30
print(name)       # Output: Bob
print(age)        # Output: 30
print(name, age)  # Output: Bob 30
```

#### Python's Main Data Types

Python has several built-in data types. Here are the main ones:

**1. String (text)**
```python
greeting = "Hello, Python!"
language = 'Python'  # Both " and ' work for strings
empty_string = ""     # Empty string is still a string

print(greeting)       # Output: Hello, Python!
print(language)       # Output: Python
```

Key points:
- Strings are text data
- Always use quotes (single `'` or double `"`)
- Numbers inside quotes become text: `"42"` is text, not a number

**2. Integer (whole numbers)**
```python
age = 25
score = 100
temperature = -5

print(age)        # Output: 25
print(temperature)  # Output: -5
```

Key points:
- Integers are whole numbers (no decimal point)
- Can be positive, negative, or zero
- Used for counts, ages, IDs, etc.

**3. Float (decimal numbers)**
```python
price = 19.99
height = 5.8
pi = 3.14159

print(price)      # Output: 19.99
print(height)     # Output: 5.8
```

Key points:
- Floats have decimal points
- Used for measurements, prices, scientific values
- Python automatically uses floats when you use decimals

**4. Boolean (True/False)**
```python
is_student = True
is_complete = False
has_license = True

print(is_student)  # Output: True
print(is_complete) # Output: False
```

Key points:
- Booleans are either `True` or `False` (capitalized!)
- Used for yes/no decisions
- Very important for conditions (coming in Chapter 3)

#### Changing Variable Values

You can change a variable's value anytime:

```python
count = 5
print(count)  # Output: 5

count = 10    # Change the value
print(count)  # Output: 10

count = 15    # Change again
print(count)  # Output: 15
```

**Important**: Reassigning doesn't keep the old value. It's replaced.

```python
name = "Alice"
print(name)    # Output: Alice

name = "Bob"   # Overwrites "Alice"
print(name)    # Output: Bob
```

#### Using Variables in Calculations

You can use variables in math:

```python
x = 10
y = 5

print(x + y)  # Output: 15
print(x - y)  # Output: 5
print(x * y)  # Output: 50
print(x / y)  # Output: 2.0
```

**Important**: Division (`/`) always produces a float, even with whole numbers.

```python
result = 10 / 2
print(result)  # Output: 5.0 (not 5!)
```

If you want whole number division, use `//`:

```python
result = 10 // 3
print(result)  # Output: 3 (discards decimal)
```

#### Activity 1: Create and Use Variables (10 minutes)

Create a new file called `variables_practice.py` and write code that:

1. Creates a variable `favorite_food` and stores your favorite food
2. Creates a variable `portion_size` and stores a number
3. Creates a variable `is_healthy` and stores True or False
4. Prints all three variables (one per line)

**Expected Output (example):**
```
Pizza
3
False
```

**Discussion Questions:**
- Why do you think we use variable names like `favorite_food` instead of just `x`?
- What would happen if you tried to use `favorite-food` (with a dash) as a variable name?
- Can a variable hold multiple values at once? (Hint: we'll explore this more later!)

---

### 🤖 Phase 2: AI Exploration & Comparison (25 minutes)

Now let's see how AI approaches variables and data types. You'll explore different patterns and styles.

#### Exploration Activity: Multiple Approaches

**Using Claude Code or ChatGPT:**

Ask the AI:
```
"Show me 5 different ways to store and display a person's information
(name, age, height) in Python. Explain when you'd use each approach."
```

**Expected responses will show variations like:**

Approach 1: Individual variables
```python
name = "Alice"
age = 25
height = 5.8
```

Approach 2: Combining into one print
```python
info = "Name: Alice, Age: 25, Height: 5.8"
print(info)
```

Approach 3: Using format strings (more on this in a minute!)
```python
name = "Alice"
age = 25
height = 5.8
print(f"Name: {name}, Age: {age}, Height: {height}")
```

**Your Task:**
1. Ask the AI for these variations
2. Copy each one and run it
3. Discuss with your partner or write down:
   - Which approach is clearest to read?
   - Which would be easiest to change?
   - Which feels most "Pythonic"?

#### Exploration Activity: Type Conversion

**Using Gemini CLI or Claude Code:**

Ask the AI:
```
"Show me common ways to convert between different data types in Python.
Include examples of string to int, int to string, and float conversions."
```

**You'll see patterns like:**
```python
# String to Integer
text = "42"
number = int(text)
print(number)  # Output: 42

# Integer to String
count = 100
text = str(count)
print(text)  # Output: "100" (as text)

# Integer to Float
whole = 5
decimal = float(whole)
print(decimal)  # Output: 5.0
```

**Why do we care?**
- Input from users is always text (we'll learn about `input()` soon)
- Sometimes you need to convert text to numbers to do math
- Sometimes you need to convert numbers to text for display

#### Comparison Discussion

After exploring with AI, discuss:

1. **Formatting Options**: Which formatting style did you see the most?
   - `print(name, age)` (separate arguments)
   - `print(name + " " + str(age))` (concatenation)
   - `print(f"Name: {name}, Age: {age}")` (f-strings)

2. **Type Conversion**: When would you use each?
   - `int()` for text to number
   - `str()` for number to text
   - `float()` for decimal numbers

3. **Variable Naming**: What patterns did AI use for variable names?
   - Did they use `_` between words or `camelCase`?
   - Did they use meaningful names or single letters?

---

### 🧠 Phase 3: Reverse Engineering & Debugging (20 minutes)

Now you'll debug code to cement your understanding of data types and variables.

#### Bug Example 1: Missing Quotes (String vs Text)

**Buggy Code from AI:**
```python
favorite_food = Pizza  # ❌ Wrong - no quotes
print(favorite_food)
```

**Error Message:**
```
NameError: name 'Pizza' is not defined
```

**Why it fails:**
- Without quotes, Python thinks `Pizza` is a variable name
- It tries to find a variable called `Pizza` (doesn't exist)
- With quotes, `"Pizza"` is text (a string)

**Fixed Code:**
```python
favorite_food = "Pizza"  # ✅ Correct - has quotes
print(favorite_food)
# Output: Pizza
```

**Your Turn:** Write both versions and see the error yourself!

#### Bug Example 2: Type Conversion Without Conversion

**Buggy Code:**
```python
age_text = "25"
next_age = age_text + 1  # ❌ Wrong - can't add number to text
print(next_age)
```

**Error Message:**
```
TypeError: can only concatenate str (not "int") to str
```

**Why it fails:**
- `age_text` is a string ("25" with quotes)
- You can't do math with strings
- Must convert to integer first

**Fixed Code:**
```python
age_text = "25"
age = int(age_text)  # Convert text to number
next_age = age + 1   # Now we can add
print(next_age)
# Output: 26
```

**Understanding the fix:**
- `int(age_text)` converts `"25"` (text) to `25` (number)
- Now `age + 1` makes sense (number plus number)
- Result is `26`

#### Bug Example 3: Variable Naming Issues

**Buggy Code:**
```python
favorite-food = "Pizza"  # ❌ Wrong - dash not allowed
print(favorite-food)
```

**Error Message:**
```
SyntaxError: invalid syntax
```

**Why it fails:**
- Variable names can only have letters, numbers, and `_`
- Dashes (`-`) are for subtraction, not naming
- Python gets confused

**Fixed Code:**
```python
favorite_food = "Pizza"  # ✅ Correct - underscore instead
print(favorite_food)
# Output: Pizza
```

**Important Rules for Variable Names:**
- Can contain: letters (a-z, A-Z), numbers (0-9), underscore (_)
- Cannot contain: dashes, spaces, special characters
- Cannot start with a number
- Are case-sensitive (`name` and `Name` are different)

**Valid:** `age`, `favorite_food`, `x2`, `_private`, `Age`

**Invalid:** `favorite-food`, `age!`, `2x`, `favorite food`

#### Debugging Activity

Create a file called `debug_practice.py` and copy this buggy code:

```python
# Bug 1
student_name = Bob
print(student_name)

# Bug 2
price = "9.99"
total = price * 2

# Bug 3
is-active = True
print(is-active)
```

**Your Task:**
1. Run the code and see what errors appear
2. Fix each bug based on what you learned
3. Verify it runs without errors

**Discuss:**
- What was the error for each bug?
- How did you fix it?
- Why does that fix work?

---

### 💡 Phase 4: Creative AI Collaboration (10 minutes)

Now you'll use AI to solve a problem that's slightly harder than what you've practiced.

#### Collaborative Challenge

**Problem:** Create a program that calculates a discount on an item.

**Given:**
- Item name (text)
- Original price (number)
- Discount percentage (number between 0-100)

**Goal:** Calculate and display the final price after discount

**Example Output:**
```
Item: Laptop
Original Price: $1000.00
Discount: 15%
Final Price: $850.00
```

#### Part A: Get AI Code (5 minutes)

**Prompt to AI (Gemini CLI or Claude Code):**
```
"Write a Python program that calculates a discount on a product.
Store these in variables:
- item_name (text)
- original_price (number)
- discount_percent (number between 0-100)

Calculate the discount amount and final price.
Print the results nicely formatted."
```

**What you'll get:** AI will generate working code (probably 8-12 lines)

#### Part B: Modify the Code (5 minutes)

**Your modifications:**
1. Change the item, price, and discount to your own values
2. Look at the code and explain to yourself (or a partner) what each line does
3. If the discount calculation seems confusing, ask: "Explain how you calculated the discount"

**What you're learning:**
- How to work with AI-generated code
- How to adapt it to your needs
- How to understand code you didn't write

#### Sample AI-Generated Code (for reference)

```python
item_name = "Phone"
original_price = 500.00
discount_percent = 20

discount_amount = original_price * (discount_percent / 100)
final_price = original_price - discount_amount

print(f"Item: {item_name}")
print(f"Original Price: ${original_price:.2f}")
print(f"Discount: {discount_percent}%")
print(f"Final Price: ${final_price:.2f}")
```

**Concepts in this code:**
- Variables storing different data types
- Math with variables
- Format strings (`f"..."`) for nice output
- The `.2f` means "show 2 decimal places"

---

### 🧱 Phase 5: Manual Reinforcement Challenge (15 minutes)

**IMPORTANT: NO AI ALLOWED FOR THIS SECTION**

Your challenge: Write a program from scratch that manages a simple inventory.

**Requirements:**
Your program should:

1. Create variables for three items in a store inventory:
   - Item 1: Product name, quantity, price
   - Item 2: Product name, quantity, price
   - Item 3: Product name, quantity, price

2. Calculate the total value for each item (quantity × price)

3. Calculate the total inventory value (sum of all item values)

4. Print a report like this:

```
=== INVENTORY REPORT ===

Item: Apples
  Quantity: 50
  Price: $0.50
  Total Value: $25.00

Item: Bread
  Quantity: 20
  Price: $2.50
  Total Value: $50.00

Item: Milk
  Quantity: 15
  Price: $3.00
  Total Value: $45.00

=== SUMMARY ===
Total Inventory Value: $120.00
```

**Getting Started:**
```python
# Start with these variable assignments
item1_name = "Apples"
item1_quantity = 50
item1_price = 0.50

# Continue with items 2 and 3...
```

**Success Criteria:**
- All variables are created and assigned correctly ✓
- All calculations are correct ✓
- Output prints without errors ✓
- You understand every line of code you wrote ✓
- NO copy-paste from AI ✓

**Tips:**
- Write out the calculations step by step
- Use meaningful variable names
- Test by printing each calculation
- You can use f-strings like Phase 4 showed, or simpler print statements

**Time Limit:** 15 minutes

**When Done:**
- Run your code and verify it works
- Check your calculations manually
- Feel confident that you understand variables and data types

---

## 🧪 Homework / Practice Tasks

### Part 1: AI Exploration (15 minutes)

**Task:** Explore data types and variable patterns with an AI tool.

**Prompts to use:**
1. "Show me how to check what type a variable is in Python using type()."
2. "Show me common variable naming conventions used by professional Python developers."
3. "What's the difference between = and == in Python?"

**What to do:**
- Copy each example the AI shows
- Run them to see the output
- Note down what you learned about each one
- Save your notes in a file called `exploration_notes.txt`

**Expected output should include:**
- Using `type()` to check variable types
- Examples of good vs bad variable naming
- Understanding that `=` assigns, `==` compares

### Part 2: Manual Coding Practice (30 minutes)

**Task:** Create a program that stores information about you.

**File name:** `about_me.py`

**Requirements:**
1. Store your basic information:
   - `full_name` (string)
   - `age` (integer)
   - `height_in_inches` (float)
   - `favorite_hobby` (string)
   - `is_student` (boolean)

2. Calculate something:
   - Calculate your age in months (age × 12)
   - Calculate your height in centimeters (height_in_inches × 2.54)

3. Print a nicely formatted profile:
```
=== MY PROFILE ===

Name: [your name]
Age: [age] years old
Age in months: [calculated]
Height: [height] inches ([height in cm] cm)
Hobby: [hobby]
Currently a student: [True/False]
```

**Rules:**
- No copy-paste from AI
- Write all variable assignments manually
- All calculations must be correct
- Output must match the format shown

**Testing:**
- Run your program
- Verify output is correct
- Make sure there are no errors

### Part 3: Reflection Journal (15 minutes)

**File name:** `reflection.txt`

**Answer these questions (3-5 sentences each):**

1. **What felt easy about variables?**
   - Which data types felt most natural to use?
   - Why?

2. **What was confusing?**
   - Did you struggle with any data type or concept?
   - What helped you understand it?

3. **How did AI help you?**
   - What did you learn by asking AI questions?
   - What would have been harder without AI?

4. **Variable Naming**
   - Why does choosing good variable names matter?
   - How did you name your variables in Part 2?

5. **What will you remember?**
   - What's one key insight about variables/types you'll carry forward?

---

## 🧭 Assessment (10 points)

Use this rubric to check your work:

| Criterion | Full Points | Partial (1/2) | Zero | Notes |
|-----------|-------------|---------------|------|-------|
| **Variables Created Correctly** (3 pts) | All variables properly declared with correct types | Some variables have type issues | Variables missing or all wrong types | Check: right type for each value? |
| **Type Understanding** (2 pts) | Clearly demonstrates understanding of strings, ints, floats, booleans | Understands most types but confused on one | Fundamental misunderstanding of types | Ask yourself: Can I explain each type? |
| **Calculations & Conversions** (2 pts) | All calculations correct; proper use of operators | Calculations mostly work; minor conversion issue | Calculations wrong or conversion missing | Check: Does math output match expectations? |
| **AI Collaboration** (2 pts) | Effectively used AI; modified code thoughtfully; can explain it | Used AI but understanding is surface-level | Copied code without understanding | Can you explain the AI-generated code? |
| **Reflection Quality** (1 pt) | Thoughtful, specific insights about learning | Generic observations; little depth | Reflection missing or too brief | Is this YOUR thinking, not generic? |

**Total: 10 points**

**How to Self-Grade:**
1. Check each criterion against your work
2. Be honest about understanding
3. If you scored less than 8/10, review that section before moving to Chapter 3
4. Ask your instructor for feedback on any criterion

---

## 🔑 Key Takeaways

- **Variables store data** with meaningful names
- **Data types matter**: strings (`"text"`), integers (`5`), floats (`5.0`), booleans (`True`)
- **`=` means assignment**, not equality
- **Type conversion** converts between types: `int()`, `str()`, `float()`
- **Variable names** should be meaningful and follow naming rules
- **AI helps you explore patterns** but you must understand the code
- **Manual practice** builds deep understanding that sticks
- **When debugging**, check variable types first (most common error)

---

## 📖 Quick Reference

### Creating Variables
```python
name = "Alice"           # String
age = 25                 # Integer
height = 5.8             # Float
is_student = True        # Boolean
```

### Checking Types
```python
x = "hello"
print(type(x))  # Output: <class 'str'>

y = 42
print(type(y))  # Output: <class 'int'>
```

### Type Conversion
```python
text = "42"
number = int(text)       # Convert string to int: 42

count = 100
text = str(count)        # Convert int to string: "100"

decimal = float(5)       # Convert int to float: 5.0
```

### String Formatting
```python
# Simple concatenation
name = "Bob"
print("Hello, " + name)

# F-strings (modern Python)
name = "Bob"
age = 30
print(f"Hello, {name}. You are {age} years old.")

# Format with decimal places
price = 9.999
print(f"Price: ${price:.2f}")  # Output: Price: $10.00
```

### Common Mistakes
```python
# ❌ Wrong - missing quotes
favorite = Pizza

# ✅ Correct
favorite = "Pizza"

# ❌ Wrong - can't add number to string
total = "10" + 5

# ✅ Correct
total = int("10") + 5

# ❌ Wrong - invalid character in name
my-age = 25

# ✅ Correct
my_age = 25
```

### Variable Naming Rules
```python
# ✅ Valid names
x, name, age_in_years, _private, Name2, CONSTANT

# ❌ Invalid names
my-var, 2x, my var, my!, my*var
```

---

## 🚀 What's Next?

In **Chapter 3: Conditionals**, you'll learn:
- How to make decisions in your code with `if`, `elif`, `else`
- Comparing values using comparison operators (`==`, `>`, `<`, etc.)
- Combining conditions with `and`, `or`, `not`
- Writing code that behaves differently based on data

**Preview:** You'll use variables and data types to make intelligent decisions!

```python
age = 16
if age >= 18:
    print("You can vote!")
else:
    print("You need to wait a bit longer.")
```

---

> **Navigation:** [← Previous: Chapter 1](./01-getting-started.md) | [Home](./index.md) | [Next: Chapter 3 →](./03-conditionals.md)

---

## 📖 Teaching Notes (For Instructors)

### Pacing Guide

- **Phase 1** (30 min): Live coding with class typing along
  - Pause after variable definition to verify students understand
  - Do Activity 1 together if time allows
  - Watch for confusion about quotes vs no quotes (biggest pain point)

- **Phase 2** (25 min): Demonstrate AI prompts
  - Show Gemini/Claude actually producing the code
  - Discuss which approach seems most Pythonic
  - Don't let students get overwhelmed by multiple styles yet

- **Phase 3** (20 min): Debugging practice
  - Do Bug Example 1 live; have students predict the error
  - Let them run buggy code to see real errors
  - Emphasize: "Error messages are your friend"

- **Phase 4** (10 min): Quick AI collaboration
  - This should feel easy after Phase 3
  - Focus on code modification, not understanding everything

- **Phase 5** (15 min): Work time
  - Circulate and check understanding
  - Students should not feel rushed
  - Reassure that mistakes are learning

### Common Student Mistakes

1. **Quotes Confusion (Most common!)**
   - They write `name = Alice` instead of `name = "Alice"`
   - Error message confuses them ("name 'Alice' is not defined")
   - Teach: "Without quotes, Python thinks it's a variable name, not text"

2. **Type Conversion Panic**
   - They don't understand why `"5" + 5` fails
   - Teach: "Strings and numbers are different. You must convert."
   - Practice: Have them convert repeatedly until it clicks

3. **Variable Name with Spaces**
   - They try `my age = 25` instead of `my_age = 25`
   - Show them: "Python reads the space as 'end of variable name'"
   - Teach: "Use underscores for spaces in variable names"

4. **Assuming Variables Persist**
   - They write 5 programs, each with variable `x`, expecting it to carry over
   - Clarify: "Each program is separate. Variables die when program ends."

5. **Overwriting Variables Accidentally**
   - `x = 5` then `x = 10` and they're surprised `x` is no longer 5
   - Teach: "Assignment replaces. There's no 'undo' unless you store it elsewhere."

### Troubleshooting Tips

| Issue | Solution |
|-------|----------|
| Students don't understand type() | Have them check type of everything: numbers, text, True/False |
| Formatting looks too complex | Start with basic print(name, age), skip f-strings in Phase 1 |
| Type conversion is confusing | Use analogy: "Converting a street address (text) to GPS coordinates (numbers)" |
| Some students finish early | Have them create more complex discount calculator or inventory system |
| Some students feel behind | Pair them with student who's ahead; let them debug together |

### Extension Activities (For Advanced Learners)

1. **Temperature Converter**
   - Store Celsius temperature
   - Convert to Fahrenheit: (C × 9/5) + 32
   - Display both

2. **BMI Calculator**
   - Store weight (lbs) and height (inches)
   - Calculate BMI
   - Print health category based on BMI

3. **String Manipulation**
   - Store a sentence
   - Calculate its length: `len(sentence)`
   - Find if a word exists: `"word" in sentence`

4. **Multiple Variable Updates**
   - Create bank account with initial balance
   - "Deposit" and "withdraw" by reassigning
   - Show running balance

### Assessment Tips

- **High Scores (8-10)**: Student understands types, can debug type errors, AI collaboration is thoughtful
- **Medium Scores (6-7)**: Variables work but some type confusion, needs guidance on conversions
- **Low Scores (0-5)**: Fundamental concept misunderstanding; recommend 1-on-1 help before Chapter 3

### Key Teachable Moments

1. **After Phase 3**: "See how error messages tell you exactly what's wrong? That's Python being helpful."
2. **When type() first works**: "This is how you 'talk' to Python about its data. It's a super power."
3. **During Phase 5**: "You just wrote this completely without AI. This is what real programming feels like."
4. **In reflection**: "Good naming means future you (and your team) can understand your code."

### Customization Ideas

- **Use local examples**: Replace "Pizza" with local food, use local prices, heights
- **Different AI tools**: Some students prefer ChatGPT, others like Gemini—let them choose
- **Extra practice**: Create more buggy code for debugging practice
- **Group activity**: Phase 2 as class discussion about different AI approaches
- **Quick wins**: If students are struggling, jump to Phase 5 early; success builds confidence

### Real-World Connection

- **Data science**: Variables storing sensor readings, stock prices, user information
- **Web apps**: Variables storing usernames, passwords, account balances
- **Games**: Variables for player score, health, inventory
- **Finance**: Variables for transactions, interest calculations, account management

Emphasize: "Every app you use is storing data in variables. You're learning the foundation of all software."

---

*Part of the Modern Python with AIDD curriculum*
*Last updated: 2025*
