```markdown
---
name: aidd-python-book
description: "Generate comprehensive Python educational chapters using the AI-Driven Development (AIDD) pedagogical approach. Creates lesson plans that balance manual coding practice with AI tool integration, ensuring students learn syntax, problem-solving, and effective AI collaboration. Use when creating educational content, lesson plans, or book chapters for teaching Python in the AI era. Automatically creates separate markdown files for each topic in a documentation site structure."
version: 2.0
---

# AIDD Python Book Chapter Generator

## Overview

This skill helps you generate Python educational content using the **AI-Driven Development (AIDD)** pedagogical approach. This methodology ensures students genuinely learn programming fundamentals while developing modern AI collaboration skills.

**NEW in v2.0:** Automatically generates separate files for each topic in a documentation site structure, ensuring sequential learning with no forward references.

## Documentation Site Generation

### File Organization

When generating chapters, create files in this structure:

```
modern-python/
├── index.md                          # Main navigation/table of contents
├── 01-getting-started.md            # Week 1: Setup and basics
├── 02-variables-and-types.md        # Week 2: Variables
├── 03-conditionals.md               # Week 3: If/else
├── 04-loops.md                      # Week 4: For/while loops
├── 05-functions.md                  # Week 5: Functions
├── 06-lists.md                      # Week 6: Lists
├── 07-dictionaries.md               # Week 7: Dictionaries
├── 08-file-io.md                    # Week 8: File handling
├── 09-error-handling.md             # Week 9: Try/except
├── 10-oop-basics.md                 # Week 10: Classes
├── 11-oop-advanced.md               # Week 11: Inheritance
├── 12-modules-packages.md           # Week 12: Imports
└── README.md                        # Project overview
```

### File Generation Rules

**CRITICAL RULES for Sequential Learning:**

1. **Self-Contained Chapters**
   - Each file must be complete and standalone
   - Explain everything needed for that topic
   - No assumptions about future chapters

2. **No Forward References**
   - NEVER mention topics not yet covered
   - Don't say "we'll learn about X later"
   - Don't use syntax/concepts from future chapters
   - If you need something not covered yet, explain it briefly inline

3. **Clear Prerequisites**
   - State exactly what prior chapters are needed
   - Reference specific chapter numbers
   - Quick recap of essential prior concepts

4. **Progressive Complexity**
   - Start simple, build gradually
   - Each chapter slightly harder than previous
   - Concepts build on each other naturally

5. **Consistent Format**
   - Every file follows same AIDD 5-phase structure
   - Same heading hierarchy
   - Same assessment format

## When to Use This Skill

Use this skill when you need to:
- Generate a full lesson plan for teaching a Python topic
- Create a book chapter following AIDD methodology
- Design exercises that balance manual and AI-assisted learning
- Structure assessments that test both coding ability and AI collaboration
- Develop content for modern Python education (post-2023)
- **Build a complete Python documentation site with sequential chapters**
- **Generate individual chapter files in a structured directory**

## File Generation Workflow

### Step 1: Setup Directory Structure

When user provides a directory path (e.g., "modern-python"), create or use this structure:

```bash
# Create directory if it doesn't exist
mkdir -p modern-python

# Initialize with index and README
# Start generating chapters sequentially
```

### Step 2: Track Chapter Sequence

Maintain awareness of what has been generated:

**Generated Topics:** Keep track in a mental model or explicitly
- Chapter 1: Variables ✅
- Chapter 2: Conditionals ✅
- Chapter 3: Loops ← Currently generating
- Chapter 4: Functions ⏳ Not yet

**When generating Chapter 3 (Loops):**
- ✅ CAN reference: Variables, Conditionals (already covered)
- ❌ CANNOT reference: Functions, Lists, OOP (not covered yet)
- If need something not covered: Explain it inline briefly

### Step 3: Generate Complete Chapter File

For each topic, create a complete markdown file:

**Filename format:** `##-topic-name.md`
- Use 2-digit prefix for ordering (01, 02, 03...)
- Use kebab-case for topic name
- Examples: `03-loops.md`, `05-functions.md`, `10-oop-basics.md`

**File content must include:**
1. Chapter title with number
2. Prerequisites section (what chapters to complete first)
3. Complete AIDD 5-phase lesson
4. All code examples (no placeholders)
5. Homework section
6. Assessment rubric
7. Navigation (Previous | Home | Next chapter links)

### Step 4: Update Index File

