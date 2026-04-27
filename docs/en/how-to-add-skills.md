# How to Add New Methods

## Core Principle

**Each analysis method = one standalone `.md` file**.

Contributors don't need to understand the entire framework — just write one method file well.

---

## Method File Structure

Create a new file in the `insight-engine/methods/` directory:

```
insight-engine/methods/013-your-method-name.md
```

### File Template

```markdown
# #013 Your Method Name · Subtitle

## Core Positioning

You are a **[role definition]**, [one-sentence description of core function].

**Best for**: [scenario 1], [scenario 2].
**Output value**: [what value this method brings to users].

---

## Output Structure

### 【Section One】
[Content]

### 【Section Two】
[Content]

### 【Section Three】
[Content]

---

## Processing Principles

1. [Principle 1]
2. [Principle 2]
3. [Principle 3]
```

---

## Quality Requirements

A good method file needs to satisfy:

1. **Clear role**: One sentence explaining "who you are"
2. **Clear scenarios**: Explain "when to use this"
3. **Structured output**: Has a clear output template
4. **Processing principles**: Has actionable judgment criteria
5. **Example** (recommended): Has a de-sensitized example

---

## Submission Process

1. Fork the repository
2. Create a branch: `git checkout -b method/013-your-method-name`
3. Write the method file
4. Update the method index in `insight-engine/SKILL.md`
5. Submit a PR

### PR Template

```markdown
## New Method: #013 [Method Name]

### Method Positioning
[One sentence description]

### Best For
[When to use this method]

### Core Value
[What problem this method solves]

### Testing
- [ ] Tested on example recordings?
- [ ] Output meets quality standards?
- [ ] Has a de-sensitized example?
```

---

## Method Numbering

- 001-012: Core methods (built-in)
- 013-099: Community-contributed methods
- 100+: Experimental methods

---

## Reference Methods

Read these method files as references:

- `002-bone-piercing.md` — Gold standard for quality (sharp, structured, with banned words)
- `005-execution-tracker.md` — Gold standard for practicality (tabular, actionable)
- `007-first-principles.md` — Gold standard for analysis (assumption audit, logical rigor)
