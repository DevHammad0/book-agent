# AI Tool Prompts Reference Guide

This document provides proven AI prompts for different learning scenarios in the AIDD methodology.

## Supported AI Tools

### Primary Tools
1. **Gemini CLI** - Command-line interface, good for quick queries
2. **Claude Code** - Agentic coding tool, excellent for explanations
3. **GitHub Copilot** - IDE integration, code completion
4. **ChatGPT** - Web interface, conversational
5. **Claude.ai** - Web interface, detailed explanations

## Prompt Templates by Phase

### Phase 2: AI Exploration & Comparison

#### Template 1: Multiple Approaches
**Format:**
```bash
[ai-tool] "Show [N] different ways to [task] in Python. For each approach: (1) provide working code, (2) explain when to use it, (3) list pros and cons, (4) discuss efficiency."
```

**Examples:**

**Loops:**
```bash
gemini "Show 4 different ways to iterate over a list in Python. For each: provide code, explain when to use it, list pros/cons, discuss efficiency."
```

**Functions:**
```bash
claude-code "Show 3 different ways to create a function that validates email addresses in Python. Include: basic approach, regex approach, and using a library. Explain trade-offs."
```

**Data Structures:**
```bash
gemini "Show 3 different ways to count word frequency in a text using Python data structures. Compare lists, dicts, and Counter. Include time complexity."
```

#### Template 2: Concept Explanation
**Format:**
```bash
[ai-tool] "Explain [concept] in Python as if teaching a beginner. Include: (1) what it is, (2) why it's useful, (3) simple example, (4) common mistakes, (5) best practices."
```

**Examples:**

**List Comprehensions:**
```bash
claude "Explain Python list comprehensions as if teaching a beginner. Include: what they are, why they're useful, simple example, common mistakes, and best practices."
```

**Decorators:**
```bash
gemini "Explain Python decorators step-by-step for someone who just learned functions. Include simple examples before advanced ones."
```

#### Template 3: Optimization Analysis
**Format:**
```bash
[ai-tool] "Here's my Python code: [paste code]. Show 3 ways to optimize it for [performance/readability/memory]. Explain the trade-offs of each."
```

**Example:**
```bash
claude-code "Here's my code that finds prime numbers:

```python
def find_primes(n):
    primes = []
    for num in range(2, n):
        is_prime = True
        for i in range(2, num):
            if num % i == 0:
                is_prime = False
        if is_prime:
            primes.append(num)
    return primes
```

Show 3 ways to optimize this for performance. Explain trade-offs."
```

### Phase 3: Debugging Prompts

#### Template 1: Bug Explanation
**Format:**
```bash
[ai-tool] "This Python code has a bug: [paste code]. Explain: (1) what's wrong, (2) why it's a problem, (3) how to fix it, (4) how to prevent similar bugs."
```

**Example:**
```bash
claude "This code has a bug:

```python
def calculate_average(numbers):
    total = 0
    for num in numbers:
        total += num
    return total / len(numbers)

result = calculate_average([])
```

Explain what's wrong, why it fails, how to fix it, and how to prevent similar bugs."
```

#### Template 2: Error Message Explanation
**Format:**
```bash
[ai-tool] "I got this Python error: [error message]. Explain in simple terms: (1) what this error means, (2) common causes, (3) how to fix it, (4) example fix."
```

**Example:**
```bash
gemini "I got this error: 'list index out of range'. Explain what this means in simple terms, common causes, and how to fix it with examples."
```

#### Template 3: Code Review
**Format:**
```bash
[ai-tool] "Review this Python code and identify potential bugs, style issues, and improvements: [paste code]"
```

### Phase 4: Creative Collaboration

#### Template 1: Open-Ended Problem
**Format:**
```bash
[ai-tool] "Write a Python program that [task description] with these requirements: (1) [req1], (2) [req2], (3) [req3]. Include comments explaining your approach."
```

