# AIDD Chapter Templates

This file contains copy-paste templates for quickly generating AIDD-compliant Python chapters.

## Full Chapter Template

```markdown
# Week [N]: [Topic Name] in the AI Era

## Module Context

This comes after students have already learned about [previous topics].

**Goal:** Students will understand and use [core concept] both manually and in collaboration with AI copilots like Gemini CLI and Claude Code.

## 🎯 Learning Objectives

By the end of the week, students will be able to:

1. [Manual skill - e.g., "Write and execute X manually in Python"]
2. [Conceptual understanding - e.g., "Understand how X works internally"]
3. [AI collaboration - e.g., "Prompt AI tools to generate, explain, and optimize X"]
4. [Debugging - e.g., "Debug and rewrite AI-generated code to solidify syntax understanding"]
5. [Synthesis - e.g., "Compare manual and AI approaches to develop algorithmic reasoning"]

## 📚 Lesson Flow (90 minutes)

### 🧩 Phase 1: Manual Concept Discovery (30 minutes)

**Instructor Demo:**

```python
# [Simplest example of the concept]
```

**Explain:**
- [Key concept 1]
- [Key concept 2]
- [What happens internally]

**Student Activity 1:**
Write the following by hand:
1. [Exercise 1]
2. [Exercise 2]
3. [Exercise 3]

**Discussion Question:**
"[Question that explores edge cases or reasoning]"

This builds manual logic understanding before any AI involvement.

### 🤖 Phase 2: AI Exploration & Comparison (25 minutes)

**Prompt 1 (Gemini CLI):**

```bash
gemini "[Prompt that requests multiple approaches and explanations]"
```

Students review output — for example:

```python
# Approach 1: [Description]
[code]

# Approach 2: [Description]
[code]

# Approach 3: [Description]
[code]
```

**Instructor Task:**
Ask students:
- Which method is clearest?
- Which uses more memory?
- Which would you use in production?

**Mini Reflection:**
"What did the AI code get right? What could you simplify?"

### 🧠 Phase 3: Reverse Engineering & Debugging (20 minutes)

**Instructor Setup:**
Give students an AI-generated buggy script:

```python
# [Intentionally buggy code]
```

**Ask:**
- "Why does this [fail/produce wrong output]?"
- "How would you fix it?"

**Expected fix:**

```python
# [Corrected code]
```

**Then:** Ask Claude Code to explain the bug and compare its reasoning with the students' answers.

Students learn both syntax and error reasoning.

### 💡 Phase 4: Creative AI Collaboration (10 minutes)

**Prompt 2 (Claude Code):**

```bash
"Write a Python program that [open-ended problem description]."
```

AI outputs code.

Students are asked to:
1. Explain what [specific part] controls.
2. Rewrite part of it manually to [modification requirement].

**Bonus:**
Ask the AI to optimize for [readability/performance] and discuss the trade-offs.

### 🧱 Phase 5: Manual Reinforcement Challenge (15 minutes)

**No AI allowed for this part.**

Students must code manually:

"[Clear, specific problem that uses the day's concept]"

Then verify with the class and compare with how the AI might have done it.

## 🧪 Homework / Practice Tasks

**AI Interaction:**
Ask [AI tool]:
```
"[Prompt for creative exploration]"
```
Pick one and modify it manually to [requirement].

**Manual Task:**
Write a Python script that [specific requirement].

**Reflection Journal:**
- What syntax patterns do you now recognize by sight?
- How did AI help you understand [concept] — not just generate them?

## 🧭 Assessment (10 points)

| Criterion | Description | Points |
|-----------|-------------|--------|
| Manual [topic] correctness | Accurate, working Python syntax | 3 |
| AI collaboration | Effective prompt use and explanation | 3 |
| Debugging reasoning | Clear identification and fix of logic errors | 2 |
| Reflection clarity | Insight into what AI helped explain | 2 |

## 🧠 Teaching Notes

**Key Points:**
- [Important concept to emphasize]
- [Common student misconception]
- [Extension opportunities]

**Common Struggles:**
- [Challenge 1 and how to help]
- [Challenge 2 and how to help]

**Teaching Philosophy Reinforced:**
1️⃣ Manual builds understanding
2️⃣ AI expands perspective
3️⃣ Debugging cements syntax
4️⃣ Reflection builds mastery
```

