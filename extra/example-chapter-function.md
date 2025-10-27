# Example Chapter: Functions in the AI Era

This is a complete example of an AIDD chapter following all best practices.

---

# Week 4: Functions in the AI Era

## Module Context

This comes after students have already learned about variables, conditionals, and loops (Weeks 1-3).

**Goal:** Students will understand and use Python functions both manually and in collaboration with AI copilots like Gemini CLI and Claude Code. They'll learn to write, call, and debug functions while understanding when AI can help and when manual coding is essential.

## 🎯 Learning Objectives

By the end of the week, students will be able to:

1. Write and execute Python functions with parameters and return values manually
2. Understand scope, parameter passing, and function execution flow
3. Prompt AI tools to generate, explain, and optimize function-based programs
4. Debug and rewrite AI-generated functions to solidify syntax understanding
5. Compare manual and AI approaches to develop functional programming reasoning

## 📚 Lesson Flow (90 minutes)

### 🧩 Phase 1: Manual Concept Discovery (30 minutes)

**Instructor Demo (5 minutes):**

```python
def greet(name):
    message = f"Hello, {name}!"
    return message

result = greet("Alice")
print(result)  # Output: Hello, Alice!
```

**Explain:**
- **Function Definition**: `def` keyword, function name, parameters in parentheses
- **Function Body**: Indented code that runs when function is called
- **Return Statement**: Sends value back to caller
- **Function Call**: Using the function name with arguments
- **What Happens Internally**:
  1. Python jumps to function definition
  2. Creates local variable `name` with value "Alice"
  3. Executes function body
  4. Returns result back to caller
  5. Continues with rest of program

**Student Activity 1 (20 minutes):**

Write the following by hand:

1. **Basic Function:**
```python
# Write a function called add that takes two numbers and returns their sum
# Test it with: add(5, 3) → should return 8
```

2. **Function with Logic:**
```python
# Write a function called is_even that takes a number and returns True if even, False if odd
# Test with: is_even(4) → True, is_even(7) → False
```

3. **Function with Multiple Statements:**
```python
# Write a function called find_max that takes two numbers and returns the larger one
# Use if-else inside the function
# Test with: find_max(10, 25) → 25
```

**Discussion Question (5 minutes):**

"What would happen if you forget the `return` statement in a function? Try it and explain the difference between `print()` inside a function and `return`."

**Expected Insights:**
- Without `return`, function returns `None`
- `print()` shows output but doesn't give value back to caller
- `return` provides value that can be used in expressions

This builds manual logic understanding before any AI involvement.

### 🤖 Phase 2: AI Exploration & Comparison (25 minutes)

**Prompt 1 (Gemini CLI) (8 minutes):**

```bash
gemini "Show 4 different ways to write a function that calculates the area of a rectangle in Python. Include: basic approach, with default parameters, with type hints, and with documentation. Explain when to use each."
```

Students review output — for example:

```python
# Approach 1: Basic function
def area_rectangle(length, width):
    return length * width

# Approach 2: With default parameters (assumes square if width not given)
def area_rectangle(length, width=None):
    if width is None:
        width = length
    return length * width

# Approach 3: With type hints (Python 3.5+)
def area_rectangle(length: float, width: float) -> float:
    return length * width

# Approach 4: With full documentation
def area_rectangle(length: float, width: float) -> float:
    """
    Calculate the area of a rectangle.

    Args:
        length (float): The length of the rectangle
        width (float): The width of the rectangle

    Returns:
        float: The area of the rectangle

    Example:
        >>> area_rectangle(5, 3)
        15
    """
    return length * width
```

**Instructor Task (15 minutes):**
Ask students:

**Readability Questions:**
- "Which version is easiest to understand for a beginner?"
- "Which provides the most helpful information to other developers?"
- "When would documentation be essential vs. optional?"

**Functionality Questions:**
- "What's the advantage of default parameters? When might this cause bugs?"
- "What do type hints tell us? Do they enforce types?"
- "Which version would you use in a professional project? Why?"