**Examples:**

**File Processing:**
```bash
claude-code "Write a Python program that reads a CSV file of student grades and generates a summary report with: (1) average grade per student, (2) highest and lowest grades, (3) grade distribution. Include error handling."
```

**Data Processing:**
```bash
gemini "Write a Python program that analyzes a text file and outputs: word count, most common words (top 10), average word length, and reading time estimate. Make it handle large files efficiently."
```

#### Template 2: Extension Request
**Format:**
```bash
[ai-tool] "I have this working code: [paste code]. Extend it to also [new feature]. Maintain the existing functionality and keep code clean."
```

**Example:**
```bash
claude "I have this calculator:

```python
def calculate(num1, num2, operation):
    if operation == 'add':
        return num1 + num2
    elif operation == 'subtract':
        return num1 - num2
```

Extend it to handle multiplication, division, and power operations. Add input validation."
```

#### Template 3: Optimization Request
**Format:**
```bash
[ai-tool] "Optimize this code for [readability/performance/memory]: [paste code]. Explain what changes you made and why."
```

### Phase 5: Post-Challenge Comparison

#### Template 1: Approach Comparison
**Format:**
```bash
[ai-tool] "Compare these two approaches to [problem]:

Approach 1: [student code]
Approach 2: [alternative approach]

Which is better and why? Consider readability, efficiency, and Pythonic style."
```

#### Template 2: Alternative Solutions
**Format:**
```bash
[ai-tool] "I solved [problem] this way: [paste code]. Show 2 completely different approaches to the same problem. Explain when each would be preferred."
```

## Topic-Specific Prompt Collections

### Variables & Data Types

**Exploration:**
```bash
gemini "Show 5 interesting things you can do with Python string formatting. Include f-strings, .format(), and % formatting with creative examples."
```

**Debugging:**
```bash
claude "Explain this Python error: 'TypeError: can only concatenate str (not int) to str'. Why does it happen and how do I fix it?"
```

**Creative:**
```bash
claude-code "Write a Python program that converts temperatures between Celsius, Fahrenheit, and Kelvin. Include input validation and clear output formatting."
```

### Conditionals

**Exploration:**
```bash
gemini "Show 4 different ways to write conditional logic in Python: if-elif-else, ternary operator, match-case (Python 3.10+), and dictionary mapping. When would you use each?"
```

**Debugging:**
```bash
claude "This code doesn't work as expected:

```python
age = input('Enter age: ')
if age >= 18:
    print('Adult')
else:
    print('Minor')
```

Explain the bug and the correct solution."
```

### Loops

**Exploration:**
```bash
gemini "Show creative uses of Python loops: generating patterns, processing data, creating animations, solving puzzles. Give 5 examples with code."
```

**Debugging:**
```bash
claude "Why does this create an infinite loop?

```python
i = 0
while i < 10:
    print(i)
    if i == 5:
        continue
    i += 1
```

Explain and fix it."
```

**Creative:**
```bash
claude-code "Write a Python program using nested loops that creates ASCII art of your choice. It should be at least 10x10 characters and use different symbols."
```

### Functions

**Exploration:**
```bash
gemini "Explain Python function parameters in depth: positional, keyword, default, *args, **kwargs. Give clear examples of when to use each."
```

**Debugging:**
```bash
claude "This function doesn't work:

```python
def add_to_list(item, my_list=[]):
    my_list.append(item)
    return my_list

print(add_to_list(1))  # [1]
print(add_to_list(2))  # [1, 2] - Why?
```

Explain this Python gotcha."
```

**Creative:**
```bash
claude-code "Write a Python program with functions that simulates a simple banking system: create account, deposit, withdraw, check balance. Use function parameters effectively."
```

### Lists & Data Structures

**Exploration:**
```bash
gemini "Compare Python lists, tuples, sets, and dictionaries. For each: show creation syntax, common operations, time complexity, and when to use vs. alternatives."
```