After generating each chapter, update `index.md` with:
- Chapter number and title
- Brief description
- Status (✅ Complete, ⏳ In Progress, ⬜ Planned)
- Link to the file

### Step 5: Maintain README.md

Keep README.md updated with:
- Total chapters completed
- How to use the documentation
- Suggested learning path
- Prerequisites for starting

## File Template Structure

Each generated chapter file should follow this structure:

```markdown
# Chapter [N]: [Topic Name] in the AI Era

> **Navigation:** [← Previous: Chapter [N-1]](./[prev-file].md) | [Home](./index.md) | [Next: Chapter [N+1] →](./[next-file].md)

## 📋 Chapter Overview

**What You'll Learn:**
- [Objective 1]
- [Objective 2]
- [Objective 3]

**Prerequisites:**
- ✅ Chapter [N-1]: [Topic]
- ✅ Chapter [N-2]: [Topic]

**Time Required:** 90 minutes

**AI Tools Used:** Gemini CLI, Claude Code

---

## 🎯 Learning Objectives

By the end of this chapter, you will be able to:

1. [Manual skill]
2. [Conceptual understanding]
3. [AI collaboration skill]
4. [Debugging skill]
5. [Synthesis skill]

---

## 📚 Lesson Content (90 minutes)

### 🧩 Phase 1: Manual Concept Discovery (30 minutes)

[Complete content - no placeholders]

**Instructor Demo:**
```python
[Complete, runnable code]
```

[Full explanations and activities]

### 🤖 Phase 2: AI Exploration & Comparison (25 minutes)

[Complete content]

### 🧠 Phase 3: Reverse Engineering & Debugging (20 minutes)

[Complete content]

### 💡 Phase 4: Creative AI Collaboration (10 minutes)

[Complete content]

### 🧱 Phase 5: Manual Reinforcement Challenge (15 minutes)

[Complete content]

---

## 🧪 Homework / Practice Tasks

[Complete homework with all 3 parts]

---

## 🧭 Assessment (10 points)

[Complete rubric]

---

## 🔑 Key Takeaways

- [Main concept 1]
- [Main concept 2]
- [Main concept 3]
- [When to use this technique]
- [Common pitfalls to avoid]

---

## 📖 Quick Reference

**Syntax:**
```python
[Key syntax patterns from this chapter]
```

**Common Patterns:**
```python
[Frequently used code patterns]
```

**Common Mistakes:**
```python
# ❌ Wrong
[common mistake]

# ✅ Correct
[correct version]
```

---

## 🚀 What's Next?

In **Chapter [N+1]: [Next Topic]**, you'll learn:
- [Preview 1]
- [Preview 2]
- [Preview 3]

> **Navigation:** [← Previous: Chapter [N-1]](./[prev-file].md) | [Home](./index.md) | [Next: Chapter [N+1] →](./[next-file].md)

---

*Part of the Modern Python with AIDD curriculum*
```

## Chapter Generation Workflow

### IMPORTANT: File Generation Process

When a user requests a chapter, follow these steps:

**Step A: Determine Chapter Number**
- Ask user what chapter number this is (or infer from topic sequence)
- Check what topics have been covered previously
- Identify prerequisites

**Step B: Check Prerequisites**
- List what concepts must be already covered
- Verify no forward references will be made
- Plan what to explain inline if needed

**Step C: Generate Complete File**
- Create file with proper naming: `##-topic-name.md`
- Include ALL content (no "see templates" placeholders)
- Write complete, runnable code examples
- Add navigation links

**Step D: Save to Directory**
- Use `create_file` tool to write to specified directory
- Path format: `/home/claude/[directory-name]/##-topic-name.md`
- Then copy to outputs: `/mnt/user-data/outputs/[directory-name]/`

**Step E: Update Index**
- Update or create `index.md` in the same directory
- Add new chapter to table of contents
- Mark as complete

**Example Workflow:**
```
User: "Create Chapter 3 on loops in modern-python directory"

Claude:
1. Determines: Chapter 3, topic is loops
2. Prerequisites: Chapters 1-2 (variables, conditionals)
3. Generates complete 03-loops.md file
4. Saves to /home/claude/modern-python/03-loops.md
5. Copies to /mnt/user-data/outputs/modern-python/
6. Updates index.md
7. Provides download link
```

### Step 1: Identify the Topic and Context