**Best Practices Discussion:**
- "PEP 8 recommends descriptive names—are these good function names?"
- "When is it worth adding documentation vs. when is it overkill?"

**Mini Reflection (2 minutes):**

Students write quick notes:
- "What did the AI show you that you hadn't considered?"
- "Which approach matches how you were thinking about functions?"
- "What's one new technique you want to try?"

### 🧠 Phase 3: Reverse Engineering & Debugging (20 minutes)

**Instructor Setup (3 minutes):**

"An AI tool generated this function to calculate the factorial of a number, but there's a bug. Your job is to find and fix it."

**The Buggy Code:**

```python
def factorial(n):
    result = 0  # Bug here
    for i in range(1, n + 1):
        result = result * i
    return result

print(factorial(5))  # Should be 120, but prints 0
```

**Ask Students (10 minutes):**

1. **Identify the Bug:**
   - "What's wrong with this code?"
   - "Why does it output 0 instead of 120?"

2. **Trace Execution:**
   - "Walk through what happens when factorial(5) is called"
   - "What's the value of result after each iteration?"

3. **Fix It:**
   - "How would you fix this bug?"
   - "What should result be initialized to?"

**Expected Fix:**

```python
def factorial(n):
    result = 1  # Fixed: start with 1, not 0
    for i in range(1, n + 1):
        result = result * i
    return result

print(factorial(5))  # Correctly prints 120
```

**Explanation:**
- Multiplying by 0 always gives 0
- Factorial requires starting with 1 (the multiplicative identity)
- This is a common initialization error

**AI Comparison (7 minutes):**

**Then:** Ask Claude Code to explain the bug:

```bash
claude "This factorial function has a bug:

def factorial(n):
    result = 0
    for i in range(1, n + 1):
        result = result * i
    return result

Explain what's wrong, why it fails, and how to fix it."
```

**Discussion:**
- "How did Claude's explanation compare to your understanding?"
- "Did Claude mention anything you didn't think of?"
- "Whose explanation would help a confused student more?"
- "What did you learn from debugging this manually first?"

**Bonus Bug (if time):**

```python
def calculate_average(numbers):
    total = sum(numbers)
    return total / len(numbers)

result = calculate_average([])  # ZeroDivisionError
```

### 💡 Phase 4: Creative AI Collaboration (10 minutes)

**Problem Statement (2 minutes):**

"Create a function that validates passwords. A valid password must:
1. Be at least 8 characters long
2. Contain at least one uppercase letter
3. Contain at least one number

Your function should return True if valid, False otherwise, and optionally explain why it failed."

**Prompt Claude Code (3 minutes):**

```bash
claude-code "Write a Python function called validate_password that checks if a password meets these requirements: at least 8 characters, at least one uppercase letter, at least one number. Return True if valid, False otherwise. Include helpful comments."
```

**Sample AI Output:**

```python
def validate_password(password):
    """
    Validate a password based on security requirements.

    Args:
        password (str): The password to validate

    Returns:
        bool: True if password is valid, False otherwise
    """
    # Check length requirement
    if len(password) < 8:
        return False

    # Check for at least one uppercase letter
    has_uppercase = any(char.isupper() for char in password)
    if not has_uppercase:
        return False

    # Check for at least one number
    has_number = any(char.isdigit() for char in password)
    if not has_number:
        return False

    return True

# Test cases
print(validate_password("Test1234"))   # True
print(validate_password("test1234"))   # False (no uppercase)
print(validate_password("Test"))       # False (too short, no number)
```

**Manual Modification Tasks (5 minutes):**

Students must manually:

**Task 1 - Explain:**
"In your own words, explain how the `any()` function works in this code. Don't just read the comment—explain why this approach works."

**Task 2 - Modify:**
"Change the function to also require at least one special character (!@#$%^&*). Edit the code yourself—don't ask AI to do it."

**Expected modification:**
```python
# Add after the number check:
has_special = any(char in "!@#$%^&*" for char in password)
if not has_special:
    return False
```