**Debugging:**
```bash
claude "Why does this code modify both lists?

```python
list1 = [1, 2, 3]
list2 = list1
list2.append(4)
print(list1)  # [1, 2, 3, 4] - Why?
```

Explain Python's reference behavior."
```

**Creative:**
```bash
claude-code "Write a Python program that manages a to-do list using appropriate data structures. Support: add task, complete task, view tasks, filter by status."
```

### File I/O

**Exploration:**
```bash
gemini "Show different ways to read files in Python: read(), readlines(), line-by-line iteration, with statement, pathlib. Explain when to use each."
```

**Debugging:**
```bash
claude "This code leaves files open:

```python
file = open('data.txt', 'r')
data = file.read()
print(data)
```

Why is this bad? Show the correct approach."
```

**Creative:**
```bash
claude-code "Write a Python program that reads a log file, counts error messages, and writes a summary report to a new file. Handle file not found errors gracefully."
```

### Object-Oriented Programming

**Exploration:**
```bash
gemini "Explain Python OOP concepts: classes, objects, methods, inheritance, composition. Use a real-world analogy (like modeling vehicles) with complete code."
```

**Debugging:**
```bash
claude "This class has a bug:

```python
class Counter:
    count = 0

    def increment(self):
        count += 1
```

Why doesn't it work? Explain self and class variables."
```

**Creative:**
```bash
claude-code "Create a Python class hierarchy for a library system: Book, Member, Library. Include methods for borrowing, returning, and searching books. Use inheritance appropriately."
```

### Error Handling

**Exploration:**
```bash
gemini "Show Python exception handling patterns: try-except, except with specific exceptions, try-except-else-finally, custom exceptions. Give use cases for each."
```

**Debugging:**
```bash
claude "What's wrong with this exception handling?

```python
try:
    result = 10 / 0
except:
    pass
```

Explain why this is bad practice and show better approaches."
```

**Creative:**
```bash
claude-code "Write a Python program that validates user input for a registration form. Handle various errors: empty fields, invalid email format, weak password. Provide helpful error messages."
```

## Advanced Prompt Techniques

### Chain of Thought Prompting
Encourage AI to show reasoning:
```bash
[ai-tool] "Walk through solving this problem step-by-step: [problem]. Explain your reasoning at each step before writing code."
```

### Constraint-Based Prompting
Make AI work within limitations:
```bash
[ai-tool] "Solve [problem] using ONLY [specific features]. Don't use [restricted features]. Explain why your approach works with these constraints."
```

**Example:**
```bash
gemini "Sort a list of numbers without using .sort() or sorted(). Explain your algorithm and why it works."
```

### Comparison Prompting
Get AI to evaluate options:
```bash
[ai-tool] "Compare these three approaches to [problem]:
1. [approach 1]
2. [approach 2]
3. [approach 3]

Which is best for: (a) beginners, (b) production code, (c) performance-critical applications? Explain."
```

### Socratic Prompting
Have AI teach through questions:
```bash
[ai-tool] "Don't solve this directly. Instead, ask me 3-5 questions that would help me solve: [problem]"
```

### Error-Injection Prompting (for creating bugs)
```bash
[ai-tool] "Write Python code that [task] but include a subtle bug related to [concept]. The bug should be realistic and educational."
```

**Example:**
```bash
claude "Write a function to calculate factorial but include a subtle bug with recursion. Make it look almost correct."
```

## Prompt Quality Guidelines

### ✅ Good Prompts
- **Specific:** "Show 3 ways to reverse a string in Python"
- **Structured:** "Explain X with: definition, example, use cases"
- **Contextual:** "For a beginner who just learned loops..."
- **Actionable:** "Show code that I can run and test"

### ❌ Poor Prompts
- **Vague:** "Tell me about Python"
- **Too Broad:** "Teach me everything about functions"
- **Ambiguous:** "Make this better" (without context)
- **Incomplete:** "Fix my code" (without showing code)

