---
name: aidd-python-book
description: "Generate comprehensive Python educational chapters using the AI-Driven Development (AIDD) pedagogical approach. Creates lesson plans that balance manual coding practice with AI tool integration, ensuring students learn syntax, problem-solving, and effective AI collaboration. Use when creating educational content, lesson plans, or book chapters for teaching Python in the AI era."
version: 1.0
---

# AIDD Python Book Chapter Generator

## Overview

This skill helps you generate Python educational content using the **AI-Driven Development (AIDD)** pedagogical approach. This methodology ensures students genuinely learn programming fundamentals while developing modern AI collaboration skills.

## Core AIDD Philosophy

**The Five-Phase Learning Framework:**
1. **Manual Concept Discovery** - Build foundational understanding through hands-on coding
2. **AI Exploration & Comparison** - Expand perspective by seeing multiple approaches
3. **Reverse Engineering & Debugging** - Cement syntax through problem-solving
4. **Creative AI Collaboration** - Apply knowledge with AI assistance
5. **Manual Reinforcement Challenge** - Ensure independence from AI tools

**Key Principle:** Manual practice builds understanding → AI expands perspective → Debugging cements syntax → Reflection builds mastery

## When to Use This Skill

Use this skill when you need to:
- Generate a full lesson plan for teaching a Python topic
- Create a book chapter following AIDD methodology
- Design exercises that balance manual and AI-assisted learning
- Structure assessments that test both coding ability and AI collaboration
- Develop content for modern Python education (post-2023)

## Chapter Generation Workflow

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
- v1.0 (2025): Initial release with 5-phase AIDD framework
