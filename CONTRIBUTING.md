# Contributing to Deep Insight Agent · 贡献指南

Thank you for your interest! We welcome community contributions.

感谢你的关注！我们欢迎社区贡献。

---

## Ways to Contribute · 贡献方式

| EN | CN |
|----|-----|
| **Submit new analysis methods** — Each method is a standalone `.md` file | **提交新的分析方法** — 每种方法是一个独立的 `.md` 文件 |
| **Improve existing methods** — Fix logic, improve readability, add examples | **改进现有方法** — 修复逻辑、增加可读性、补充示例 |
| **Improve documentation** — Translate, add examples, improve guides | **完善文档** — 翻译、补充示例、改进指南 |
| **Report issues** — Routing issues, template problems, quality gaps | **报告问题** — 路由不准确、模板不合理、质量标准不清晰 |

---

## Submission Process · 提交流程

1. **Fork** this repository · Fork 本仓库
2. **Create a branch** · 创建分支:
   ```bash
   git checkout -b method/013-your-method-name
   ```
3. **Commit changes** · 提交更改:
   ```bash
   git commit -m "Describe your changes · 描述你的更改"
   ```
4. **Push branch** · 推送分支:
   ```bash
   git push origin your-branch-name
   ```
5. **Create a PR** · 创建 PR

### Branch Naming · 分支命名规范

| Type · 类型 | Pattern · 格式 | Example · 示例 |
|-------------|---------------|----------------|
| New method · 新方法 | `method/013-name` | `method/013-risk-analysis` |
| Improvement · 改进 | `improve/what` | `improve/bone-piercing-clarity` |
| Documentation · 文档 | `docs/what` | `docs/zh-quickstart` |
| Fix · 修复 | `fix/what` | `fix/typo-in-readme` |

---

## Method Contribution Spec · 方法贡献规范

### File Structure · 文件结构

```
insight-engine/{en|zh}/methods/013-your-method-name.md
```

### Must Include · 必须包含

1. **Core positioning** — One sentence: "who you are" · 核心定位——一句话说清"你是谁"
2. **Best for** — When to use this method · 适用场景
3. **Output structure** — Clear output template · 输出结构——明确的输出模板
4. **Processing principles** — Actionable criteria · 处理原则——可执行的判断标准

### Recommended · 推荐包含

1. **De-sensitized example** · 脱敏示例
2. **Relationship with other methods** · 与其他方法的关系
3. **Quality standards** · 质量标准

### Quality Requirements · 质量要求

- Every judgment must have basis · 每个判断必须有依据
- Output must be actionable · 输出结构必须可操作
- No filler or empty talk · 不能有废话和套话
- Language: direct, sharp, evidence-based · 语言直接、尖锐、有证据

---

## PR Template · PR 模板

```markdown
## New Method: #013 [Method Name] · 新方法：#013 [方法名]

### Method Positioning · 方法定位
[One sentence · 一句话]

### Best For · 适用场景
[When to use · 什么时候用]

### Core Value · 核心价值
[What problem it solves · 解决什么问题]

### Testing · 测试
- [ ] Tested on example recordings? · 在示例录音上测试过？
- [ ] Output meets quality standards? · 输出符合质量标准？
- [ ] Has de-sensitized example? · 有脱敏示例？
```

---

## Code of Conduct · 行为准则

### We Welcome · 欢迎

- Direct, sharp, evidence-based feedback · 直接、尖锐、有证据的反馈
- Fact-based discussions · 基于事实的讨论
- Constructive criticism · 建设性批评

### We Don't Welcome · 不欢迎

- Personal attacks · 人身攻击
- Unfounded speculation · 无依据的主观臆断
- Filler and empty talk · 套话和废话

---

## License

Contributions will be published under the [MIT License](LICENSE).

贡献内容将按照 [MIT License](LICENSE) 发布。
