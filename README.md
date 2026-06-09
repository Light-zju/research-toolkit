# research-toolkit

Academic research toolkit for AI coding agents — a set of 5 skills that help you read papers, review papers, generate research ideas, plan implementations, and survey research fields. All skills share a common set of reference policies for rigorous, evidence-driven research.

## Skills

| Skill | Description |
|-------|-------------|
| `paper-reader` | Understand papers efficiently — extract metadata, explain methods, interpret experiments, build knowledge graphs |
| `paper-reviewer` | Evaluate scientific quality — assess novelty, technical soundness, experimental quality, provide reviewer feedback |
| `research-idea-generator` | Discover research opportunities — gap analysis, cross-domain exploration, feasibility assessment |
| `implementation-advisor` | Plan reproduction and deployment — reproducibility analysis, engineering roadmap, risk assessment |
| `research-radar` | Survey research fields — trend analysis, technology evolution, landscape mapping |



## Shared References

All skills load these policies before execution:

| Reference | Content |
|-----------|---------|
| `research-principles.md` | 8 core research principles (understand before judging, evidence before conclusion, etc.) |
| `evidence-policy.md` | 4-level evidence hierarchy for source evaluation |
| `search-policy.md` | Search priority rules and retry limits |
| `failure-handling.md` | Guidelines for missing information and process termination |

On-demand references:
- `domain-expansions.md` — domain-specific knowledge (navigation, optics, DL, RL, LLM, agents)
- `venue-standards.md` — venue-specific evaluation criteria (TIM, TNNLS, ICRA, NeurIPS)



## Installation

### Claude Code

```bash
# Register the marketplace
/plugin marketplace add Light-zju/research-toolkit

# Install the skills
/plugin install research-toolkit@research-toolkit

# Reload to apply
/reload-plugins
```

### Codex / Other Agents (via npx skills)

```bash
npx skills add https://github.com/Light-zju/research-toolkit
```



## Directory Structure

```
research-toolkit/
├── .claude-plugin/
│   └── marketplace.json
├── references/
│   ├── research-principles.md
│   ├── evidence-policy.md
│   ├── search-policy.md
│   ├── failure-handling.md
│   ├── domain-expansions.md
│   └── venue-standards.md
├── paper-reader/
│   └── SKILL.md
├── paper-reviewer/
│   └── SKILL.md
├── research-idea-generator/
│   └── SKILL.md
├── implementation-advisor/
│   └── SKILL.md
└── research-radar/
    └── SKILL.md
```



## Customization

To adapt for your own research domain:
1. Edit `references/domain-expansions.md` to add your field's key concepts
2. Edit `references/venue-standards.md` to add your target venues
3. Each skill's `SKILL.md` frontmatter `description` controls when it triggers — adjust for your use cases



## License

MIT