## Phase 1 Template (Detailed)

```markdown
### 🧩 Phase 1: Manual Concept Discovery (30 minutes)

**Learning Goal:** Students understand [concept] without AI assistance

**Instructor Demo (5 minutes):**

```python
# Start with the simplest possible example
[minimal working code]
```

**Key Points to Explain:**
1. **Syntax:** What each part means
   - `[syntax element]` → [explanation]
   - `[syntax element]` → [explanation]

2. **Execution:** What happens when code runs
   - Step 1: [execution detail]
   - Step 2: [execution detail]
   - Step 3: [execution detail]

3. **Memory/Internal Behavior:** What's happening under the hood
   - [Memory/state explanation]

**Student Practice (20 minutes):**

**Exercise 1 (Basic):**
```
[Clear instruction]
Expected output: [show output]
```

**Exercise 2 (Intermediate):**
```
[Slightly more complex instruction]
Expected output: [show output]
```

**Exercise 3 (Application):**
```
[Apply concept to new scenario]
Expected output: [show output]
```

**Discussion Question (5 minutes):**

"[Open-ended question that makes students think about edge cases, efficiency, or when to use this approach]"

**Possible Answers:**
- [Answer direction 1]
- [Answer direction 2]
- [Common misconception to address]

**Transition to Phase 2:**
"Now that you understand how to [concept] manually, let's see how AI approaches the same problem..."
```

## Phase 2 Template (AI Exploration)

```markdown
### 🤖 Phase 2: AI Exploration & Comparison (25 minutes)

**Learning Goal:** Students see multiple approaches and learn to evaluate code quality

**Setup (2 minutes):**
Introduce the AI tool and prompt structure

**Prompt Activity (8 minutes):**

**Prompt 1 - Multiple Approaches:**
```bash
[ai-tool] "Show [N] different ways to [task] in Python. For each approach, explain: (1) when to use it, (2) pros and cons, (3) efficiency considerations."
```

**Expected AI Output:**
```python
# Approach 1: [Name]
# Use when: [scenario]
# Pros: [benefits]
# Cons: [drawbacks]
[code example]

# Approach 2: [Name]
# Use when: [scenario]
# Pros: [benefits]
# Cons: [drawbacks]
[code example]

# Approach 3: [Name]
# Use when: [scenario]
# Pros: [benefits]
# Cons: [drawbacks]
[code example]
```

**Critical Analysis (15 minutes):**

**Question Set 1 - Readability:**
- "Which code is easiest to understand? Why?"
- "Which would a beginner find clearest?"
- "Which requires the most Python knowledge to understand?"

**Question Set 2 - Efficiency:**
- "Which approach uses the most memory? Why?"
- "Which would be fastest for [specific use case]?"
- "Does efficiency matter for this problem size?"

**Question Set 3 - Best Practices:**
- "Which follows Python conventions (PEP 8) best?"
- "Which would you use in production code? Why?"
- "Are there any approaches you'd never use? Why not?"

**Mini Reflection:**
Students write 2-3 sentences:
- "What did the AI teach you that you didn't know before?"
- "What could be simplified or improved in the AI's code?"
- "Which approach matches how you think about the problem?"
```

## Phase 3 Template (Debugging)

```markdown
### 🧠 Phase 3: Reverse Engineering & Debugging (20 minutes)

**Learning Goal:** Students develop debugging skills and deepen syntax understanding

**Bug Scenario Setup (3 minutes):**

**Context:**
"An AI tool generated this code for [purpose], but there's a bug. Your job is to find and fix it."

**The Buggy Code:**
```python
# Bug Type: [Infinite loop / Logic error / Syntax error / etc.]
[intentionally broken code]
```

**Expected Behavior:**
```
[What it should do]
```

**Actual Behavior:**
```
[What it actually does / error message]
```

**Student Debugging Process (10 minutes):**

**Step 1 - Identify:**
"Read the code carefully. Where do you think the bug is? Mark the problematic line(s)."

**Step 2 - Explain:**
"Why is this a problem? What would happen when this code runs?"

**Step 3 - Fix:**
"How would you fix it? Write the corrected code."

**Step 4 - Verify:**
"How can you test that your fix works? What test cases should you try?"

**The Fix:**
```python
# Corrected version with comments explaining changes
[fixed code with annotations]
```

**Key Learning Points:**
- [What this bug teaches about the concept]
- [Common pattern to watch for]

**AI Comparison (7 minutes):**

**Prompt Claude Code:**
```bash
"This code has a bug: [paste buggy code]. Explain what's wrong and why, then show the fix."
```

**Discussion:**
- "How did Claude's explanation compare to yours?"
- "Did Claude identify anything you missed?"
- "Did you catch anything Claude didn't explain clearly?"
- "Whose explanation would help a beginner more?"

**Bonus Bug (if time):**
[Optional second buggy code example]
```

