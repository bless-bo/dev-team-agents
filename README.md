# Dev Team Agents

Multi-agent software development team coordination system.

## Team Roles

| Role | Agent ID | Model | Responsibilities |
|------|----------|-------|------------------|
| Project Manager | `main` | MiniMax | Requirement analysis, task dispatch, coordination |
| Architect | `architect` | 智谱 GLM-4.7 | Technical architecture, design review |
| Software Designer | `designer` | 智谱 GLM-4.7 | Detailed design, interface specs |
| Developer | `developer` | 智谱 GLM-4.7 | Code implementation |
| Test Engineer | `tester` | 智谱 GLM-4.7 | Test cases, bug reports, QA |

## Workflow

```
Requirement Issue
       ↓
Architecture Design (architect) → User LGTM
       ↓
Detailed Design (designer) → User LGTM
       ↓
Code Implementation (developer)
       ↓
Multi-Agent Code Review (architect + designer + developer + tester)
       ↓
User Final LGTM → Done
```

## Multi-Agent Code Review

When development is ready, ALL agents participate:

| Agent | Review Focus |
|-------|--------------|
| **architect** | Architecture compliance, tech choices |
| **designer** | Design completeness, interface standards |
| **developer** | Code quality, best practices |
| **tester** | Test coverage, edge cases, risks |

## Issue Labels

- `requirement` - New requirements
- `architecture` - Architecture design phase
- `design` - Detailed design phase
- `development` - Development phase
- `review` - Multi-agent code review phase
- `pending-lgtm` - Awaiting your approval
- `approved` - Approved, proceed
- `rejected` - Rejected, needs rework

## Quick Start

1. Tell me: "我要开发 XXX"
2. I create Requirement Issue
3. Agents work through phases
4. You LGTM at each phase gate
5. After multi-agent review, you final LGTM

## Repository

https://github.com/bless-bo/dev-team-agents
