[English](https://chatgpt.com/c/README.md) | [简体中文](https://chatgpt.com/c/README.zh-CN.md)

# research-toolkit

> Skills 的价值不在于下载，而在于定制。

面向 AI Coding Agent 的模块化科研工具集（Research Toolkit），用于帮助研究者理解论文、验证科研结论、发现研究机会并加速工程落地。

与许多通用 Prompt 或 Skills 集合不同，**research-toolkit** 更关注科研工作流本身。它并不试图提供一个适用于所有人的“完美 Skill”，而是提供一套可扩展、可定制的 Research OS 框架，让研究者能够逐步将自己的科研习惯和思考方式沉淀为可复用的 Skills。

<img width="1185" height="380" alt="1" src="https://github.com/user-attachments/assets/a4558809-9ee4-4ab6-874e-2134bcd27cb9" />

------

## 为什么要做这个项目？

大多数公开的 Skills 都在追求更强的通用性。

这当然能够帮助更多人使用，但与此同时，也意味着它们很难完全符合某个具体研究者的需求。

科研工作流本质上是高度个性化的：

- 有人更关注数学推导；
- 有人更关注实验设计；
- 有人更关注工程实现；
- 有人更关注创新性与投稿价值；
- 有人更关注领域趋势与未来方向。

因此，并不存在适用于所有人的“最佳 Skill”。

本项目尝试采用另一种思路：

- 使用模块化设计组织 Skills；
- 将共性的研究规范抽离为共享策略；
- 将领域知识与评价标准解耦；
- 允许研究者根据自身需求持续扩展与修改。

与其寻找最好的 Skill，不如构建最适合自己的 Skill。

------

## Skills

| Skill                     | 功能说明                                                     |
| ------------------------- | ------------------------------------------------------------ |
| `paper-reader`            | 高效理解论文，提取元信息，解析方法原理，解释实验结果，构建知识图谱 |
| `paper-reviewer`          | 评估论文质量，分析创新性、技术合理性、实验设计与可复现性     |
| `research-idea-generator` | 挖掘研究空白，发现潜在研究方向，评估创新机会与可行性         |
| `implementation-advisor`  | 制定复现与部署方案，分析工程成本、风险与实现路线             |
| `research-radar`          | 调研研究领域，分析技术演进、研究热点与未来趋势               |

------

## 共享参考策略（Shared References）

所有 Skills 在执行前都会加载统一的研究策略，以保证分析过程的一致性与可靠性。

### 核心策略

| 文件                     | 内容                             |
| ------------------------ | -------------------------------- |
| `research-principles.md` | 科研分析的核心原则与推理规范     |
| `evidence-policy.md`     | 证据等级体系与信息可信度评估标准 |
| `search-policy.md`       | 搜索优先级与检索策略             |
| `failure-handling.md`    | 缺失信息处理与终止条件规范       |

### 按需加载

| 文件                   | 内容                     |
| ---------------------- | ------------------------ |
| `domain-expansions.md` | 领域知识扩展与分析视角   |
| `venue-standards.md`   | 期刊、会议及审稿标准配置 |

------

## 项目结构

```text
research-toolkit/
├── .claude-plugin/
│   └── marketplace.json
│
├── references/
│   ├── research-principles.md
│   ├── evidence-policy.md
│   ├── search-policy.md
│   ├── failure-handling.md
│   ├── domain-expansions.md
│   └── venue-standards.md
│
├── paper-reader/
│   └── SKILL.md
│
├── paper-reviewer/
│   └── SKILL.md
│
├── research-idea-generator/
│   └── SKILL.md
│
├── implementation-advisor/
│   └── SKILL.md
│
└── research-radar/
    └── SKILL.md
```

------

## 安装方式

### Claude Code

```bash
# 添加插件市场
/plugin marketplace add Light-zju/research-toolkit

# 安装工具集
/plugin install research-toolkit@research-toolkit

# 重新加载插件
/reload-plugins
```

### Codex 与其他 Agent

```bash
npx skills add https://github.com/Light-zju/research-toolkit
```

------

## 自定义与扩展

本项目被设计为可持续演化的科研工作流框架。

### 添加你的研究领域

编辑：

```text
references/domain-expansions.md
```

补充：

- 核心概念
- 技术路线
- 分析视角
- 评价标准
- 研究方法论

### 添加目标期刊与会议

编辑：

```text
references/venue-standards.md
```

补充：

- 目标期刊
- 目标会议
- 审稿偏好
- 评价标准
- 投稿要求

### 调整 Skill 触发逻辑

每个 Skill 的触发条件均可通过修改：

```text
SKILL.md
```

中的 Frontmatter 配置进行调整：

```yaml
description:
```

用于控制 Claude Code 在何种场景下自动调用对应 Skill。

------

## 设计理念（Philosophy）

本项目建立在一个非常简单的理念之上：

> Skill 的价值不在于下载，而在于定制。

很多公开 Skills 的目标是覆盖尽可能多的用户。

而本项目更关注另一件事：

如何将研究者自己的工作流、思考习惯与分析框架沉淀为可复用的能力模块。

Research Toolkit 并不是一个终点。

它更像是一套起点。

你可以 Fork 它、修改它、扩展它，并逐渐构建属于自己的 Research OS。

------

## 致谢

感谢 Claude Code Skills 生态提供的灵感。

如果这个项目对你的科研工作有所帮助，欢迎提出 Issue、分享改进建议或提交 Pull Request。

------

## License

MIT
