# Deep Insight Agent

> **EN**: Transform chaotic meeting recordings, lectures, and strategic discussions into actionable insight assets.
>
> **CN**: 将混沌的会议录音、讲课录音、战略讨论转化为可驱动决策的洞察资产。

**Deep Insight Agent** is a **deep insight analysis framework** — not a summarizer, but a translator of truth. It doesn't repeat what people said. It reveals what they didn't say.

**Deep Insight Agent** 是一个**深度洞察分析框架**——不是总结器，是真相的翻译官。它不复述别人说过的话，而是说出他们没说出口的真话。

---

## Core Capabilities · 核心能力

| EN | CN |
|----|-----|
| **12 Analysis Methods** — Intelligently matched by recording type | **12种分析方法** — 根据录音类型智能匹配 |
| **Multi-User Isolation** — Strict per-user data separation | **多用户隔离** — 每个用户的分析记录严格隔离 |
| **Speaker Identity Inference** — Auto-identify with confidence scoring | **说话人身份推理** — 自动识别，置信度标注 |
| **Cross-Recording Tracking** — Longitudinal stance & action tracking | **跨录音纵向追踪** — 立场演变、行动项兑现追踪 |
| **Structured Output** — Judgment + Evidence + Visualization + Actions | **结构化输出** — 核心判断 + 证据引用 + 可视化 + 行动建议 |

---

## 12 Analysis Methods · 12种分析方法

| # | EN | CN | Best For · 适用场景 |
|---|-----|-----|---------------------|
| 001 | Full Spectrum | 总秘·全谱分析 | Important strategy meetings · 重要战略会议 |
| 002 | Bone Piercing | 问骨·一针见血 | High-density strategy/negotiations · 高密度战略/谈判 |
| 003 | Topic Mining | 选题挖掘 | Lectures, original insights · 课堂/有思想输出的会议 |
| 004 | Knowledge Architect | 知识结构师 | Framework discussions · 讲授型/框架性讨论 |
| 005 | Execution Tracker | 执行力追踪 | Decision meetings, execution syncs · 决策会议/执行同步 |
| 006 | Brainstorm Capture | 脑洞捕捉 | Brainstorms, product discussions · 头脑风暴/产品讨论 |
| 007 | First Principles | 第一性原理 | Strategic reasoning with hidden premises · 有隐性前提的战略推演 |
| 008 | McKinsey Strategy | 麦肯锡战略 | Major strategic trade-offs · 重大战略取舍 |
| 009 | Meeting Secretary | 会议秘书 | Any meeting needing records · 任何需要留档的会议 |
| 010 | Business Negotiation | 商务谈判 | Negotiations, partnerships · 商务谈判/合作协商 |
| 011 | Casual Chat | 朋友聊天 | Friend/family conversations · 朋友/家人聊天 |
| 012 | Opportunity Assessment | 商业机会评估 | Business development, partnerships · 商业拓展/合作洽谈 |

---

## Quick Start · 快速开始

### 1. Clone · 克隆仓库

```bash
git clone https://github.com/qiuyiwu1989-star/Deep-Insight-Agent.git
cd Deep-Insight-Agent
```

### 2. Project Structure · 项目结构

```
Deep-Insight-Agent/
├── insight-engine/
│   ├── en/                         # English version
│   │   ├── SKILL.md                # Core dispatch system
│   │   └── methods/                # 12 analysis methods
│   ├── zh/                         # 中文版
│   │   ├── SKILL.md                # 核心调度系统
│   │   └── methods/                # 12种分析方法
│   ├── references/                 # Shared references · 共享参考
│   └── templates/                  # Output templates · 输出模板
├── memory/
│   ├── DESIGN.md                   # Memory system design · 记忆系统设计
│   ├── schema/                     # Storage definitions · 存储结构
│   └── examples/                   # Examples · 示例文件
├── examples/
│   ├── input/                      # Example inputs · 示例输入
│   └── output/                     # Example outputs · 示例输出
└── docs/
    ├── en/                         # English docs · 英文文档
    └── zh/                         # 中文文档
```

### 3. Entry Points · 入口文件

| Language | Entry Point |
|----------|-------------|
| English | [`insight-engine/en/SKILL.md`](insight-engine/en/SKILL.md) |
| 中文 | [`insight-engine/zh/SKILL.md`](insight-engine/zh/SKILL.md) |

The entry point defines · 入口文件定义了:
- Content diagnosis logic · 内容诊断逻辑
- Method selection routing · 方法选择路由
- Output quality standards · 输出质量标准
- Persistence rules · 持久化规则

### 4. Choose Your Method · 选择方法

| Language | Methods Directory |
|----------|------------------|
| English | [`insight-engine/en/methods/`](insight-engine/en/methods/) |
| 中文 | [`insight-engine/zh/methods/`](insight-engine/zh/methods/) |

---

## Usage · 使用方式

### As an AI Agent Skill · 作为 AI Agent 技能

```yaml
skills:
  - name: deep-insight
    path: ./insight-engine/en/SKILL.md   # or zh/SKILL.md
    methods: ./insight-engine/en/methods/
```

### As a Methodology Reference · 作为方法论参考

Read the method files directly and apply the analysis methods to your work.
直接阅读方法文件，将分析方法应用于你的工作场景。

### As a Framework to Extend · 作为框架扩展

Create your own analysis methods. See:
- [How to Add New Methods (EN)](docs/en/how-to-add-skills.md)
- [如何添加新方法](docs/zh/how-to-add-skills.md)

---

## Core Design Principles · 核心设计理念

### 1. Method Dispatch, Not a Single Analyzer · 方法调度，不是单一分析器

**EN**: The system dynamically selects or combines 12 methods based on content. Mixed recordings are segmented — each part handled with different methods.

**CN**: 系统根据录音内容动态选择或组合12种方法。混合型录音会拆段路由——不同段落用不同方法处理。

### 2. Evidence-Driven, No Empty Talk · 证据驱动，不空谈

**EN**: Every judgment must be supported by original recording text. Insight without evidence = doesn't exist.

**CN**: 每个判断必须有录音原文支撑。没有证据的洞察 = 不存在。

### 3. Silence Is Also Information · 沉默也是信息

**EN**: Topics proposed but ignored, quick topic switches — silence signals are often more important than what was said.

**CN**: 话题被提出后无人响应、快速切换——沉默信号往往比发言更重要。

### 4. Strict Multi-User Isolation · 多用户严格隔离

**EN**: Different users' analysis records are completely isolated. Confirm identity before reviewing history.

**CN**: 不同用户的分析记录完全隔离。回溯历史前先确认身份。

---

## Contributing · 贡献

We welcome community contributions! Each method is a standalone `.md` file.

我们欢迎社区贡献！每种方法是一个独立的 `.md` 文件。

See · 详见: [CONTRIBUTING.md](CONTRIBUTING.md)

---

## License

[MIT License](LICENSE)

---

## Acknowledgments · 致谢

This framework is open-sourced from the core methodology of the **「冷静·深度洞察」** (LengJing · Deep Insight) intelligent agent.

本框架基于「冷静·深度洞察」智能体的核心方法论开源而成。
