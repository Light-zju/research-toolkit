<div align="right">

[English](README.md) | [简体中文](README.zh-CN.md)

</div>

# research-toolkit

> Skills are not just tools to download — they are a way to encode and reuse your own research workflow.

A modular Research OS for AI coding agents, designed to help researchers understand papers, evaluate scientific claims, discover research opportunities, and accelerate implementation.

Unlike many generic prompt collections, **research-toolkit** focuses on building reusable research workflows. The goal is not to provide a single "perfect" skill, but to offer a framework that researchers can customize according to their own domains, interests, and working styles.

<img width="1185" height="380" alt="1" src="https://github.com/user-attachments/assets/074c8de5-5a07-4087-862a-50208005ccb3" />

---

## Why This Project?

Most public skills aim for maximum generality.

That makes them useful for many people, but often less effective for any specific individual.

Research workflows are highly personal:

* Some researchers focus on mathematical derivations.
* Some focus on experimental design.
* Some care most about engineering implementation.
* Some care about novelty, reproducibility, and publication potential.

As a result, there is no universally "best" research skill.

This project takes a different approach:

* Build modular skills.
* Share common research principles.
* Customize domain knowledge.
* Adapt the workflow to your own research style.

---

## Skills

| Skill                     | Purpose                                                                                                         |
| ------------------------- | --------------------------------------------------------------------------------------------------------------- |
| `paper-reader`            | Understand papers efficiently, extract metadata, explain methods, interpret experiments, build knowledge graphs |
| `paper-reviewer`          | Evaluate scientific quality, assess novelty, technical soundness, experimental design, and reproducibility      |
| `research-idea-generator` | Discover research opportunities through gap analysis and cross-domain exploration                               |
| `implementation-advisor`  | Plan reproduction, deployment, engineering roadmaps, and risk assessment                                        |
| `research-radar`          | Analyze research landscapes, technology evolution, and future trends                                            |

---

## Shared References

All skills share a lightweight policy layer to ensure consistent behavior.

### Core References

| Reference                | Purpose                                              |
| ------------------------ | ---------------------------------------------------- |
| `research-principles.md` | Core research principles and reasoning rules         |
| `evidence-policy.md`     | Evidence hierarchy and source credibility guidelines |
| `search-policy.md`       | Search priorities and retrieval strategies           |
| `failure-handling.md`    | Missing information and termination policies         |

### Optional References

| Reference              | Purpose                                                  |
| ---------------------- | -------------------------------------------------------- |
| `domain-expansions.md` | Domain-specific knowledge and analysis perspectives      |
| `venue-standards.md`   | Venue-specific review criteria and publication standards |

---

## Directory Structure

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

---

## Installation

### Claude Code

```bash
# Register marketplace
/plugin marketplace add Light-zju/research-toolkit

# Install toolkit
/plugin install research-toolkit@Light-zju-research-toolkit

# Reload plugins
/reload-plugins
```

### Codex and Other Agents

```bash
npx skills add https://github.com/Light-zju/research-toolkit
```

---

## Customization

The toolkit is designed to be modified.

### Add Your Research Domain

Edit:

```text
references/domain-expansions.md
```

Add:

* domain concepts
* evaluation perspectives
* technical priorities
* research methodologies

### Add Your Target Venues

Edit:

```text
references/venue-standards.md
```

Add:

* journals
* conferences
* review criteria
* publication expectations

### Modify Skill Trigger Conditions

Each skill can be customized by editing:

```text
SKILL.md
```

especially its frontmatter:

```yaml
description:
```

which controls when the skill should be activated.

---

## Philosophy

This project is built around a simple idea:

> The value of a skill is not in downloading it, but in adapting it.

Instead of searching endlessly for the perfect skill, researchers can gradually encode their own workflows, habits, and reasoning processes into reusable skills.

The toolkit is intended to be a starting point, not an endpoint.

Fork it, modify it, and make it your own.

---

## License

MIT
