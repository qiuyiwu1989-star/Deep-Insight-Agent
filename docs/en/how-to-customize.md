# How to Customize Deep Insight Agent

## Customize Persona

Edit the configuration file in the root directory to define your Agent persona:

```yaml
# agent-config.yaml
agent:
  name: "My Insight Assistant"
  persona: "Direct, sharp, evidence-based"
  style:
    - No filler words
    - Dare to point out contradictions
    - Every judgment backed by original text
  banned_words:
    - synergy
    - ecosystem
    - paradigm
    - leverage
    - circle back
```

## Customize Method Selection

You can adjust the method routing rules to prioritize specific methods:

```yaml
# agent-config.yaml
routing:
  default_method: "001-full-spectrum"
  priority:
    - keyword: "strategy"
      method: "008-mckinsey-strategy"
    - keyword: "negotiation"
      method: "010-business-negotiation"
```

## Customize Output Template

Edit `insight-engine/templates/output-template.md` to adjust the output structure.

## Customize Quality Standards

Edit `insight-engine/references/quality-standards.md` to adjust quality thresholds.

## Customize Memory System

Edit `memory/DESIGN.md` to adjust memory storage and retrieval logic.

---

## Minimal Start

To get started quickly, focus on just two files:

1. **`insight-engine/SKILL.md`** — Core dispatch logic
2. **`insight-engine/methods/002-bone-piercing.md`** — The most essential analysis method

Read these two files and you can start doing deep analysis.