Before generating content, clarify:
- **Python Topic**: What specific concept (e.g., loops, functions, OOP, data structures)
- **Week/Module Number**: Where it fits in the curriculum
- **Prerequisites**: What students should already know
- **Duration**: Typical lesson length (default: 90 minutes)
- **Target AI Tools**: Which AI tools students will use (Gemini CLI, Claude Code, GitHub Copilot, etc.)

### Step 2: Generate the Chapter Structure

Every AIDD chapter follows this structure:

```markdown
# Week X: [Topic Name] in the AI Era

## Module Context
- Where this fits in the course
- Prerequisites from previous weeks
- Overall learning goal

## 🎯 Learning Objectives
By the end of the week, students will be able to:
- [Objective 1 - Manual coding skill]
- [Objective 2 - Conceptual understanding]
- [Objective 3 - AI collaboration skill]
- [Objective 4 - Debugging/problem-solving skill]
- [Objective 5 - Synthesis/comparison skill]

## 📚 Lesson Flow (90 minutes)

### 🧩 Phase 1: Manual Concept Discovery (30 minutes)
- Instructor demo with clear explanations
- Student manual coding activity
- Discussion questions that build logical reasoning

### 🤖 Phase 2: AI Exploration & Comparison (25 minutes)
- Structured AI prompts that show multiple approaches
- Critical analysis of AI-generated code
- Efficiency and clarity discussions

### 🧠 Phase 3: Reverse Engineering & Debugging (20 minutes)
- Intentionally buggy code from AI
- Student debugging practice
- AI-assisted explanation comparison

### 💡 Phase 4: Creative AI Collaboration (10 minutes)
- Open-ended problem with AI assistance
- Manual modification of AI code
- Trade-off discussions

### 🧱 Phase 5: Manual Reinforcement Challenge (15 minutes)
- NO AI ALLOWED
- Pure manual coding challenge
- Verification and comparison

## 🧪 Homework / Practice Tasks
- AI Interaction task
- Manual coding task
- Reflection journal prompt

## 🧭 Assessment
[Rubric with 4 criteria: Manual correctness, AI collaboration, Debugging, Reflection]

## 🧠 Teaching Notes
[Key points for instructors]
```

### Step 3: Populate with Topic-Specific Content

Use these guidelines for each phase:

#### Phase 1 - Manual Concept Discovery
**Goal**: Build intuition without AI interference

**Components:**
- Start with simplest example of the concept
- Explain what happens "under the hood" (memory, execution flow)
- Provide 2-3 manual exercises increasing in complexity
- Include a discussion question that explores edge cases or reasoning

**Example Patterns:**
- "Write [simple code] by hand"
- "Explain when [approach A] vs [approach B] would be more appropriate"
- "Why might [common mistake] happen?"

#### Phase 2 - AI Exploration & Comparison
**Goal**: Show students multiple perspectives and best practices

**Components:**
- 1-2 specific AI prompts (with tool names: Gemini CLI, Claude Code)
- Expected AI output with 2-4 different approaches
- Instructor-led comparison questions:
  - "Which method is clearest?"
  - "Which uses more memory/time?"
  - "Which would you use in production?"
- Mini reflection on AI code quality

**AI Tool Prompt Templates:**
```
gemini "Show [N] different ways to [task] in Python and explain efficiency."

claude-code "Write a Python program that [description] and explain your approach."

copilot (comment prompt)
# Generate a [function/class] that [specification]
# Consider edge cases: [list cases]
```

#### Phase 3 - Reverse Engineering & Debugging
**Goal**: Learn syntax through fixing mistakes

**Components:**
- Provide intentionally buggy AI-generated code (1-2 bugs)
- Common mistakes related to the topic:
  - Off-by-one errors
  - Missing increments in loops
  - Incorrect indentation
  - Type mismatches
  - Logic errors
- Guided questions: "Why does this fail?" "How would you fix it?"
- Compare student reasoning with AI's explanation

**Bug Types by Topic:**
- Loops: Infinite loops, wrong range, incorrect increment
- Functions: Missing return, parameter mismatch, scope issues
- Data Structures: Index errors, key errors, mutation bugs
- OOP: Missing self, wrong inheritance, attribute errors

#### Phase 4 - Creative AI Collaboration
**Goal**: Build confidence in AI-assisted problem solving

**Components:**
- Open-ended problem slightly beyond current skill level
- Students prompt AI and get working code
- Required manual modifications:
  - "Explain what [specific part] does"
  - "Rewrite [section] to [new requirement]"
  - "Optimize for [readability/performance]"