## Student Prompt Training Progression

### Week 1-2: Basic Prompts
Students learn to:
- Ask for code examples
- Request explanations
- Get multiple approaches

**Template:**
```
"Show me [N] ways to [task]"
```

### Week 3-4: Structured Prompts
Students learn to:
- Add requirements
- Specify format
- Request comparisons

**Template:**
```
"Show [N] ways to [task] with: code examples, when to use each, and trade-offs"
```

### Week 5-6: Advanced Prompts
Students learn to:
- Add constraints
- Request optimizations
- Ask for debugging help

**Template:**
```
"[Task] with constraints: [list]. Compare your solution with [alternative]. Explain trade-offs."
```

### Week 7+: Expert Prompts
Students learn to:
- Chain requests
- Request specific analysis
- Guide AI toward pedagogical goals

**Template:**
```
"Solve [problem] step-by-step. For each step: explain reasoning, show code, identify potential bugs. Then compare your approach with [alternative method]."
```

## Common Prompt Mistakes & Fixes

### Mistake 1: Too Vague
**Bad:** "Help with loops"
**Good:** "Show 3 ways to iterate over a dictionary in Python and explain when to use each"

### Mistake 2: No Context
**Bad:** "Is this code good?"
**Good:** "Review this code for a beginner learning functions. Identify style issues and suggest improvements: [code]"

### Mistake 3: Asking AI to Do All Work
**Bad:** "Write my homework: create a grade calculator"
**Good:** "I wrote this grade calculator [code]. Suggest improvements for error handling without rewriting everything"

### Mistake 4: Not Specifying Output Format
**Bad:** "Teach me about classes"
**Good:** "Explain Python classes with: simple example, real-world analogy, common mistakes, and a practice problem"

### Mistake 5: Single-Shot for Complex Topics
**Bad:** "Explain everything about OOP"
**Good:**
- First: "Explain what Python classes are with a simple example"
- Then: "Now explain inheritance with an example that extends the previous class"
- Finally: "Show when to use composition instead of inheritance"

## Ethical AI Use Prompts

### Learning vs. Cheating Detection
**Appropriate:**
```bash
claude "I wrote this code [paste code]. Explain what it does line-by-line so I can understand it better."
```

**Inappropriate:**
```bash
"Write my homework assignment: [full assignment]"
```

### Verification Prompts
After AI generates code, students should ask:
```bash
"Explain why this approach works and what would happen if I changed [specific part]."
```

### Attribution Prompts
When using AI-generated code:
```bash
"I used AI to generate this [part]. Help me rewrite it in my own style while keeping the core logic."
```

## Quick Reference: Prompt Starters by Intent

| Intent | Prompt Starter |
|--------|---------------|
| Multiple approaches | "Show [N] different ways to..." |
| Explanation | "Explain [concept] as if teaching..." |
| Debugging | "This code has a bug: [code]. Explain..." |
| Optimization | "Optimize this for [goal]: [code]" |
| Comparison | "Compare [A] vs [B] for [use case]" |
| Extension | "Extend this code to also: [feature]" |
| Review | "Review this code for: [criteria]" |
| Creative | "Write a program that [requirements]" |
| Learning | "Teach me [concept] with [format]" |
| Verification | "Explain why [code] works and..." |

## Saving Effective Prompts

Students should maintain a "prompt library":

```markdown
# My Python Learning Prompts

## Loops
- Best prompt: "Show 4 ways to iterate..."
- Learned: AI shows for loop, while, comprehension, enumerate

## Functions
- Best prompt: "Explain *args and **kwargs with examples"
- Learned: Flexible parameters for functions

## Debugging
- Best prompt: "This error means... explain causes and fixes"
- Learned: How to interpret error messages
```

This helps students:
1. Remember what worked
2. Refine prompts over time
3. Share with classmates
4. Build AI collaboration skills