## Phase 4 Template (Creative Collaboration)

```markdown
### 💡 Phase 4: Creative AI Collaboration (10 minutes)

**Learning Goal:** Students apply concepts with AI assistance and modify results

**Problem Statement (2 minutes):**

"[Open-ended problem that's slightly challenging]"

**Example:** "Create a program that [achieves goal X] with [constraint Y]."

**Requirements:**
1. [Requirement 1]
2. [Requirement 2]
3. [Requirement 3]

**AI Generation (3 minutes):**

**Prompt Template:**
```bash
claude-code "Write a Python program that [problem description]. Include comments explaining your approach. Consider [edge case/constraint]."
```

**Sample AI Output:**
```python
# AI-generated solution
[working code with comments]
```

**Manual Modification Tasks (5 minutes):**

Students must manually:

**Task 1 - Explain:**
"In your own words, explain what [specific section/function] does. Don't just read the comments—explain why it works."

**Task 2 - Modify:**
"Change the code to [new requirement]. You must edit the code yourself, not ask AI to do it."

**Task 3 - Optimize:**
"Rewrite [section] to be more [readable/efficient/Pythonic]. Explain your changes."

**Trade-off Discussion:**
- "What trade-offs did the AI make in its solution?"
- "When would you choose [AI's approach] vs [alternative approach]?"
- "How would you explain this code to someone who's just learning Python?"

**Extension (if advanced students):**
"Ask the AI to optimize for [performance/readability]. What changes does it make? Are they worth it?"
```

## Phase 5 Template (Manual Challenge)

```markdown
### 🧱 Phase 5: Manual Reinforcement Challenge (15 minutes)

**⚠️ CRITICAL RULE: NO AI TOOLS ALLOWED**

**Learning Goal:** Prove independent coding capability

**Challenge Setup (2 minutes):**

**The Problem:**
"[Clear, specific problem using today's concept in a new context]"

**Requirements:**
1. [Requirement 1]
2. [Requirement 2]
3. [Requirement 3]

**Success Criteria:**
- [ ] [Criterion 1]
- [ ] [Criterion 2]
- [ ] [Criterion 3]

**Time Limit:** [10-15] minutes

**Rules:**
- ❌ No AI tools (Gemini, Claude, Copilot, etc.)
- ❌ No searching Google/Stack Overflow
- ✅ Notes from today's lesson allowed
- ✅ Python documentation allowed
- ✅ Asking clarifying questions allowed

**Individual Work (10-12 minutes):**

Students code in silence. Instructor circulates to:
- Answer clarification questions only
- Observe common struggles
- Note who finishes early vs. who struggles

**Class Verification (3 minutes):**

1. **Volunteer shares solution** (or instructor shows reference solution)
2. **Quick discussion:**
   - "Did anyone approach it differently?"
   - "What was the trickiest part?"
   - "What syntax from Phase 1 did you use?"

**Reference Solution:**
```python
# One possible correct solution
[clean, well-commented code]
```

**Optional AI Comparison (if time):**
"Now let's see how Claude would solve it..."
```bash
gemini "[same problem statement]"
```

**Compare:**
- "How similar is AI's approach to yours?"
- "What did AI do that you didn't? Vice versa?"
- "Whose code is more readable?"

**Key Message:**
"You can now solve this without AI. That's the goal—AI is a tool to enhance your skills, not replace them."
```

## Assessment Rubric Template