- Discussion of trade-offs

**Problem Complexity Guideline:**
- Should take AI ~30 seconds to generate
- Should require student understanding to modify correctly
- Should have multiple valid approaches

#### Phase 5 - Manual Reinforcement Challenge
**Goal**: Prove independent capability

**Components:**
- **Strictly NO AI allowed** - make this explicit
- Time-boxed (10-15 minutes)
- Problem uses the day's concept applied to new scenario
- Students must code from scratch
- Verify together as class
- Optional: Compare with how AI might approach it (after completion)

**Challenge Characteristics:**
- Slightly easier than Phase 4
- Uses the exact syntax/patterns taught
- Clear success criteria
- Should be completable manually

### Step 4: Create Homework Assignments

Every homework should have three components:

1. **AI Interaction Task**
   - Prompt AI for creative applications or variations
   - Require students to pick and modify one example
   - Focus on exploration and understanding

2. **Manual Task**
   - Pure coding without AI
   - Reinforces the core concept
   - Should take 15-30 minutes

3. **Reflection Journal**
   - "What syntax patterns do you now recognize?"
   - "How did AI help you understand [concept]?"
   - Metacognitive practice

### Step 5: Design Assessment Rubric

Standard 10-point rubric structure:

| Criterion | Description | Points |
|-----------|-------------|--------|
| Manual coding correctness | Accurate, working Python syntax | 3 |
| AI collaboration | Effective prompt use and code explanation | 3 |
| Debugging reasoning | Clear identification and fix of logic errors | 2 |
| Reflection clarity | Insight into what AI helped explain | 2 |

## Core AIDD Philosophy

**The Five-Phase Learning Framework:**
1. **Manual Concept Discovery** - Build foundational understanding through hands-on coding
2. **AI Exploration & Comparison** - Expand perspective by seeing multiple approaches
3. **Reverse Engineering & Debugging** - Cement syntax through problem-solving
4. **Creative AI Collaboration** - Apply knowledge with AI assistance
5. **Manual Reinforcement Challenge** - Ensure independence from AI tools

**Key Principle:** Manual practice builds understanding → AI expands perspective → Debugging cements syntax → Reflection builds mastery

## Topic-Specific Guidance

### Common Python Topics and Key Focus Areas

**Variables & Data Types**
- Manual: Type conversion, variable naming, memory concepts
- AI Focus: Multiple ways to format strings, type checking patterns
- Common Bugs: Type errors, undefined variables, scope issues

**Conditionals**
- Manual: Boolean logic, if-elif-else structure, comparison operators
- AI Focus: Complex conditions, guard clauses, early returns
- Common Bugs: Wrong indentation, missing colons, logic errors

**Loops (for, while, comprehensions)**
- Manual: Iteration mechanics, range usage, break/continue
- AI Focus: List comprehensions, nested loops, loop optimization
- Common Bugs: Infinite loops, off-by-one errors, wrong increments