**Task 3 - Enhance:**
"Modify the function to return a tuple: (is_valid, error_message). If invalid, explain what's missing."

**Trade-off Discussion:**
- "Is it better to check all conditions and return a list of problems, or fail fast on the first problem?"
- "How would you balance security (strict rules) with user experience (frustration)?"
- "What makes this code readable? What would make it more readable?"

### 🧱 Phase 5: Manual Reinforcement Challenge (15 minutes)

**⚠️ CRITICAL RULE: NO AI TOOLS ALLOWED**

**Challenge Setup (2 minutes):**

**The Problem:**
"Write a Python function called `calculate_discount` that:
1. Takes two parameters: `price` (float) and `discount_percent` (int)
2. Returns the final price after applying the discount
3. If discount is greater than 50%, apply a maximum of 50%
4. Round the result to 2 decimal places

Example:
- calculate_discount(100, 20) → 80.0
- calculate_discount(50, 60) → 25.0 (60% limited to 50%)
- calculate_discount(99.99, 15) → 84.99"

**Success Criteria:**
- [ ] Function correctly calculates discount
- [ ] Handles discount cap at 50%
- [ ] Returns value rounded to 2 decimal places
- [ ] Works with the test cases above

**Time Limit:** 12 minutes

**Individual Work (10 minutes):**

Students code in silence. Instructor circulates to answer clarification questions only.

**Class Verification (3 minutes):**

**Reference Solution:**
```python
def calculate_discount(price, discount_percent):
    # Cap discount at 50%
    if discount_percent > 50:
        discount_percent = 50

    # Calculate discount amount
    discount_amount = price * (discount_percent / 100)

    # Calculate final price
    final_price = price - discount_amount

    # Round to 2 decimal places
    return round(final_price, 2)

# Test cases
print(calculate_discount(100, 20))    # 80.0
print(calculate_discount(50, 60))     # 25.0
print(calculate_discount(99.99, 15))  # 84.99
```

**Discussion:**
- "What was the trickiest part?"
- "Did anyone use a different approach?"
- "What function syntax did you use from Phase 1?"

**Optional AI Comparison (if time):**
```bash
gemini "Write a calculate_discount function: takes price and discount_percent, caps discount at 50%, rounds to 2 decimals."
```

Compare approaches and discuss which is clearer.

## 🧪 Homework / Practice Tasks

### Assignment Overview
**Due:** Next class
**Estimated Time:** 40 minutes
**Submission:** Submit .py file and reflection document

### Part 1: AI Exploration (15 minutes)

**Task:**
Use Gemini CLI to explore different function parameter techniques.

**Prompt:**
```bash
gemini "Show 5 creative examples of Python function parameters: default parameters, *args, **kwargs, keyword-only parameters, and parameter unpacking. For each, provide code and explain when to use it."
```

