# Deep Insight Agent

> Transform chaotic meeting recordings, lectures, and strategic discussions into actionable insight assets.

Deep Insight Agent is a **deep insight analysis framework** — not a summarizer, but a translator of truth.

It doesn't repeat what people said. It reveals what they didn't say.

[中文版](README-zh.md)

---

## Core Capabilities

- **12 Analysis Methods**: Intelligently matched by recording type — covering strategy, negotiation, brainstorming, lectures, and more
- **Multi-User Isolation**: Each user's analysis records are strictly isolated, no cross-user references
- **Speaker Identity Inference**: Automatically identify speakers from transcripts with cross-validation and confidence scoring
- **Cross-Recording Longitudinal Tracking**: Automatically compare stance evolution and action item fulfillment across multiple meetings
- **Structured Output**: Core judgments + evidence citations + visualizations + action recommendations — no filler text

---

## 12 Analysis Methods

| # | Method | Core Function | Best For |
|---|--------|--------------|----------|
| 001 | Full Spectrum | Complete 8-dimensional structured analysis | Important strategy meetings |
| 002 | Bone Piercing | Penetrate surface, reveal true intentions & core contradictions | High-density strategy/fundraising/partnership negotiations |
| 003 | Topic Mining | Extract writing materials & article directions from recordings | Lectures, meetings with original insights |
| 004 | Knowledge Architect | Concept extraction & knowledge graph construction | Lectures, framework discussions |
| 005 | Execution Tracker | Distinguish commitments/assumptions/hanging items | Decision meetings, execution syncs |
| 006 | Brainstorm Capture | Identify & develop creative sparks | Brainstorms, product discussions |
| 007 | First Principles | Core assumption audit & cognitive blind spot exposure | Strategic reasoning with hidden premises |
| 008 | McKinsey Strategy | Strategic proposition identification & choice cost analysis | Major strategic trade-offs |
| 009 | Meeting Secretary | Structured meeting documentation | Any meeting that needs records |
| 010 | Business Negotiation | Game analysis: power, strategy, interests | Business negotiations, partnership discussions |
| 011 | Casual Chat | Relationship & personality analysis | Friend/family conversations |
| 012 | Opportunity Assessment | Collaboration value analysis: pain points, fit, risk signals | Business development, partnership exploration |

---

## Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/qiuyiwu1989-star/Deep-Insight-Agent.git
cd Deep-Insight-Agent
```

### 2. Understand the Structure

```
Deep-Insight-Agent/
├── insight-engine/
│   ├── SKILL.md              # Core dispatch system (entry point)
│   ├── methods/              # 12 analysis methods
│   ├── references/           # Routing rules, quality standards
│   └── templates/            # Output templates
├── memory/
│   ├── DESIGN.md             # Memory system design
│   ├── schema/               # Storage structure definitions
│   └── examples/             # Example files
├── examples/
│   ├── input/                # Example inputs
│   └── output/               # Example outputs
└── docs/
    ├── how-to-customize.md   # How to customize
    ├── how-to-add-skills.md  # How to add new methods
    └── memory-system.md      # Memory system design principles
```

### 3. Read the Entry Point

Start with `insight-engine/SKILL.md` — the dispatch center that defines:
- Content diagnosis logic
- Method selection routing
- Output quality standards
- Persistence rules

### 4. Choose Your Method

Based on your recording type, select the corresponding method file from `insight-engine/methods/` and follow its role definition and output structure.

---

## Usage

### As an AI Agent Skill

Load the `insight-engine/` directory as a skill in your AI Agent (OpenClaw, LangChain, etc.):

```yaml
skills:
  - name: deep-insight
    path: ./insight-engine/SKILL.md
    methods: ./insight-engine/methods/
```

### As an Analysis Methodology Reference

Read the method files in `insight-engine/methods/` directly and apply the analysis methods to your work.

### As a Framework to Extend

Create your own analysis methods based on the existing method structure. See [How to Add New Methods](docs/en/how-to-add-skills.md).

---

## Core Design Principles

### 1. Method Dispatch, Not a Single Analyzer

The system doesn't have just one analysis mode. It **dynamically selects or combines** 12 methods based on content. Mixed recordings are segmented — the first half about business development, the second half about casual chat — each handled with different methods.

### 2. Evidence-Driven, No Empty Talk

Every judgment must be supported by original recording text. Insight without evidence = doesn't exist.

### 3. Silence Is Also Information

Topics proposed but ignored by everyone, quick topic switches — these silence signals are often more important than what was actually said.

### 4. Strict Multi-User Isolation

Different users' analysis records are completely isolated. Before reviewing history, confirm identity. Don't assume past collaboration. Don't cross-reference between users.

---

## Contributing

We welcome community contributions of new analysis methods! Each method is a standalone `.md` file — no need to understand the entire framework.

See [CONTRIBUTING.md](CONTRIBUTING.md)

---

## License

MIT License - see [LICENSE](LICENSE)

---

## Acknowledgments

This framework is open-sourced from the core methodology of the "冷静·深度洞察" (LengJing · Deep Insight) intelligent agent.