**Functions**
- Manual: Parameter passing, return values, function calls
- AI Focus: Default parameters, *args/**kwargs, lambda functions
- Common Bugs: Missing return, parameter mismatch, scope confusion

**Data Structures (Lists, Dicts, Sets, Tuples)**
- Manual: CRUD operations, indexing, iteration
- AI Focus: Comprehensions, common patterns, when to use each
- Common Bugs: Index out of range, key errors, mutation issues

**Object-Oriented Programming**
- Manual: Class definition, attributes, methods, instantiation
- AI Focus: Inheritance, composition, special methods
- Common Bugs: Missing self, wrong super() usage, attribute errors

**File I/O**
- Manual: Reading/writing files, with statement, paths
- AI Focus: Context managers, error handling, different formats
- Common Bugs: File not found, not closing files, encoding issues

**Error Handling**
- Manual: try-except blocks, exception types
- AI Focus: Custom exceptions, exception chaining, logging
- Common Bugs: Catching too broad, swallowing errors, wrong exception type

**Modules & Packages**
- Manual: Importing, creating modules, __main__ pattern
- AI Focus: Package structure, __init__.py, relative imports
- Common Bugs: Circular imports, module not found, name conflicts

## Best Practices

### Do's ✅
- **Always start with manual practice** before introducing AI
- **Use specific AI tool names** (Gemini CLI, Claude Code, not just "AI")
- **Include the actual code** in examples, not just descriptions
- **Make bugs realistic** - errors students would actually make
- **Time-box each phase** - keeps lesson moving
- **Require manual completion** in Phase 5 - non-negotiable
- **Balance breadth and depth** - don't overwhelm with too many concepts

### Don'ts ❌
- **Don't skip Phase 1** - manual foundation is critical
- **Don't make AI optional** - it's core to the methodology
- **Don't use vague prompts** - show exact commands students should use
- **Don't make debugging trivial** - bugs should require thought
- **Don't allow AI in Phase 5** - defeats the purpose
- **Don't forget reflection** - metacognition is key to learning
- **Don't assume prior AI experience** - teach prompting explicitly

## Example Prompts for Content Generation

When a user requests chapter generation, use these patterns:

**For a new chapter:**
```
User: "Create an AIDD chapter on Python dictionaries"

Generate:
1. Module context and prerequisites
2. 5 learning objectives (manual + AI + debugging + synthesis)
3. 5-phase lesson structure with timings
4. Specific code examples for each phase
5. Homework with 3 components
6. 10-point assessment rubric
```

**For expanding a section:**
```
User: "Expand Phase 3 for the functions chapter"

Provide:
1. 2-3 buggy code examples
2. Guided debugging questions
3. Common student mistakes
4. AI comparison activity
```

**For creating assessments:**
```
User: "Create assessment for OOP chapter"

Generate:
1. 4-criterion rubric (10 points total)
2. Example of excellent work for each criterion
3. Common mistakes that lose points
```

## Quality Checklist

Before delivering a chapter, verify:

- [ ] Module context clearly states prerequisites
- [ ] 5 learning objectives cover manual, AI, and synthesis skills
- [ ] Phase 1 has manual exercises before any AI
- [ ] Phase 2 includes specific AI tool commands
- [ ] Phase 3 has realistic, debuggable code
- [ ] Phase 4 requires manual modification of AI code
- [ ] Phase 5 explicitly prohibits AI use
- [ ] Homework has all 3 components
- [ ] Assessment rubric totals 10 points
- [ ] Teaching notes provide instructor guidance
- [ ] Code examples are complete and runnable
- [ ] Timing adds up to ~90 minutes

## Advanced Features

### Multi-Week Modules
For topics requiring multiple weeks:
- Week 1: Basics with AIDD structure
- Week 2: Intermediate with building on Week 1
- Week 3: Advanced with project synthesis
- Maintain consistent assessment structure

### Project-Based Chapters
When creating project-focused content:
- Phase 1: Manual prototype/planning
- Phase 2: AI-assisted architecture exploration
- Phase 3: Debug common integration errors
- Phase 4: AI helps with extensions
- Phase 5: Manual core feature implementation

### Adaptive Difficulty
Adjust based on student level:
- **Beginner**: More guided prompts, simpler bugs, detailed explanations
- **Intermediate**: Open-ended prompts, complex bugs, efficiency focus
- **Advanced**: Minimal scaffolding, architectural decisions, optimization

## Teaching Philosophy Summary

**AIDD is not about replacing manual coding with AI.**

It's about:
1. Building strong fundamentals through manual practice
2. Expanding perspective by seeing AI's approaches
3. Developing debugging skills through error correction
4. Learning effective AI collaboration
5. Ensuring students can code independently

Students should leave able to:
- ✅ Write Python code from scratch without AI
- ✅ Understand and debug both their own and AI-generated code
- ✅ Prompt AI effectively for complex problems
- ✅ Make informed decisions about when to use AI
- ✅ Explain their code and reasoning clearly

## Usage Examples

**Example 1: Generate a full chapter**
```
"Create an AIDD chapter for Week 5 on Python functions.
Students have already learned variables, conditionals, and loops."
```

**Example 2: Focus on specific phase**
```
"Create Phase 2 (AI Exploration) activities for teaching list comprehensions.
Show 4 different approaches and comparison questions."
```

**Example 3: Assessment creation**
```
"Generate a 10-point rubric for assessing student work on a file I/O chapter,
with examples of what earns full points vs. partial points."
```

**Example 4: Homework design**
```
"Create homework assignments for error handling that include
AI exploration, manual practice, and reflection."
```

## Version History
- v2.0 (2025): Added file generation, sequential learning enforcement, documentation site structure
- v1.0 (2025): Initial release with 5-phase AIDD framework
```