```markdown
## 🧭 Assessment (10 points)

### Detailed Rubric

| Criterion | Exemplary (Full Points) | Proficient (Partial Points) | Developing (Minimal Points) | Points |
|-----------|------------------------|----------------------------|----------------------------|--------|
| **Manual [Topic] Correctness (3 pts)** | Code runs perfectly, uses correct syntax, handles edge cases, well-formatted | Code runs with minor issues OR missing edge cases OR poor formatting | Code has logic errors, syntax mistakes, or doesn't run | __/3 |
| **AI Collaboration (3 pts)** | Prompts are clear and specific; AI-generated code is well-explained; modifications are meaningful and correct | Prompts work but are vague OR explanations are superficial OR modifications have minor errors | Prompts are ineffective OR can't explain AI code OR modifications don't work | __/3 |
| **Debugging Reasoning (2 pts)** | Clearly identifies bugs, explains why they occur, provides correct fixes with reasoning | Identifies bugs but explanation is unclear OR fix is correct but poorly explained | Cannot identify bugs OR provides incorrect fixes | __/2 |
| **Reflection Clarity (2 pts)** | Deep insights about learning process; specific examples of what AI helped with; metacognitive awareness | General reflection with some specifics OR mentions AI role but lacks depth | Vague reflection OR doesn't address how AI aided learning | __/2 |
| **TOTAL** | | | | __/10 |

### Grading Examples

**Manual Correctness - Full Credit (3/3):**
```python
# Clean, working code with proper structure
[example code]
```
✓ Correct syntax
✓ Handles edge cases
✓ Good variable names
✓ Proper indentation

**Manual Correctness - Partial Credit (1-2/3):**
- Code works but has style issues (2pts)
- Code has minor logic errors (1-2pts)
- Code doesn't handle edge cases (1-2pts)

**AI Collaboration - Full Credit (3/3):**
"I prompted Gemini with: '[specific prompt]' which gave me [approach]. I modified the [specific part] to [change] because [reasoning]. This showed me that [insight]."

**Reflection - Full Credit (2/2):**
"Before AI, I thought [concept] was [assumption]. Seeing the AI's three approaches—especially [specific example]—helped me realize [insight]. Now when I write loops, I think about [new consideration] that I didn't before. The debugging exercise taught me to watch for [specific pattern]."
```

## Common Bug Templates by Topic

```markdown
### Loops - Common Bugs

**Bug 1: Infinite Loop**
```python
count = 1
while count < 10:
    print(count)
# Missing: count += 1
```

**Bug 2: Off-by-One Error**
```python
for i in range(10):  # Should be range(1, 11) for 1-10
    print(i)
```

**Bug 3: Wrong Range Step**
```python
for i in range(0, 10, -1):  # Infinite loop - should use positive step
    print(i)
```

### Functions - Common Bugs

**Bug 1: Missing Return**
```python
def calculate_sum(a, b):
    total = a + b
    # Missing: return total
```

**Bug 2: Parameter Mismatch**
```python
def greet(name, age):
    return f"Hi {name}"

greet("Alice")  # Missing age parameter
```

**Bug 3: Scope Issues**
```python
def increment():
    count += 1  # UnboundLocalError - count not defined
    return count

count = 0
increment()
```

### Lists - Common Bugs

**Bug 1: Index Error**
```python
numbers = [1, 2, 3]
print(numbers[3])  # IndexError: list index out of range
```

**Bug 2: Mutability Confusion**
```python
def add_item(lst, item):
    lst = lst + [item]  # Creates new list, doesn't modify original
    return lst

my_list = [1, 2]
add_item(my_list, 3)
print(my_list)  # Still [1, 2]
```

**Bug 3: Modifying While Iterating**
```python
numbers = [1, 2, 3, 4, 5]
for num in numbers:
    if num % 2 == 0:
        numbers.remove(num)  # Dangerous - modifies during iteration
```
```

## Homework Template

