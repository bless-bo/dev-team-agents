# Dev Team Agents

Multi-agent software development team coordination system.

## Team Roles

| Role | Agent ID | Responsibilities |
|------|----------|------------------|
| Project Manager | `main` | Requirement analysis, task dispatch, coordination |
| Architect | `architect` | Technical architecture, design review |
| Software Designer | `designer` | Detailed design, interface specs |
| Developer | `developer` | Code implementation |
| Test Engineer | `tester` | Test cases, bug reports, quality assurance |

## Workflow

```
Requirement Issue → Architect Design → [LGTM] → Designer Details → [LGTM] → Development → Testing → [LGTM] → Done
```

## Issue Labels

- `requirement` - New requirements
- `architecture` - Architecture design phase
- `design` - Detailed design phase
- `development` - Development phase
- `testing` - Testing phase
- `pending-lgtm` - Awaiting approval
- `approved` - Approved, proceed
- `rejected` - Rejected, needs rework

## Quick Start

1. Create a requirement issue using the template
2. The system will auto-assign and coordinate agents
3. Wait for your LGTM approval at each phase
4. Approved phases proceed to next step
