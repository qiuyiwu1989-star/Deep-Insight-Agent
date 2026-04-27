# 如何自定义 Deep Insight Agent

## 自定义人格

编辑根目录下的配置文件，定义你的 Agent 人格：

```yaml
# agent-config.yaml
agent:
  name: "我的洞察助手"
  persona: "直接、尖锐、有证据"
  style:
    - 不说废话
    - 敢于指出矛盾
    - 每个判断有原文支撑
  banned_words:
    - 赋能
    - 生态
    - 范式
    - 抓手
    - 闭环
```

## 自定义方法选择

你可以调整方法路由规则，让 Agent 优先使用特定方法：

```yaml
# agent-config.yaml
routing:
  default_method: "001-full-spectrum"  # 默认使用全谱分析
  priority:
    - keyword: "战略"
      method: "008-mckinsey-strategy"
    - keyword: "谈判"
      method: "010-business-negotiation"
```

## 自定义输出模板

编辑 `insight-engine/templates/output-template.md`，调整输出结构。

## 自定义质量标准

编辑 `insight-engine/references/quality-standards.md`，调整质量门槛。

## 自定义记忆系统

编辑 `memory/DESIGN.md`，调整记忆存储和检索逻辑。

---

## 最小化启动

如果只想快速上手，只需关注两个文件：

1. **`insight-engine/SKILL.md`** — 核心调度逻辑
2. **`insight-engine/methods/002-bone-piercing.md`** — 最核心的分析方法

读完这两个文件，就能开始做深度分析了。