```markdown
## 🧪 Homework / Practice Tasks

### Assignment Overview
**Due:** [Date/time]
**Submission:** [Method]
**Estimated Time:** [30-45] minutes

### Part 1: AI Exploration (15 minutes)

**Task:**
Use [AI tool] to explore creative applications of [today's concept].

**Prompt:**
```bash
[ai-tool] "[Prompt for creative/advanced uses]"
```

**Deliverable:**
1. Copy the AI's response
2. Choose ONE example that interests you
3. Manually modify it to [specific change]
4. Write 3-4 sentences explaining:
   - What the original code does
   - What you changed and why
   - One thing you learned from the AI's approach

**Example Submission:**
```
AI generated: [paste code]

I chose the [example name] because [reason].

I modified [specific part] to [change] by [method].

This taught me that [insight].
```

### Part 2: Manual Practice (20 minutes)

**Task:**
Write a Python program **without any AI assistance** that [specific requirement].

**Requirements:**
1. [Requirement 1 - uses today's concept]
2. [Requirement 2 - specific feature]
3. [Requirement 3 - edge case handling]

**Starter Code (optional):**
```python
# You may use this structure or start from scratch
[optional template]
```

**Test Cases:**
Your program should handle:
- Test 1: [Input] → [Expected output]
- Test 2: [Input] → [Expected output]
- Test 3: [Input] → [Expected output]

**Submission:**
- Your complete .py file
- Comments explaining key parts
- Screenshot of successful test runs

### Part 3: Reflection Journal (10 minutes)

Answer these questions in 5-8 sentences total:

1. **Syntax Recognition:**
   "What [concept] patterns do you now recognize by sight? Give a specific example from today."

2. **AI Learning:**
   "How did AI help you understand [concept]—not just generate code? What did you learn from seeing multiple approaches?"

3. **Manual Confidence:**
   "Rate your confidence (1-10) in writing [concept] code manually. What would help you feel more confident?"

4. **Application:**
   "Where might you use [concept] in a real project? Be specific."

**Example Reflection:**
"I now recognize [pattern] immediately—like in today's [example]. Seeing AI's three approaches to [task] taught me [insight]. I feel [confidence level] because [reason]. To improve, I need to [action]. I could use [concept] in [specific project idea]."

### Submission Checklist

Before submitting, verify:
- [ ] Part 1: AI exploration with your modification and explanation
- [ ] Part 2: Complete .py file that passes all test cases
- [ ] Part 3: Reflection answers (5-8 sentences)
- [ ] Code has comments explaining logic
- [ ] No AI was used for Part 2
- [ ] Your name and date in submission
```

## Quick Reference: AIDD Timing Guide

```
Total: 90 minutes

Phase 1: Manual Concept Discovery     → 30 min (33%)
  - Demo: 5-10 min
  - Practice: 15-20 min
  - Discussion: 5 min

Phase 2: AI Exploration               → 25 min (28%)
  - Prompt & generate: 8-10 min
  - Analysis: 12-15 min
  - Reflection: 2-3 min

Phase 3: Debugging                    → 20 min (22%)
  - Bug presentation: 3 min
  - Student debugging: 10 min
  - AI comparison: 7 min

Phase 4: Creative Collaboration       → 10 min (11%)
  - Problem setup: 2 min
  - AI generation: 3 min
  - Manual modification: 5 min

Phase 5: Manual Challenge             → 15 min (17%)
  - Setup: 2 min
  - Individual work: 10-12 min
  - Verification: 3 min

Total: 100 minutes (build in 10-min buffer)
```

## Meta-Template: Custom Topic Checklist

When creating a new chapter, verify:

**Structure:**
- [ ] Module context states prerequisites
- [ ] 5 clear learning objectives
- [ ] All 5 phases present with time allocations
- [ ] Phases total ~90 minutes

**Content Quality:**
- [ ] Phase 1 has runnable code examples
- [ ] Phase 2 names specific AI tools
- [ ] Phase 3 bugs are realistic and educational
- [ ] Phase 4 requires manual modification
- [ ] Phase 5 explicitly bans AI use

**Assessment:**
- [ ] Homework has 3 parts (AI, Manual, Reflection)
- [ ] Rubric totals 10 points
- [ ] Clear examples of full credit work

**Pedagogical Alignment:**
- [ ] Manual practice comes first
- [ ] AI expands rather than replaces learning
- [ ] Debugging cements understanding
- [ ] Reflection prompts metacognition
- [ ] Students can work independently by end
```