**Deliverable:**
1. Copy the AI's response
2. Choose ONE technique that's new to you
3. Write your own function using that technique (different from AI's example)
4. Write 3-4 sentences explaining:
   - What the technique does
   - Why it's useful
   - How your example demonstrates it

### Part 2: Manual Practice (20 minutes)

**Task:**
Write a Python program **without any AI assistance** that includes these three functions:

```python
# Function 1: celsius_to_fahrenheit
# Takes temperature in Celsius, returns Fahrenheit
# Formula: F = (C * 9/5) + 32

# Function 2: fahrenheit_to_celsius
# Takes temperature in Fahrenheit, returns Celsius
# Formula: C = (F - 32) * 5/9

# Function 3: convert_temperature
# Takes temperature, from_unit ('C' or 'F'), to_unit ('C' or 'F')
# Uses the above functions to perform conversion
# Should handle invalid inputs gracefully
```

**Test Cases:**
Your program should pass these tests:
```python
assert celsius_to_fahrenheit(0) == 32
assert celsius_to_fahrenheit(100) == 212
assert fahrenheit_to_celsius(32) == 0
assert fahrenheit_to_celsius(212) == 100
assert convert_temperature(0, 'C', 'F') == 32
assert convert_temperature(32, 'F', 'C') == 0
```

**Requirements:**
- All three functions must work correctly
- Add comments explaining key parts
- Use descriptive variable names
- Handle edge cases (what if someone enters 'Celsius' instead of 'C'?)

### Part 3: Reflection Journal (5 minutes)

Answer these questions (6-8 sentences total):

1. **Syntax Recognition:**
   "What function patterns do you now recognize immediately? Give a specific example from today."

2. **AI Learning:**
   "How did seeing AI's different parameter techniques help you understand functions better? What surprised you?"

3. **Manual Confidence:**
   "Rate your confidence (1-10) in writing functions manually. What specific aspect of functions do you find most challenging?"

4. **Application:**
   "Describe a specific problem in your life that you could solve with a Python function. What would the function do?"

**Example Reflection:**
"I now immediately recognize the def keyword and understand that parameters are placeholders for values. Seeing AI's use of default parameters showed me how to make functions more flexible—I didn't know you could make some parameters optional. I'd rate my confidence at 7/10 because I can write basic functions easily, but I sometimes forget the return statement. The most challenging part is deciding what should be a function vs. just regular code. I could write a function to calculate my monthly savings based on income and expenses, which would help me budget better."

### Submission Checklist

Before submitting:
- [ ] Part 1: AI exploration with your own example and explanation
- [ ] Part 2: Complete temperature_converter.py file
- [ ] Part 2: All test cases pass
- [ ] Part 3: Reflection answers (6-8 sentences)
- [ ] Code has helpful comments
- [ ] No AI was used for Part 2
- [ ] File includes your name and date

## 🧭 Assessment (10 points)

| Criterion | Exemplary (Full Points) | Proficient (Partial) | Developing (Minimal) | Points |
|-----------|------------------------|---------------------|---------------------|--------|
| **Manual Function Correctness (3 pts)** | All functions work perfectly, handle edge cases, clean code with good names and comments | Functions work with minor issues OR missing some edge cases OR formatting needs improvement | Functions have logic errors, syntax mistakes, or don't run | __/3 |
| **AI Collaboration (3 pts)** | Clear, specific prompt; thorough explanation of chosen technique; own example demonstrates deep understanding | Prompt works but vague OR explanation superficial OR own example has minor errors | Ineffective prompt OR can't explain technique OR example doesn't work | __/3 |
| **Debugging Reasoning (2 pts)** | Identified bug correctly, explained root cause clearly, provided correct fix with detailed reasoning | Identified bug but explanation unclear OR fix correct but reasoning weak | Failed to identify bug OR incorrect fix | __/2 |
| **Reflection Clarity (2 pts)** | Insightful reflection with specific examples; clear metacognitive awareness; thoughtful application ideas | General reflection with some specifics OR mentions AI but lacks depth OR application idea vague | Vague reflection OR doesn't address AI learning OR no real application thought | __/2 |

### Grading Examples

**Manual Correctness - Full Credit (3/3):**
```python
def celsius_to_fahrenheit(celsius):
    """Convert Celsius to Fahrenheit."""
    return (celsius * 9/5) + 32

def fahrenheit_to_celsius(fahrenheit):
    """Convert Fahrenheit to Celsius."""
    return (fahrenheit - 32) * 5/9

def convert_temperature(temp, from_unit, to_unit):
    """
    Convert temperature between Celsius and Fahrenheit.

    Args:
        temp: Temperature value
        from_unit: 'C' or 'F' (case insensitive)
        to_unit: 'C' or 'F' (case insensitive)
    """
    # Normalize to uppercase for comparison
    from_unit = from_unit.upper()
    to_unit = to_unit.upper()

    # Validate inputs
    if from_unit not in ['C', 'F'] or to_unit not in ['C', 'F']:
        return "Invalid unit. Use 'C' or 'F'."

    # If same unit, return original
    if from_unit == to_unit:
        return temp

    # Convert
    if from_unit == 'C':
        return celsius_to_fahrenheit(temp)
    else:
        return fahrenheit_to_celsius(temp)
```
✓ All functions work correctly
✓ Handles edge cases (same unit, invalid input, case insensitive)
✓ Clear function names and documentation
✓ Proper code organization

**AI Collaboration - Full Credit (3/3):**
"I prompted Gemini: 'Show 5 creative examples of Python function parameters: default parameters, *args, **kwargs, keyword-only parameters, and parameter unpacking.'

I chose default parameters because I didn't realize you could make some parameters optional. Here's my example:

```python
def create_profile(name, age=18, country='Unknown'):
    return f"{name}, {age} years old, from {country}"

print(create_profile("Alice"))  # Uses defaults
print(create_profile("Bob", 25, "USA"))  # Overrides all
```

This demonstrates default parameters by showing that age and country are optional—if you don't provide them, the function uses 18 and 'Unknown'. This is useful when most users will want the same default values but you still want flexibility."

✓ Specific, effective prompt
✓ Clear explanation showing understanding
✓ Original working example
✓ Explains why the technique is useful

**Reflection - Full Credit (2/2):**
"Functions now make sense to me because I understand they're like reusable recipes—def is the keyword, parameters are ingredients, and return gives back the result. Seeing AI's four different ways to write the area function (especially the one with documentation) showed me that professional code needs to explain itself, not just work. I'm at 6/10 confidence because I can write simple functions, but I struggle with knowing when to use default parameters vs. required ones. I could create a study_time_calculator function that takes my assignment list and deadlines, returns how many hours to study each day, which would help me manage my time better since I always leave things to the last minute."

✓ Specific syntax understanding
✓ Deep insight about AI teaching
✓ Honest self-assessment with specific challenge
✓ Real, detailed application idea

## 🧠 Teaching Notes

### Key Concepts to Emphasize
- **Functions as Abstraction**: They hide complexity and let you reuse code
- **Parameters vs. Arguments**: Parameters are in definition, arguments are in call
- **Return vs. Print**: Common beginner confusion—return gives value back
- **Scope**: Variables inside functions are local unless declared global
- **DRY Principle**: Don't Repeat Yourself—functions prevent code duplication

### Common Student Struggles
1. **Forgetting Return Statement**
   - Solution: Have them trace what happens to the value without return
   - Show examples where the value is needed in calculations

2. **Parameter Naming Confusion**
   - Solution: Emphasize that parameter names are just placeholders
   - Show same function with different parameter names

3. **When to Use Functions**
   - Solution: Rule of thumb: if you do something twice, make it a function
   - Show examples of repetitive code vs. function calls

4. **Scope Issues**
   - Solution: Draw scope diagrams showing local vs. global
   - Demonstrate with print statements showing what's visible where

### Extension Opportunities
**For fast finishers:**
- Lambda functions (anonymous functions)
- Recursion basics
- Higher-order functions (map, filter, reduce)
- Decorators (introductory)

**For struggling students:**
- More practice with simple functions (one parameter, simple logic)
- Visual function call diagrams
- Pairing with stronger students for peer teaching

### Assessment Notes
- Watch for students who can call functions but can't write them
- Check if they understand WHY to use functions, not just HOW
- Look for good naming conventions—this shows understanding
- Note students who skip directly to AI without manual attempts

### Teaching Philosophy Reinforced
1️⃣ **Manual builds understanding** - Students write simple functions first
2️⃣ **AI expands perspective** - Multiple approaches show best practices
3️⃣ **Debugging cements syntax** - Finding initialization bug teaches careful thinking
4️⃣ **Reflection builds mastery** - Students articulate what they've learned

### Next Week Preview
Week 5 will build on functions by introducing:
- Lists and data structures (functions that operate on lists)
- Function composition (calling functions inside functions)
- Sets up for Week 6 on file I/O (functions for reading/writing)
