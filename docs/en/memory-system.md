# Memory System Design Principles

## Why a Memory System?

A single analysis has limited value. Real insight comes from **longitudinal tracking across time and scenarios**:

- How have stances changed between the 1st and 10th meeting of the same project?
- Is a person consistent across different scenarios?
- Were the action items from last time actually fulfilled?

The memory system gives the Agent "long-term memory" to:
1. **Link history**: Automatically search related historical records before analysis
2. **Track changes**: Compare stance evolution and action item fulfillment
3. **Learn from corrections**: Remember user corrections to avoid repeating mistakes

---

## User Isolation Principles

### Problem

If multiple users share the same memory system:
- User A's analysis results may be visible to User B
- Different users' contexts may be confused
- Privacy leak risk

### Solution

1. **Strict isolation**: Each user's analysis records stored independently
2. **Identity confirmation**: Must confirm user identity before reviewing history
3. **Don't assume**: Don't assume past collaboration with the user
4. **Don't cross-reference**: Don't reveal User A's content to User B

### Implementation

```
memory/
├── users/
│   ├── user-a.md    # User A's profile
│   └── user-b.md    # User B's profile
├── analyses/
│   ├── user-a/      # User A's analysis records
│   └── user-b/      # User B's analysis records
```

---

## Cross-Recording Correlation

### Trigger Conditions

- Nth meeting of the same project
- Same person appears again
- User explicitly requests "compare with history"

### Correlation Dimensions

| Dimension | Comparison | Value |
|-----------|-----------|-------|
| Core topics | Advance/stagnate/regress/new | See project progress |
| Person stances | Harden/soften/drift | See human dynamics |
| Action items | Complete/partial/not done/not mentioned | Track execution |
| Contradictions | New/existing | See risk evolution |

---

## Auto-Learning

### Correction Types

| Type | Example | Learning Method |
|------|---------|----------------|
| Speaker correction | "Speaker 1 is not Zhang San, it's Li Si" | Update speaker identification logic |
| Method correction | "No need for Bone Piercing, just give execution list" | Adjust method selection preference |
| Depth correction | "Analysis too shallow, didn't penetrate surface" | Raise quality standards |
| Missed signal | "You missed Wang Wu's silence" | Add silence signal detection |

### Correction Record

```markdown
# YYYY-MM-DD Correction Record

## Correction Content
[What was corrected]

## Correction Type
[Speaker/Method/Depth/Missed Signal]

## Applicable Scenario
[How to apply this correction in next analysis]
```

---

## Design Trade-offs

### Memory Depth vs Response Speed

- **Deep memory**: Search all history, inject full context → More comprehensive, but slower
- **Shallow memory**: Only search recent records → Faster, but may miss key context

**Current choice**: Quick scan ≤3 seconds, total timeout 15 seconds. Skip if exceeded.

### Memory Completeness vs Privacy Protection

- **Full memory**: Save all analysis details → More accurate tracking, but higher privacy risk
- **Minimal memory**: Only save core judgments → More private, but limited tracking

**Current choice**: Save core judgments and action items, don't save raw recording transcripts.
